# Incident handling (NIST)

The National Institute of Standards and Technology (NIST) developed a framework for incident handling, which is the most commonly used model, also by the EC.

## Preparation

An incident management plan is put in place for detecting an incident in the environment. This involves, for example, identifying different malware attacks and determining what their impact on systems would be. It also involves ensuring that the tools to respond to an incident and the appropriate [security measures are in place to stop an incident from happening in the first place](prevention.md).

* A team must consider how to manage communications, software, hardware, and any other available resources such as port lists and network diagrams.
* Teams must be conscious of frameworks, standards, and the main recommended practices for securing networks and systems.
* Team members should understand a range of common attack vectors, so they can identify attacks through certain types of activity. 

### Communications

Consider contact information (email addresses, phone numbers, on-call information, and public encryption keys), and security information to help verify identities. This needs to be readily available for team members, law enforcement, and other incident response teams.

Best is to also secure incident reporting mechanisms, an issue-tracking system, and smartphones to facilitate out-of-hours offsite and onsite communications. Encryption software can help secure communications with external parties. A so-called "war room" can be used as a base for these communications.

[Standardisation of communication on evidence-based information](standards.md) is also in progress.

### Containment strategies

Decision-making is key to containment and is made easier by following documented procedures for specific types of incidents. NIST advises defining acceptable risks to develop strategies for containment. Strategies can be based on incident types; A few examples of considerations:

* Potential damage to and theft of resources
* Need for evidence preservation
* Service availability (how services provided to clients may be affected)
* Time and resources for strategy implementation
* Strategy effectiveness (partial containment, full containment)
* Solution duration (emergency workarounds to be removed within four hours, temporary workarounds to be removed within two weeks, permanent solutions)

### Hardware and software

Hardware and software to analyse an incident should be installed in advance. This can include a [SIEM stack](siem.md), forensic workstations, backup drives, disk images to preserve log files and incident data, laptops for live analysis and report writing, and packet sniffers to track network activity.

Spare hardware, workstations, laptops, servers, network equipment, and any virtual equivalents, is useful if the primary hardware has been compromised, mainly to restore operations when time permits.

For evidence handling, keep used and blank removable storage media. Store backups of trusted software versions on used storage media, and store evidence ready for further analysis on the blank ones. It is also recommended to have additional evidence gathering accessories, such as notebooks, digital cameras, audio recorders, chain of custody forms, evidence storage bags and tags, and evidence tape. These are useful for legal purposes in particular if evidence is to be used in court proceedings.

### Analysis resources

* Port lists detailing commonly used ports and those associated with specific strains of malware.
* Documentation for operating systems, applications, and protocols.
* Documentation for intrusion detection systems (IDS) antivirus (AV) software.
* Network diagrams and lists of critical assets to identify assets at risk.
* A baseline of activity across all networks, systems, and applications while interpreting incident activity. These can be used to compare with the incident data and check for anomalous behaviour. 
* Hashes of critical files to assess whether they have been modified.

### Mitigation software

Make sure the team has access to clean images of operating systems and applications for restoration purposes. Keeping up-to-date images of applications as backups means they can be easily restored.

## Detection and analysis

Signs (attack vectors) of an incident can be precursors (an incident may occur in the future) and indicators (an incident might have already occurred or might still be happening).

When an incident occurs, the initial analysis has several critical steps that are key to identifying the scope of the incident and determining which systems, networks, and applications have been affected. Things like normal behaviours, system and network profiling, and event correlation can make analysis easier. 

An incident response analyst is responsible for collecting and analysing data to find clues to help identify the source of an attack. In this step, analysts identify the nature of the attack and its impact on systems. Security professionals work with tools and indicators of compromise (IOCs) that have been developed to track the attacked systems.

## Containment, eradication, and recovery

This is the main phase of security incident response, in which the responders take action to stop any further damage. 

For evidence to be admissible in court, it's crucial to document how it was acquired and preserved. All evidence activity should be recorded in a detailed log that includes identifying information, such as the location, hostname, MAC, and IP addresses. This log should also include the names, titles, and contact numbers of each individual who collected or handled the evidence. Timestamps are key to any investigation and should also be logged, particularly when handling evidence. Lastly, the storage location should be logged separately from the location of the identifying information, which refers to where the evidence was collected rather than stored.

### Containment

Containment is essential to prevent further damage and to ensure resources aren't overwhelmed. Containment includes evidence gathering, handling, and identifying the attacking hosts. Actions might be disconnecting systems from networks, quarantining infected systems, or blocking traffic to and from known malicious IP addresses.

### Identifying the attacking hosts

Identifying the attacking hosts can be important, but often detracts from the containment, eradication, and recovery of an incident. It's time consuming and not always possible. A system owner may want to know who caused the incident purely for investigative purposes, but it won't help achieve the main goal of reducing business impact. The most common activities used to identify an attacker are:

* Validating the attacking host's IP address
* Researching the attacking host through open-source intelligence and domain intel
* Using incident databases, which contain incident data and information about attacks
* Monitoring possible attacker communication channels

### Eradication

After containing a security issue, breached accounts need be disabled, and/or malicious code or software needs to be eradicated from the environment. This can involve using antivirus tools or manual removal techniques. It also includes ensuring that all security software is up-to-date in order to prevent any future incidents. Eradication is not always necessary, and is sometimes part of the recovery process.

When eradication crosses over with recovery, administrators might mitigate vulnerabilities that have been exploited.

### Recovery

After eradication, all systems are restored to their pre-incident state. Administrators oversee the restoration of operations, the resumption of normal activity, and confirm everything is functioning adequately. This may involve restoring data from backups, rebuilding infected systems, and re-enabling disabled accounts. 

Eradication and recovery are often done in a phased approach that prioritises remediation steps, so the threat can not become active again.

In general, it is best practice to focus on the critical security issues, and sometimes it is a good idea to implement temporary infrastructure changes that are refined later.

## Post-incident activity

The final phase of the incident response life cycle is to perform a postmortem of the entire incident: What lessons have been learned to improve incident security protocols and make security strategies more robust and effective. The incident data and any evidence that has been recorded or documented is also collected. If a court case is opened, these become important.

## Resources

* [Computer security incident handling guide (Special Publication 800-61, Revision 2, pdf)](https://nvlpubs.nist.gov/nistpubs/specialpublications/nist.sp.800-61r2.pdf), Cichonski, P., Millar, T., Grance, T.., & Scarfone, K., 2012, National Institute of Standards & Technology
* [NIST incident response plan: Building your own IR process based on NIST guidelines](https://www.cynet.com/incident-response/nist-incident-response/), Cynet, 2022, Incident Response
* [Three ways to improve your security incident response plan](https://www.himss.org/resources/three-ways-improve-your-security-incident-response-plan), HIMSS, 2022, Cybersecurity and Privacy Resource Center
* [Microsoft security incident management](https://learn.microsoft.com/en-us/compliance/assurance/assurance-security-incident-management), Mazzoli, R., Gluck, D., 2021, Risk Assessment Guide for Microsoft Cloud
