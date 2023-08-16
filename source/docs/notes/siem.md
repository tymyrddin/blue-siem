# Security information and event management

Security information and event management (SIEM) is an approach to security management that combines security information management (SIM) and security event management (SEM) functions into one security management system.

It is a software solution that aggregates and analyses activity from many different resources across an IT infrastructure. SIEM collects security data from network devices, servers, domain controllers, etc., and search queries can be done to look for specific answers from ingested logs. 

## Tools and architecture

Many SIEM tools exist, Kibana, Splunk, Elastic SIEM, Datadog, QRadar, UnderDefense, etc., and architecture varies. In general, if a tool has a SIEM engine, it contains three components:

* A data collector forwarding selected audit logs from a host (agent based or host based log streaming into index and aggregation point)
* An aggregation point for parsing, correlation, and data normalisation.
* A search node used for visualisation, queries, reports, and alerts (actual analysis takes place on a search node)