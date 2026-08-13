# Product-to-Pain Mapping — Cybersecurity Products and CISO Pain Points

This file is a reference for the `/ciso-outreach` skill. Read it before completing Section 7 (Product-to-Pain Mapping) of the intelligence report.

---

## How to Use This File

1. Identify the product or service the user is selling
2. Find the closest match below
3. Map the CISO's specific situation (industry, company size, signals found) to the pain column
4. Use that specific pain — not a generic version of it — in every piece of outreach copy

The rule: pitch the outcome, not the product. CISOs do not buy features. They buy risk reduction, compliance coverage, and operational efficiency.

---

## Product Categories and Pain Mapping

---

### Penetration Testing / Red Team Services

**What it is:** Third-party security testing — network pen test, web app pen test, social engineering, red team exercises, purple team.

**Who buys it:**
- CISO (approves budget)
- Head of AppSec or VP Security Engineering (sponsors and runs it)
- Compliance Officer (if compliance-driven)

**The real pain:**
- "We need to prove to auditors / the board / our insurance carrier that we've tested our defenses"
- "We had a breach and need to know how bad the exposure was"
- "We're going through SOC 2 / ISO 27001 / CMMC / PCI certification and need pen test evidence"
- "Our internal team doesn't have the bandwidth or objectivity to test themselves"
- "We have a new CISO who wants to know the real state of security before committing to a roadmap"

**Best pitch angle by trigger:**
- Compliance deadline: "Your [SOC 2 / PCI / CMMC] audit is coming up — we help [industry] security teams generate the pen test evidence auditors need, without slowing down the certification timeline."
- New CISO: "A lot of new CISOs we work with want an independent baseline before they commit to a security roadmap. That's usually where we come in."
- Recent breach in sector: "After the [company X] incident, a few [industry] CISOs asked us to run a targeted test specifically on [attack vector used]."
- No prior testing: "Job postings for your AppSec team listed several tools — but we haven't seen evidence of formal third-party testing. Happy to share what that usually surfaces."

**Proof points to look for:**
- Compliance cert timeline (audit deadlines = procurement urgency)
- Open AppSec job posting mentioning pen testing or red team experience
- No public evidence of prior third-party testing

**What to avoid saying:**
- "Identify vulnerabilities before hackers do" — every pen test vendor says this
- "Comprehensive assessment" — meaningless
- Don't lead with methodology unless the target is a technical CISO who asked

---

### CNAPP / CWPP / CSPM (Cloud Security)

**What it is:** Cloud Native Application Protection Platform — protects cloud workloads, detects misconfigurations, manages cloud risk across AWS / Azure / GCP.

**Alternate names:** CloudGuard (Check Point), Prisma Cloud (Palo Alto), Defender for Cloud (Microsoft), Orca Security, Wiz.

**Who buys it:**
- CISO (owns cloud security posture)
- VP Engineering or CTO (at cloud-native companies — they control the platform)
- Head of Cloud Security or Cloud Architect

**The real pain:**
- "We moved to the cloud fast and we don't know what's exposed"
- "We have S3 buckets / storage / databases misconfigured — we just don't know which ones"
- "The security team can't keep up with what the engineering team is deploying"
- "We're drowning in alerts and most of them are noise"
- "We failed a cloud security audit and need to fix it fast"

**Best pitch angle by trigger:**
- Cloud migration in progress: "Most companies that move to [AWS/Azure/GCP] fast find out 6 months later what was left exposed during the migration. We help security teams see that before an auditor or an attacker does."
- Job posting for Cloud Security Engineer: "You're hiring for cloud security — which usually means the team has identified the gap but doesn't have capacity to close it yet. Happy to share how [peer company] covered that gap while the hire came onboard."
- Recent cloud breach in sector: "After the [incident], three [industry] CISOs called us specifically about cloud misconfiguration exposure. Happy to show you what they found."
- Compliance: "[SOC 2 / FedRAMP / HIPAA] requires continuous cloud monitoring. Most teams are doing this manually today — we can automate the evidence generation."

**What to avoid saying:**
- "Single pane of glass" — overused
- "Full visibility" — every vendor says this
- Don't pitch to a technical CISO without knowing which cloud they use

---

### SASE / Zero Trust Network Access (ZTNA)

**What it is:** Secure Access Service Edge — replaces VPN and network perimeter security with identity-based, cloud-delivered access control. Covers SD-WAN, SWG, CASB, FWaaS, and ZTNA in one platform.

**Alternate names:** Harmony Connect (Check Point), Zscaler ZIA/ZPA, Netskope, Cloudflare One, Prisma Access (Palo Alto).

**Who buys it:**
- CISO (owns the zero trust roadmap)
- VP of IT or Chief Infrastructure Officer (network team)
- CTO (at mid-market companies)

**The real pain:**
- "We killed the perimeter with remote work and our VPN is a liability"
- "Our network team is managing 50 different appliances and we can't scale it"
- "We're moving to the cloud and our network security architecture is 2014"
- "Zero trust is on my roadmap but I don't know where to start"
- "Our VPN is slow, our users hate it, and IT can't keep up with access requests"

**Best pitch angle by trigger:**
- Remote/hybrid workforce: "Most security teams we talk to are still running VPN for remote access and are aware it's a problem — but haven't had the forcing function to replace it yet. What's held you back?"
- Zero trust mentioned in their posts or talks: "Saw your talk at [conference] on zero trust architecture — specifically your point on [topic]. Happy to share how [peer company] solved the [specific part they mentioned]."
- Cloud migration: "The move to [AWS/Azure] usually surfaces the VPN problem because the appliances can't handle split tunneling well. We see this a lot in [their industry]. Worth 20 minutes?"

**What to avoid saying:**
- "Zero trust journey" — everyone says this
- Don't pitch SASE without knowing if they're cloud-first or still on-prem heavy

---

### Email Security / Business Email Compromise (BEC) Protection

**What it is:** Advanced email security — catches phishing, BEC, account takeover, impersonation, malicious attachments beyond what Microsoft / Google native security catches.

**Alternate names:** Harmony Email (Check Point), Proofpoint, Mimecast, Abnormal Security, Tessian.

**Who buys it:**
- CISO
- Head of Security Operations / SOC Manager
- IT Director (at smaller companies)

**The real pain:**
- "Our existing email security misses targeted phishing — we've had incidents"
- "We're an M365 shop and the native security isn't catching sophisticated BEC attacks"
- "Finance team wired $X because an attacker spoofed the CFO's email"
- "SOC team is spending half their day triaging email alerts manually"

**Best pitch angle by trigger:**
- Finance or executive impersonation attack (sector news): "BEC attacks against [healthcare / financial / manufacturing] companies are up — specifically CFO impersonation. Happy to share what [peer company] caught that their M365 native security missed."
- SOC headcount constraint: "A lot of security teams we work with are paying analysts to triage email alerts manually. We help eliminate that queue. Worth 20 minutes to show you the difference?"

---

### Endpoint Detection and Response (EDR) / XDR

**What it is:** Endpoint and extended detection — monitors and responds to threats on laptops, servers, and cloud workloads in real time.

**Alternate names:** Harmony Endpoint (Check Point), CrowdStrike Falcon, SentinelOne, Microsoft Defender for Endpoint, Palo Alto Cortex XDR.

**Who buys it:**
- CISO
- Head of Security Operations
- SOC Manager

**The real pain:**
- "We had a ransomware incident and our AV didn't catch it"
- "We're running legacy AV and know we need to modernize"
- "Our SOC is overwhelmed with alerts from endpoint and can't triage fast enough"
- "We can't see what's happening on our endpoints — we're flying blind"

**Best pitch angle by trigger:**
- Ransomware in their sector: "Ransomware hit [number] [industry] companies last quarter — most of them had traditional AV in place. Happy to share what the gap was."
- Legacy AV replacement: "Job posting for a Security Engineer mentions [legacy tool] — if you're evaluating modernizing that stack, worth a conversation."

---

### Network Security / NGFW (Next-Gen Firewall)

**What it is:** Network perimeter security — next-gen firewall, IPS, threat prevention, network segmentation.

**Alternate names:** Check Point NGFW, Palo Alto Networks, Fortinet FortiGate, Cisco Firepower.

**Who buys it:**
- CISO
- VP of IT / Network Security Manager
- CTO (at smaller companies)

**The real pain:**
- "We're still running legacy firewalls that don't understand application context"
- "Our network team can't keep up with the rule set — it's become a compliance liability"
- "We need to segment our network for HIPAA / PCI compliance but don't have the visibility"
- "We had a lateral movement incident and the firewall didn't stop it"

**Best pitch angle by trigger:**
- Compliance: "PCI / HIPAA / CMMC requires network segmentation and logging. Most organizations running legacy firewalls are failing those audits. Happy to share what the audit prep looks like."
- Lateral movement incident in sector: "The [incident] last quarter moved laterally because the firewall wasn't catching east-west traffic. We see this frequently in [industry]. Worth 20 minutes?"

---

### SOC / MDR / MSSP Services (Managed Security)

**What it is:** Managed Detection and Response — a third-party security operations team that monitors, detects, and responds to threats 24/7 on behalf of the client.

**Who buys it:**
- CISO
- CTO (at mid-market companies without a dedicated CISO)
- IT Director

**The real pain:**
- "We can't staff a 24/7 SOC internally"
- "We had an incident after hours and had no one watching"
- "We need to show the board and our insurance carrier we have round-the-clock monitoring"
- "We're spending more than we should building a SOC when it's not our core business"

**Best pitch angle by trigger:**
- After-hours incident: "Most incidents happen on weekends and holidays — when internal teams aren't watching. Happy to share how [peer company] covered that gap without building a full internal SOC."
- Cyber insurance requirement: "Insurers are now requiring 24/7 monitoring as a condition for coverage. We help [industry] organizations meet that requirement without the headcount."

---

## Mapping to Company Size

Adjust the pitch based on company size and security team maturity.

**Under 500 employees / no dedicated CISO:**
- Security is shared with IT or the CTO. Pitch efficiency, not complexity.
- They need managed services or simple-to-deploy solutions.
- Price sensitivity is real. Lead with ROI or cost avoidance.
- Compliance requirements (SOC 2, PCI, HIPAA) are often the primary driver.

**500–5,000 employees / CISO with small team (1–10 people):**
- This is the highest-value segment for most enterprise cybersecurity products.
- They have budget but not people. Anything that reduces manual work wins.
- The CISO is actively building the program — a new vendor relationship is possible.
- Lead with operational efficiency and team leverage.

**5,000+ employees / mature security organization:**
- Complex buying committees. Multiple stakeholders.
- They already have most categories covered — you're displacing something.
- Lead with why you're better than what they have, using specific metrics.
- The entry point is the technical champion, not the CISO.
- Sales cycles are 6–18 months. Relationship precedes pipeline.
