# Adding data

Splunk can ingest any data. As per the Splunk documentation, when data is added to Splunk, the data is processed and transformed into a series of individual events. 

The data sources can be event logs, website logs, firewall logs, etc. Data sources are grouped into categories. 

Upload the `VPN_logs` data and create an index `VPN_Logs`. 

**How many events are present in the log file?**

| ![Splunk Basics](../../_static/images/splunk-c1.png)
|:--:|
| Answer: `2862` |

**How many log events by the user Maleena are captured?**

| ![Splunk Basics](../../_static/images/splunk-c2.png)
|:--:|
| Answer: `60` |

**What is the name associated with IP `107.14.182.38`?**

| ![Splunk Basics](../../_static/images/splunk-c3.png)
|:--:|
| Answer: `Smith` |

**What is the number of events that originated from all countries except France?**

| ![Splunk Basics](../../_static/images/splunk-c4.png)
|:--:|
| Answer: ` 2814` |

**How many VPN Events were observed by the IP 107.3.206.58?**

| ![Splunk Basics](../../_static/images/splunk-c5.png)
|:--:|
| Answer: `14` |

## More rooms

* [Incident Handling with Splunk](https://tryhackme.com/room/splunk201)
* [Investigating With Splunk](http://tryhackme.com/jr/investigatingwithsplunk)
* [Benign - Challenge](http://tryhackme.com/jr/benign)
* [PoshEclipse - Challenge](http://tryhackme.com/jr/posheclipse)
