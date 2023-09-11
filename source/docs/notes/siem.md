# SIEM stack

Security information and event management (SIEM) is an approach to security management that combines security information management (SIM) and security event management (SEM) functions into one security management system.

It is a software solution that aggregates and analyses activity from many different resources across an IT infrastructure. SIEM collects security data from network devices, servers, domain controllers, etc., and search queries can be done to look for specific answers from ingested logs. 

## Tools and architecture

Many SIEM tools exist, Kibana, Splunk, Elastic SIEM, Datadog, QRadar, UnderDefense, etc., and architecture varies. In general, if a tool has a SIEM engine, it contains three components:

* A data collector forwarding selected audit logs from a host (agent based or host based log streaming into index and aggregation point)
* An aggregation point for parsing, correlation, and data normalisation.
* A search node used for visualisation, queries, reports, and alerts (actual analysis takes place on a search node)

## SIEM stack requirements

[![SIEM stack](../../_static/images/siem-stack.png)](https://socfortress.medium.com/build-your-own-siem-stack-with-open-source-tools-series-39da0f2d412a)

### Log ingestion

* Collect logs originating on endpoint devices, network devices, or 3rd party services
* Normalise log fields to universal names for faster searching and better visualisations
* Ensure caching of logs if backend storage is busy or offline
* Ability to ingest mobile logs

### Log analysis

* Analyse logs from endpoints/services
* Determine the severity of logs ingested via log analysis
* Ability to discard noisy alerts to limit overflow of unnecessary data

### Backend storage

* Store received logs for a period of time
* Fast searching and viewing of data
* Ability to provide access control to stored logs

### Visualisation

* Ability to view logs via widgets
* Fast searching and viewing of data
* Support the ability to read from multiple log storages (Elastic, MySQL, ...)

### Intelligence enrichment

* Enrich received log with threat intelligence gathered from various providers
* Ability to parse and store selected responses so that only crucial data is stored
* Automated, so that SOC analysts are not having to manually attempt to enrich logs

### Case management

* Platform to view and react to high severity events
* Allow collaboration with multiple SOC analysts
* Allow responsive actions so that analysts can trigger events on their endpoints (escalation procedure)

### Automate

* SOAR platform
* Ability to automate workflows in response to critical alerts, failed health checks, or ticket analysis
* Fully customisable, and fast

### Investigation

* Incident response
* Quarantine a device
* Ability to remotely collect endpoint forensics

### Health monitoring

* Monitor resources consumed on endpoints
* Monitor services/process whose stoppage would cause operational impact
* Ability to alert in real-time when health check thresholds are met

## Testlab

Gradually building up to something useful for the IPA project:

### Wazuh

* [Wazuh single-node deployment with docker](https://testlab.tymyrddin.dev/docs/siem/wazuh-single-node), bare-bones single-node deployment: One Wazuh manager, indexer, and dashboard node.
* [Wazuh multi-node deployment with docker](https://testlab.tymyrddin.dev/docs/siem/wazuh-multi-node), two Wazuh manager nodes (one master and one worker), three Wazuh indexer nodes, and a Wazuh dashboard node.
* [Building Wazuh images](https://testlab.tymyrddin.dev/docs/siem/wazuh-images) for making changes for the IPA project.

Wazuh agents can easily be installed on endpoints such as laptops, desktops, servers, cloud instances, or virtual machines. For mobile endpoints, [Android syslogs can be forwarded to Wazuh](https://wazuh.com/blog/how-to-forward-android-syslog-to-wazuh/), but iOS and iPad are still a problem. A [stackoverflow answer from 12 years ago](https://stackoverflow.com/questions/7277804/ios-iphone-ipad-ipodtouch-view-real-time-console-log-terminal/19148654#19148654) suggests using the [libimobiledevice](https://libimobiledevice.org/) library, which supports wirelessly viewing an iOS device's syslog, making it possible to send the devices' logs via the local network to a Mac, and with something like that it would be possible to run a script that forwards the logs to the Wazuh Manager. Meaning it is only monitored when in reach of the Mac, and the connection is not secured. Other than that, sending the logs directly from the device to a Wazuh Manager over a secured connection is (technically) possible, but requires development of an iOS native application. I haven't found any such proposal on any roadmaps (yet).

Still, the Wazuh installations were exercise, and Wazuh is easy to install and use.

## Testlab

* [SIEM stack](https://testlab.tymyrddin.dev/docs/siem/readme) All tools in these stacks are open source and free. 
