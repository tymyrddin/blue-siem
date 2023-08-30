# Delivery phase

We have identified various IP addresses, domains and Email addresses associated with this adversary.

Attackers create malware and infect devices to gain initial access or evade defenses and find ways to deliver 
it through different means. 

This investigation phase would be to use the information we have about the adversary and use various Threat Hunting 
platforms and OSINT sites to find any malware linked with the adversary.

Threat Intel report suggested that this adversary group Poison lvy appears to have a secondary attack vector in case 
the initial compromise fails. Our objective would be to understand more about the attacker and their methodology and 
correlate the information found in the logs with various threat Intel sources.

## OSINT sites

* [Virustotal](https://www.virustotal.com/gui/file/9709473ab351387aab9e816eff3910b9f28a7a70202e250ed46dba8f820f34a8/community)
* [ThreatMiner](https://www.threatminer.org/host.php?q=23.22.63.114#gsc.tab=0&gsc.q=23.22.63.114&gsc.page=1)
* [Hybrid-Analysis](https://www.hybrid-analysis.com/sample/9709473ab351387aab9e816eff3910b9f28a7a70202e250ed46dba8f820f34a8?environmentId=100)

## Questions

**What is the HASH of the Malware associated with the APT group?**

| ![hash](../../_static/images/splunk-wayne11.png) |
|:------------------------------------------------:|
|        `c99131e0169171935c5ac32615ed6261`        |

**What is the name of the Malware associated with the Poison Ivy Infrastructure?**

| ![malware name](../../_static/images/splunk-wayne12.png) |
|:--------------------------------------------------------:|
|             `MirandaTateScreensaver.scr.exe`             |


