# Components

## Splunk forwarder

Splunk forwarder is a lightweight agent installed on the endpoint intended to be monitored, and its main task is to 
collect the data and send it to the Splunk instance. It does not affect the endpoint's performance as it takes very 
few resources to process. Some key data sources are:

* Web server generating web traffic.
* Windows machine generating Windows Event Logs, PowerShell, and Sysmon data.
* Linux host generating host-centric logs.
* Database generating DB connection requests, responses, and errors.

## Splunk indexer

Splunk indexer plays the main role in processing the data it receives from forwarders. It takes the data, normalises 
it into field-value pairs, determines the datatype of the data, and stores them as events. Processed data is easy to 
search and analyse.

## Search head

Splunk search head is the place within the Search & Reporting App where users can search the indexed logs. 
When the user searches for a term or uses a Search language known as Splunk Search Processing Language, the request 
is sent to the indexer and the relevant events are returned in the form of field-value pairs.

Search head also provides the ability to transform the results into presentable tables, visualizations like 
pie-chart, bar-chart and column-chart.

