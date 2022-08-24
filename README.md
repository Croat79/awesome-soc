# Awesome SOC
A collection of sources of documentation, and field best practices, to build/run a SOC.

Those are my view, based on my own experience as SOC/CERT analyst and team manager, as well as well-known papers. 

NB: Generally speaking, SOC here refers to detection activity, and CERT/CSIRT to incident response activity.

# Basic concepts:

## What is a SOC? 
As per MITRE paper (SOC strategies, see [below](https://github.com/cyb3rxp/awesome-soc/blob/main/README.md#for-a-soc)):
![image](https://user-images.githubusercontent.com/16035152/186421761-ff5bab84-5982-43e1-8d0c-fa9406422b2c.png)

## SOC/CERT incident response lifecycle (detection // incident response):
As per NIST SP800-61 rev2 paper (see [below](https://github.com/cyb3rxp/awesome-soc/blob/main/README.md#for-a-soc)):
![image](https://user-images.githubusercontent.com/16035152/186421468-5136db5b-55d4-4841-9a4a-7d03904af81e.png)

As an IT security teacher used to tell his students, like a SOC motto: "Without response, detection is useless" (Freely inspired from Bruce Schneier, [Secrets and Lies: Digital Security in a Networked World](https://www.amazon.fr/Secrets-Lies-Digital-Security-Networked/dp/1119092434) book).

## SOC mission and context:
As per MITRE paper (see [below](https://github.com/cyb3rxp/awesome-soc/blob/main/README.md#for-a-soc)):
![image](https://user-images.githubusercontent.com/16035152/186420020-8507b3b3-7fb8-46cf-a5f9-9d6506284cb2.png)


# Must read

## For a SOC:
* NIST, [Cybersecurity framework](https://www.nist.gov/cyberframework) 
* FIRST, [Building a SOC](https://www.first.org/resources/guides/Factsheet_Building_a_SOC_start_small.pdf) 
* NIST, [SP800-61 rev2, incident handling guide](https://csrc.nist.gov/publications/detail/sp/800-61/rev-2/final) 
* MITRE, [11 strategies for a world-class SOC](https://www.mitre.org/publications/technical-papers/11-strategies-world-class-cybersecurity-operations-center), part 0 (Fundamentals) 

## For a CERT: 
* FIRST, [CERT-in-a-box](https://www.first.org/resources/guides/cert-in-a-box.zip) 
* ENISA, [Good practice for incident management](https://www.enisa.europa.eu/publications/good-practice-guide-for-incident-management)
* NIST, [SP800-86, integration forensics techniques into IR](https://nvlpubs.nist.gov/nistpubs/legacy/sp/nistspecialpublication800-86.pdf) 

## Globally (SOC and CERT):
* ThreatConnect, [SIRP / SOA / TIP benefits](https://threatconnect.com/blog/realizing-the-benefits-of-security-orchestration-automation-and-response-soar/) 
* Orange Cyberdefense, [Feedback regarding experience with SOAR in 2020 (in French)](https://www.orangecyberdefense.com/fr/insights/blog/threat-management/soar-quelles-conclusions-en-2020) 
* Lutessa, [Red/blue/purple teams’ roles](https://www.lutessa.com/wp-content/uploads/2020/09/red-team-purple-team-blue-team.png)  (https://www.lutessa.com/?p=5524)




# Critical means (tools/sensors)

## Critical tools for a SOC/CERT:
* **[SIEM](https://www.gartner.com/en/information-technology/glossary/security-information-and-event-management-siem)**
   * See [Gartner magic quadrant](https://www.bankinfosecurity.com/whitepapers/2021-gartner-magic-quadrant-for-security-information-event-w-8758) 
   * My recommendation: [Splunk](www.splunk.com), [Elastic](https://www.elastic.co/)
* **[SIRP](https://d3security.com/blog/whats-the-difference-between-soar-and-sao/)**
  * e.g.: [IBM Resilient](https://www.ibm.com/qradar/security-qradar-soar?utm_content=SRCWW&p1=Search&p4=43700068028974608&p5=e&gclid=Cj0KCQjw9ZGYBhCEARIsAEUXITW2yUqAfNqWNeYXyENeUAoqLxV543LT0n2oYhYxEQ47Yjm7NfYTFHAaAtwpEALw_wcB&gclsrc=aw.ds),  [TheHive](https://thehive-project.org/), [SwimLane](https://swimlane.com/), [PAN Cortex XSOAR](https://www.paloaltonetworks.com/cortex/cortex-xsoar)
* **[SOA](https://d3security.com/blog/whats-the-difference-between-soar-and-sao/)**
  * My recommendation: [IBM Resilient]( https://www.ibm.com/qradar/security-qradar-soar?utm_content=SRCWW&p1=Search&p4=43700068028974608&p5=e&gclid=Cj0KCQjw9ZGYBhCEARIsAEUXITW2yUqAfNqWNeYXyENeUAoqLxV543LT0n2oYhYxEQ47Yjm7NfYTFHAaAtwpEALw_wcB&gclsrc=aw.ds), [SwimLane](https://swimlane.com/), [TheHive](https://thehive-project.org/), [PAN Cortex XSOAR](https://www.paloaltonetworks.com/cortex/cortex-xsoar)
* **[TIP](https://www.ssi.gouv.fr/en/actualite/opencti-the-open-source-solution-for-processing-and-sharing-threat-intelligence-knowledge/)**
  * My recommendation: [MISP](https://www.misp-project.org/), [OpenCTI](https://www.filigran.io/en/products/opencti/), [Sekoia.io](https://www.sekoia.io/fr/produire-et-personnaliser-votre-propre-intelligence/), [ThreatQuotient](https://www.threatq.com/)
  * don't forget the needed feeds (community / paid ones)
     * My recommendation for paid ones: [ESET](https://www.eset.com/us/business/services/threat-intelligence/), [Sekoia.io](https://www.sekoia.io/fr/sekoia-io-cti/), [Mandiant](https://www.mandiant.com/advantage/threat-intelligence/subscribe), [RecordedFuture](https://www.recordedfuture.com/platform/threat-intelligence)...
     * My recommendation for community ones: MISP default feeds list, [ISAC](https://www.enisa.europa.eu/publications/information-sharing-and-analysis-center-isacs-cooperative-models), [OTX](https://otx.alienvault.com/api), the [Covert.io list](http://www.covert.io/threat-intelligence/).
     

## Critical sensors for a SOC:

* **Antimalware**
  * See [Gartner magic quadrant](https://www.threatscape.com/microsoft-security-named-leader-in-4-gartner-magic-quadrants/) 
  * My recommendation: Microsoft Defender, BitDefender, ESET Nod32.
* **[Endpoint Detection and Response](https://www.gartner.com/reviews/market/endpoint-detection-and-response-solutions)** 
  * see [Gartner magic quadrant](https://www.microsoft.com/security/blog/uploads/securityprod/2022/01/Gartner-EIA-1963x2048.png) 
  * My recommendation: SentinelOne, Microsoft Defender for Endpoint, Harfanglab.
* **[Secure Email Gateway](https://www.gartner.com/reviews/market/email-security)**
  * My recommendation: [Microsoft Defender for Office365](https://www.microsoft.com/en-us/security/business/siem-and-xdr/microsoft-defender-office-365), [ProofPoint](https://www.proofpoint.com/fr/threat-reference/email-gateway), [Mimecast](https://www.mimecast.com/products/email-security/secure-email-gateway/)
* **[Secure Weg Gateway](https://www.gartner.com/en/information-technology/glossary/secure-web-gateway)** / Security Service Edge 
  * see [Gartner magic quadrant](https://www.zscaler.fr/cdn-cgi/image/format%3Dauto/sites/default/files/images/page/gartner-magic-quadrant-security-service-edge-sse-2022/zscaler-gartner-sse-2022-%401x.png) 
  * My recommendation: BLueCoat, CISCO, Zscaler
* **AD security** (audit logs, or specific security monitoring solutions)
  * My recommendation: [Semperis](https://www.purple-knight.com/fr/?utm_source=gads&utm_medium=paidsearch&utm_campaign=pk_emea&gclid=Cj0KCQjw9ZGYBhCEARIsAEUXITV3yX7Nn6_GR-YVwiOANFvS9wsEQdTyUGHvMMirMzNQEoQ1Q3EQYIMaAjTgEALw_wcB) or [PingCastle](https://www.pingcastle.com/download/)
* [Cloud Access Security Broker](https://www.gartner.com/en/information-technology/glossary/cloud-access-security-brokers-casbs), if company's IT environment uses a lot of external services like SaaS/IaaS:
   * See [Gartner magic quadrant](https://www.netskope.com/wp-content/uploads/2021/01/Screen-Shot-2021-01-05-at-10.15.23-AM-1024x456.png)
   * My recommendation: Microsoft, Zscaler, Netskope.


## Critical tools for CERT:
* On-demand sandbox:
  * My recommendation: [Joe's sandbox](https://www.joesandbox.com/#windows), [Hybrid Analysis](https://www.hybrid-analysis.com/), etc.
* Forensics and reverse-engineering tools suite
  * My recommendation: [SIFT Workstation](https://www.sans.org/tools/sift-workstation/), or [Tsurugi](https://tsurugi-linux.org/)
  * My recommendation: for reverse engineering, [FireEye Flare-VM](https://github.com/mandiant/flare-vm)
* Incident tracker: 
  * My recommendation: [Timesketch](https://timesketch.org/), [GitLab](https://about.gitlab.com/handbook/engineering/security/security-operations/sirt/sec-incident-response.html)
* Scanners:
  * IOC scanners:
    * My recommendation: [Loki](https://github.com/Neo23x0/Loki)
  * Offline antimalware scanners: 
    * My recommendation: [Windows Defender Offline](https://support.microsoft.com/en-us/windows/help-protect-my-pc-with-microsoft-defender-offline-9306d528-64bf-4668-5b80-ff533f183d6c)
    

# IT/security Watch (recommended sources)

* [Sigma HQ (detection rules)](https://github.com/SigmaHQ/sigma/tree/master/rules) 
* [Splunk Security content (free detection rules for Splunk)](https://research.splunk.com/) 
* [Awesome Threat Intelligence](https://github.com/hslatman/awesome-threat-intelligence) 
* LinkedIn / Twitter:
  * e.g.: [LinkedIn Information Security Community group](https://www.linkedin.com/groups/38412/) 
* RSS reader/portal:
  * e.g.: [Netvibes](https://www.netvibes.com/phvialle?page=phvialle#Security)  
* Government CERT, industry sector related CERT...
  * e.g.: [CERT-FR](https://www.cert.ssi.gouv.fr/avis/), [CERT-US](https://www.cisa.gov/uscert/ncas/alerts)
* other interesting websites:
  * e.g.: [ISC](https://isc.sans.edu/), [ENISA](https://www.enisa.europa.eu/publications), [ThreatPost](https://threatpost.com/) ...


# Management

## SOC HR and organization:
* no real need for tiering (L1/L2/L3)
  * this is an old model for service provider, not necesseraly for a SOC!
  * as per MITRE paper (p65):
  ![image](https://user-images.githubusercontent.com/16035152/186418647-c2d30648-fe83-4065-a68c-2db652e21c40.png)

* 3 different teams should be needed:
  * security monitoring team (which does actually the "job" of detecting security incident being fully autonomous)
  * security monitoring engineering team (which fixes/improves security monitoring, like SIEM rules and SOA playbooks)
  * build / project management team (which does tools deployment, SIEM data ingestion, and secific DevOps tasks).

## CERT HR and organization:
* designate among team analysts: 
  * triage officer;
  * incident handler;
  * incident manager;
  * deputy CERT manager.
* Generally speaking, follow best practices as described in ENISA's paper ("Good practice for incident management", see "Must read" section above)

## TTP (attack methods) knowledge base reference:
* Use [MITRE ATT&CK](https://attack.mitre.org/matrices/enterprise/)
* Document all detections (SIEM Rules, etc.) using MITRE ATT&CK ID, whenever possible.

## Data quality and management:
* implement an information model, like the [Splunk CIM one](https://docs.splunk.com/Documentation/CIM/5.0.1/User/Overview)
  * do not hesitate to extend it, depending on your needs
  * make sure this datamodel is being implemented in the SIEM, SIRP, SOA and even TIP.

## Detection quality controls: 
 * **Run regular [purpleteaming sessions](https://about.gitlab.com/handbook/engineering/security/threat-management/red-team/purple-teaming/)** in time!!
   * e.g.: [Intrinsec](https://www.intrinsec.com/purple-team/), [FireEye](https://www.fireeye.fr/content/dam/fireeye-www/regional/fr_FR/services/pdfs/ds-purple-team-assessment.pdf)


## Detection capabilities representation standard:
*	Use [Security Stack Mappings](https://github.com/center-for-threat-informed-defense/security-stack-mappings) to picture detection capabilities for a given security solution/environment (like AWS, Azure, NDR, etc.): 

## SOC detection capabilities **simplified** representation:
 * Generate [ATT&CK heatmaps](https://www.signalblur.io/getting-started-with-mitres-att-ck-navigator/), to picture the SOC detection capabilities

## SOC Self-assessment:
*	[SOC Cyber maturity model](https://www.soc-cmm.com/introduction/) 
*	[SOC-CMM self-assessment tool](https://www.soc-cmm.com/downloads/latest/) 

## CERT/CSIRT self-assessment:
* ENISA, [OpenCSIRT cybersecurity maturity framework](https://www.enisa.europa.eu/topics/csirts-in-europe/csirt-capabilities/csirt-maturity/)  
  * OpenCSIRT, [SIM3 self-assessment](https://sim3-check.opencsirt.org/#/v1/) 
* CMM, [SOC-CMM 4CERT](https://www.soc-cmm.com/4CERT/) 
  * [SOC-CMM 4CERT self-assessment tool](https://www.soc-cmm.com/downloads/latest/soc-cmm%20for%20CERT%201.0%20-%20advanced.xlsx)
  
## Reporting:
* Generate metrics, leveraging the SIRP capabilities to do so:
  * detection rules triggering most false positives
  * detection rules taking the longest to be handled
  * number of false positives
  * number of detection rules which detection capability and handling process have been confirmed with purpleteaming session, so far
  * most seen TTP in detection
  * most common incident types
  * mean time to verify (confirm) the alerts
  * mean time to handle (verify and be ready for incident response) the alerts  

# IT achitecture

Implement SOC enclaves, as per MITRE paper:
![image](https://user-images.githubusercontent.com/16035152/186420265-4c0275b2-d70e-4fec-936c-712c1c4802a8.png)



# To go further

## Must read:
* MITRE, [11 strategies for a world-class SOC (remaining of PDF)](https://www.mitre.org/publications/technical-papers/11-strategies-world-class-cybersecurity-operations-center) 
*	Microsoft, [SOC/IR hierarchy of needs](https://github.com/swannman/ircapabilities) 
* CISA, [Cyber Defense Incident Responder role](https://www.cisa.gov/cyber-defense-incident-responder)
* Betaalvereniging, [TahiTI (threat huting methdology)](https://www.betaalvereniging.nl/wp-content/uploads/TaHiTI-Threat-Hunting-Methodology-whitepaper.pdf) 
* GMU, [Improving Social Maturity of Cybersecurity Incident Response Teams](https://edu.anarcho-copy.org/Against%20Security%20-%20Self%20Security/GMU_Cybersecurity_Incident_Response_Team_social_maturity_handbook.pdf)
* FireEye, [Purple Team Assessment](https://www.fireeye.fr/content/dam/fireeye-www/regional/fr_FR/services/pdfs/ds-purple-team-assessment.pdf)
* FIRST, [CVSS v3.1 specs](https://www.first.org/cvss/specification-document) 

## Nice to read:
* NIST, [SP800-53 rev5 (Security and Privacy Controls for Information Systems and Organizations)](https://csrc.nist.gov/publications/detail/sp/800-53/rev-5/final)
* Amazon,	[AWS Security Fundamentals](https://aws.amazon.com/fr/training/digital/aws-security-fundamentals/)   
* Microsoft, [PAW Microsoft](https://docs.microsoft.com/en-us/security/compass/privileged-access-devices) 
* CIS, [Business Impact Assessment](https://bia.cisecurity.org/) 
* Abdessabour Boukari, [RACI template (in French)](https://github.com/cyberabdou/SOC/blob/77f01ba82c22cb11028cde4a862ae0bea4258378/SOC%20RACI.xlsx) 
* Trellix, [XDR Gartner market guide](https://www.trellix.com/fr-fr/solutions/gartner-report-market-guide-xdr.html)
* [Awesome Security Resources](https://github.com/Johnson90512/Awesome-Security-Resources)
* [Incident Response & Computer Forensics, 3rd ed](https://www.google.fr/books/edition/Incident_Response_Computer_Forensics_Thi/LuWINQEACAAJ?hl=fr)


## SOC sensors, nice to have:
* Asset Security Monitoring / Attack Surface Management:
  * My recommendation: [Intrinsec (in French)](https://www.intrinsec.com/monitoring-cyber/), [Mandiant](https://www.mandiant.fr/advantage/attack-surface-management)
* Honeypot
  * My recommendation: [Canary.tools](https://canary.tools/)
* NDR:
  * My recommendation: [Gatewatcher](https://www.gatewatcher.com/en/our-solutions/trackwatch/)
* MDM:
  * My recommendation: [Microsoft Intune](https://docs.microsoft.com/en-us/mem/intune/fundamentals/what-is-intune)
* DLP:
  * See [Gartner reviews and ratings](https://www.gartner.com/reviews/market/data-loss-prevention)
* Network TAP.


# Special thanks
Clément G., Alexandre C., Jean B., Frédérique B., Pierre d'H., Hamdi C., Fabien L., Gilles B., Olivier R., Jean-François L., Fabrice M., Pascal R., Florian S., Maxime P., Pascal L., Jérémy d'A., Olivier C. x2, David G., Guillaume D., Patrick C., Lesley K., Gérald G., Jean-Baptiste V., Antoine C.
