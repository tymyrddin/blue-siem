# Diamond model

The diamond model of intrusion analysis is an approach to authenticate and track cyber threats. In this approach, every incident is depicted as a diamond. The methodology underlines the relationships and characteristics of four components of the diamond: adversary, capability, infrastructure, and victim. These four core elements are connected in relationship between each other which can then be analytically examined to further uncover insights and gain knowledge of malicious activities. 

| ![Empire's capabilities](../../_static/images/starwars-diamond.png)
|:--:|
| Empire’s capabilities and infrastructure, as well as the dependencies or tactics that enable them. |

The diamond model of intrusion analysis illustrates that an `adversary` uses a `capability` over an `infrastructure` against a `victim`.

## Adversary

An adversary is an organisation or threat actor responsible for leveraging a capability against a victim to fulfill its goals. The adversary is the person who stands behind the cyberattack. 

The distinction between adversary operator and adversary makes intent, attribution, adaptability, and persistence clear by helping to frame the relationship between an adversary and victim pair.  

It is difficult to identify an adversary during the first stages of a cyberattack. Using data collected from an incident or breach, signatures, and other relevant information can help determine who the adversary might be.

* Adversary Operator is the hacker or person(s) conducting the intrusion activity.
* Adversary Customer is the entity that stands to benefit from the activity in the intrusion. It may be the same person who stands behind the adversary operator, or it may be a separate person or group. An adversary customer could control different operators simultaneously. Each operator might have its capabilities and infrastructure.

## Capability

The capabilities refer to the tools and techniques used by an adversary in an event. It highlights the adversary's tactics, techniques, and procedures (TTPs) and includes all techniques used to attack the victims, from the less sophisticated methods, such as manual password guessing, to the most sophisticated techniques, like developing malware or a malicious tool. 

* Capability Capacity is all the vulnerabilities and exposures that the individual capability can use. 
* An Adversary Arsenal is a set of capabilities that belong to an adversary. The combined capacities of an adversary's capabilities make it the adversary's arsenal.

An adversary must have the required capabilities. The capabilities can be malware and phishing email development skills or, at least, access to capabilities, such as acquiring malware or ransomware as a service.

## Infrastructure

The infrastructure includes the physical or logical communication structures such as IP or e-mail addresses, domain names, and others, employed by an adversary to deliver a capability. 

* Type 1 Infrastructure is the infrastructure controlled or owned by the adversary. 
* Type 2 Infrastructure is the infrastructure controlled by an intermediary. Sometimes the intermediary might or might not be aware of it. This is the infrastructure that a victim will see as the adversary. Type 2 Infrastructure has the purpose of obfuscating the source and attribution of the activity. Type 2 Infrastructure includes malware staging servers, malicious domain names, compromised email accounts, etc.
* Service Providers are organisations that provide services considered critical for the adversary availability of Type 1 and Type 2 Infrastructures, for example, Internet Service Providers, domain registrars, and webmail providers.

## Victim

A victim is a target against whom attacks are initiated, vulnerabilities are exploited, or capabilities are used. 
It can be organisations, people, or assets, such as target email or IP addresses, domains, and so on. 

There is always a victim in every cyberattack. For example, the spear-phishing email (a well-crafted email targeting a specific person of interest) was sent to the company, and someone (victim) clicked on the link. In this case, the victim is the selected target of interest for an adversary. 

* Victim Personae are the people and organisations being targeted and whose assets are being attacked and exploited. These can be organisation names, people’s names, industries, job roles, interests, etc.
* Victim Assets are the attack surface and include the set of systems, networks, email addresses, hosts, IP addresses, social networking accounts, etc., to which the adversary will direct their capabilities.

## Centered approaches

The model focuses on several trade-craft concepts of intrusion analysis which are referred to as ‘centered’ approaches. These approaches are centered on a certain feature of the diamond model to detect new malicious activities and expose activities related to the other relevant features. There are six centered approaches: adversary-centered, capability-centered, infrastructure-centered, victim-centered, social-political-centered, and technology centered. The first four focus on the diamond nodes while the remaining two focus on the meta-features of the diamond.

## Meta features

Meta-features are not required, but they can add some valuable information or intelligence to the Diamond Model.

* Timestamp - is the date and time of the event. Each event can be recorded with a date and time that it occurred, such as 2021-09-12 02:10:12.136. The timestamp can include when the event started and stopped. Timestamps are essential to help determine the patterns and group the malicious activity. For example, if the intrusion or breach happened at 3 am in the United States, it might be possible that the attack was carried out from a specific country with a different time zone and standard business hours. 
* Phase - these are the phases of an intrusion, attack, or breach. An example can be the Cyber Kill Chain (CKC) developed by Lockheed Martin. For example, an attacker needs to do some research to discover the target or a victim. Then they would try to exploit the target, establish a command-and-control centre and, lastly, exfiltrate the sensitive information. 
* Result - While the results and post-conditions of an adversary’s operations will not always be known or have a high confidence value when they are known, they are helpful to capture. The event results can be labelled as "success," "failure," or "unknown." The event results can also be related to the CIA (confidentiality, integrity, and availability) triad, such as Confidentiality Compromised, Integrity Compromised, and Availability Compromised. Another approach can also be documenting all the post-conditions resulting from the event, for example, information gathered in the reconnaissance stage or successful passwords/sensitive data exfiltration.
* Direction - This meta-feature helps describe host-based and network-based events and represents the direction of the intrusion attack. The Diamond Model of Intrusion Analysis defines seven potential values for this meta-feature: Victim-to-Infrastructure, Infrastructure-to-Victim, Infrastructure-to-Infrastructure, Adversary-to-Infrastructure, Infrastructure-to-Adversary, Bidirectional or Unknown.
* Methodology - This meta-feature will allow an analyst to describe the general classification of intrusion, for example, phishing, DDoS, breach, port scan, etc. 
* Resources - According to the Diamond Model, every intrusion event needs one or more external resources to be satisfied to succeed. Examples of the resources can include the following: software (e.g., operating systems, virtualisation software, or Metasploit framework), knowledge (e.g., how to use Metasploit to execute the attack and run the exploit), information (e.g., a username/password to masquerade), hardware (e.g., servers, workstations, routers), funds (e.g., money to purchase domains), facilities (e.g., electricity or shelter), access (e.g., a network path from the source host to the victim and vice versa, network access from an Internet Service Provider (ISP)).

## Social political

The social-political component describes the needs and intent of the adversary, for example, financial gain, gaining acceptance in the hacker community, hacktivism, espionage, ... 

The scenario can be that the victim provides a “product”, for example, computing resources & bandwidth as a zombie in a botnet for crypto mining (producing new cryptocurrencies by solving cryptographic equations through the use of computers) purposes, while the adversary consumes their product or gets financial gain. 

## Technology

Technology – the technology meta-feature or component highlights the relationship between the core features: capability and infrastructure. The capability and infrastructure describe how the adversary operates and communicates. 
A scenario can be a watering-hole attack which is a methodology where the adversary compromises legitimate websites that they believe their targeted victims will visit.

|  ![Getting Closer to the Adversary](../../_static/images/starwars-diamond2.png)   |
|:---------------------------------------------------------------------------------:|
| A more realistic, general Diamond Model summarizing a cyber adversary’s activity. |

## Resources

* [What is the Diamond Model of Intrusion Analysis?](https://cyware.com/educational-guides/cyber-threat-intelligence/what-is-the-diamond-model-of-intrusion-analysis-5f02/)
* [A Security Professional’s Guide to the Diamond Model](https://mcsi-library.readthedocs.io/articles/2022/07/a-security-professional-s-guide-to-the-diamond-model/a-security-professional-s-guide-to-the-diamond-model.html)
