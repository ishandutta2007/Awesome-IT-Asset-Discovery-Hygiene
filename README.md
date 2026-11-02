# Awesome-IT-Asset-Discovery-Hygiene

## Top IT Asset Discovery & Hygiene Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**  

*Focused on Agentless Discovery, Asset Reconciliation & Self-Hosted CMDB Platforms*  

**Last updated: November 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **IT Asset Discovery & Hygiene**. These tools enable organizations to continuously discover every device, application, and identity across their environment—then reconcile that data to eliminate blind spots, track agent coverage, and maintain an accurate, audit-ready inventory.



**Examples** include CrowdStrike Falcon Discover, Axonius, Tanium Asset, Armis, Lansweeper, Qualys CSAM, runZero, Sevco Security, Device42, and Microsoft Defender Device Inventory (the category leaders).



**Open-source emphasis**: IT Asset Discovery & Hygiene is a domain where open-source tooling is **fragmented across distinct discovery philosophies but genuinely capable for specific layers**. **Wazuh's IT Hygiene module** is the most notable new entrant—introduced in v4.13.0, it provides a centralized dashboard for endpoint inventory including hardware specs, installed packages, running processes, open ports, user accounts, and **browser extensions**, all queryable across the fleet . **NetAlertX** offers continuous network visibility with a centralized source of truth for connected devices, detecting unauthorized hardware and Shadow IT . For traditional CMDB foundations, **OCS Inventory NG** provides agent-based inventory across Windows, Linux, macOS, and Android with network discovery for agentless devices . The critical caveat: **no open-source project replicates the cross-source reconciliation and normalization** of Axonius or Sevco—those platforms aggregate data from 1,000+ sources, deduplicate conflicting records, and build a unified asset graph .



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-products)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[CrowdStrike Falcon Discover](https://www.crowdstrike.com/)**  

  IT hygiene and asset discovery within the Falcon platform; identifies unmanaged devices, tracks agent coverage, and reconciles inventory with ServiceNow CMDB for enriched context . **Best for CrowdStrike customers** wanting unified endpoint visibility and hygiene checks.



- **[Axonius](https://www.axonius.com/)**  

  Cyber asset attack surface management platform integrating **1,000+ sources** into a single normalized asset model; covers cyber assets, exposures, software, SaaS, identities, and IoT/OT/IoMT . **Best for organizations wanting comprehensive cross-source reconciliation**—the benchmark for CAASM.



- **[Tanium Asset](https://www.tanium.com/)**  

  Real-time endpoint discovery and inventory without pre-ingestion; finds every managed and unmanaged endpoint across cloud, on-prem, and hybrid environments, providing high-fidelity data to CMDB and SIEM systems . **Best for large fleets** needing instant interrogation at scale.



- **[Armis](https://www.armis.com/)**  

  Agentless cyber exposure management powered by the **Asset Intelligence Engine**—a cloud-based device security data lake tracking billions of assets in real time for classification and threat detection . **Best for agentless visibility** across IT, IoT, IoMT, OT, and cloud.



- **[Lansweeper](https://www.lansweeper.com/)**  

  Automated hardware discovery across IT, OT, cloud, and remote environments using combined agent-based and agentless, active and passive methods; tracks lifecycle from procurement to retirement with NIST/ISO 19770/GDPR audit readiness .



- **[Qualys CSAM](https://www.qualys.com/)**  

  CyberSecurity Asset Management with external attack surface management (EASM), automatic tagging for third-party assets, IPv6 support, and business context grouping . **Best for Qualys VMDR customers** wanting unified internal and external asset visibility.



- **[runZero](https://www.runzero.com/)**  

  Network discovery and asset inventory with **continuous scanning** options; supports performance tuning for large networks (scan speed, max group size, subnet sampling) and structured tagging per site for overlapping IP ranges . **Best for large, distributed networks** needing active discovery control.



- **[Sevco Security](https://www.sevcosecurity.com/)**  

  Asset intelligence platform with **Asset Graph** that continuously deduplicates and correlates data from endpoints, cloud, identity, and vulnerability scanners; claims **40% of assets are typically missing from inventory** . **Best for closing inventory blind spots** through multi-source reconciliation.



- **[Device42](https://www.device42.com/)**  

  Hybrid cloud CMDB with agentless discovery and dependency mapping; pre-configured CMDB eliminates CI design, with visualizations and a deep integration library .



- **[Microsoft Defender Device Inventory](https://learn.microsoft.com/)**  

  Authoritative source for all devices visible to Defender for Endpoint, including onboarded and discovered devices; tabs for Computers & mobile, Network devices, IoT/OT, and Uncategorized . **Best for Microsoft Defender customers** wanting unified device visibility.



## Open-Source GitHub Projects



### Endpoint IT Hygiene (Wazuh)



- **[Wazuh IT Hygiene](https://github.com/wazuh/wazuh)**  

  Wazuh v4.13.0 introduced a dedicated **IT Hygiene capability** (GPLv2) providing a centralized dashboard for endpoint inventory . Features: **hardware specs** (CPU, memory, storage), **OS details**, **installed packages and versions**, **running processes and services**, **network configurations and open ports**, **user accounts and group memberships**, and **browser extensions with permissions** . **Practical use cases**: patch management (identify endpoints running vulnerable package versions), browser extension auditing (detect high-risk extensions with excessive permissions), and dormant account detection (filter accounts by last login dates and shell access) . **Best for Wazuh users** wanting inventory visibility alongside SIEM/XDR capabilities—but it is endpoint-focused, not network discovery.



### Network Discovery & Visibility (NetAlertX)



- **[NetAlertX](https://github.com/netalertx/NetAlertX)**  

  Open-source **network visibility and asset intelligence framework** (Python) providing a centralized source of truth for network infrastructure . Features: **continuous monitoring** for unauthorized asset discovery, connection state changes, and IPAM drift; **multiple scan methods** including arp-scan, Pi-hole DB import, DHCP lease imports, UNIFI controller, and SNMP router import; **80+ notification gateways**; **workflows module** for automated device categorization and cleanup policies; and **RBAC via reverse proxy** integration . **Best for local network visibility** with automated governance—but it is network-scoped, not a full CMDB.



### Traditional CMDB & Inventory (OCS Inventory NG)



- **[OCS Inventory NG](https://github.com/OCSInventory-NG)**  

  Open-source **IT asset inventory and software deployment** tool (GPL v2) . Architecture: **agents** on Windows, Linux, macOS, BSD, and Android report hardware and software data to a central server; **network discovery** finds devices that cannot run an agent; **software deployment** packages; **web console and REST API** . **Sovereignty**: French-developed, self-hosted with no vendor cloud service—EU data residency and full source auditability . **Best for organizations wanting a proven, self-hosted inventory foundation**—but it is agent-heavy and lacks the modern UX of commercial tools.



### Additional Strong Open-Source Options



- **Cloudlist** — Open-source multi-cloud asset enumeration tool (ProjectDiscovery) for blue teams; centralizes inventory across cloud providers with minimal configuration and multiple output formats . **Best for cloud asset discovery** across AWS, Azure, GCP—not on-premises or endpoint discovery.

- **TWIGS** — Open-source Python CLI for **agentless attack surface discovery** (ThreatWorx); discovers code, containers, cloud, servers, and network devices without storing credentials on the platform . **Best for zero-trust discovery** where credential sharing is a concern—but it is a CLI, not a managed platform.



**Frameworks for building custom systems**: For **endpoint inventory alongside SIEM**, Wazuh IT Hygiene provides the most integrated open-source option . For **network visibility and Shadow IT detection**, NetAlertX . For **traditional agent-based CMDB**, OCS Inventory NG . For **cloud asset enumeration**, Cloudlist . **No open-source project replicates the cross-source reconciliation** of Axonius (1,000+ sources) or Sevco (asset graph deduplication)—those are commercial CAASM advantages .



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- IT asset discovery platforms handling infrastructure data must comply with organizational security policies and privacy regulations; **self-hosted solutions place full responsibility for scan authorization, credential management, and data accuracy on the operator**.

- **Open-source asset discovery is fragmented by layer**—Wazuh provides endpoint inventory , NetAlertX provides network visibility , and OCS Inventory provides traditional CMDB . However, **no open-source project matches the cross-source reconciliation and unified asset graph** of Axonius or Sevco . Choose based on whether you need endpoint hygiene (Wazuh), network discovery (NetAlertX), or CMDB inventory (OCS).

- Verify license terms for commercial use; Wazuh uses GPLv2, NetAlertX is open-source (check repository), and OCS Inventory NG uses GPL v2 .



---



**Made for IT asset managers, security engineers, and organizations building asset visibility and hygiene capabilities.**  

Let's make asset discovery and hygiene more open, but with clear eyes about the cross-source reconciliation gap that commercial CAASM platforms still fill.
