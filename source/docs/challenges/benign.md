# Benign



One of the client’s IDS indicated a potentially suspicious process execution indicating one of the hosts from the 
HR department was compromised. Some tools related to network information gathering/scheduled tasks were executed 
which confirmed the suspicion. Due to limited resources, we could only pull the process execution logs with 
Event ID: `4688` and ingested them into Splunk with the index `win_eventlogs` for further investigation.

The network is divided into three logical segments. 

IT Department:

* James
* Moin
* Katrina

HR department:

* Haroon
* Chris
* Diana

Marketing department:

* Bell
* Amelia
* Deepak

## Questions

**How many logs are ingested from the month of March?**

Answer: ``

**Imposter Alert: There seems to be an imposter account observed in the logs, what is the name of that user?**

Answer: ``

**Which user from the HR department was observed to be running scheduled tasks?**

Answer: ``

**Which user from the HR department executed a system process (LOLBIN) to download a payload from a file-sharing host.**

Answer: ``

**To bypass the security controls, which system process (lolbin) was used to download a payload from the internet?**

Answer: ``

**What was the date that this binary was executed by the infected host? format (YYYY-MM-DD)**

Answer: ``

**Which third-party site was accessed to download the malicious payload?**

Answer: ``

**What is the name of the file that was saved on the host machine from the C2 server during the post-exploitation phase?**

Answer: ``

**The suspicious file downloaded from the C2 server contained malicious content with the pattern THM{..........}; what is that pattern?**

Answer: ``

**What is the URL that the infected host connected to?**

Answer: ``