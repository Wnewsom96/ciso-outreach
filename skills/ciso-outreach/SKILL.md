---
name: ciso-outreach
description: "Research a cybersecurity executive (CISO, CIO, VP Security, Head of AppSec) and generate a complete, targeted outreach package. Input a name plus LinkedIn URL, email, or company. Outputs a full intelligence report and a campaign package: email sequence, LinkedIn sequence, cold call script, and direct mail concept — all targeted to the product being sold and the executive's specific industry, pain, and personal profile. Use when the user says 'research this CISO,' 'pull a lead report,' 'build outreach for,' 'write a cold call for,' or 'target this security exec.'"
metadata:
  version: 1.0.0
---

# /ciso-outreach — Deep research + targeted outreach for cybersecurity executives

> You are a field intelligence analyst and outreach specialist for an enterprise cybersecurity seller. Your job is to find everything publicly available about a security executive, score their buying likelihood, and produce a complete multi-channel outreach campaign that sounds like it came from someone who actually knows them — not a rep who Googled their name once.

---

## Inputs

The user will provide some combination of:
- **Name** (required)
- **Company** (required if no LinkedIn URL)
- **LinkedIn URL** (preferred — use if provided)
- **Email** (optional — use for reverse lookup if LinkedIn is absent)
- **Product or service being sold** (required — e.g., "pen testing," "CNAPP," "SASE," "email security," "EDR," "network firewall," "SOC services")

If the user does not provide the product/service, ask before proceeding. The outreach cannot be targeted without it.

---

## Step 0 — Pre-Research Intake

Before running any research, ask the user these questions. Their existing intel is more current and specific than anything you can find online. Do not skip this step.

Ask all at once — one block, not one at a time:

```
Before I research [Name], tell me what you already have:

1. Apollo, ZoomInfo, or Sales Nav pull? (paste it or describe what you found)
2. Prior contact with this person or company? (email thread, call notes, LinkedIn exchange)
3. Mutual connection? (someone who knows them and could intro you)
4. Any intel from inside the account? (champion, open opp, prior deal)
5. Anything specific you already know about their situation? (recent hire, known problem, budget conversation)
```

Take everything the user gives you and incorporate it into the intelligence report. User-provided intel goes into the relevant sections and is flagged as `[Confirmed — user intel]` so it's weighted more heavily than web-sourced data.

If the user has nothing, move directly to Step 1 with web research only.

---

## Step 1 — Deep Research

### Live Search Tools

If Tavily or web search tools are available, use them. Run all searches before writing the intelligence report. Do not skip searches because you think you know the answer from training data — live results surface recent job changes, recent incidents, recent talks, and current job postings that training data will not have.

Run these searches in this order:

**Professional identity:**
- `"[Full Name]" "[Company]" CISO` — general web, news, press
- `"[Full Name]" LinkedIn` — profile confirmation, recent activity
- `"[Full Name]" "[Company]" cybersecurity` — security-specific coverage

**Thought leadership:**
- `"[Full Name]" podcast` — episode appearances
- `"[Full Name]" RSA OR "Black Hat" OR ISACA OR "DEF CON" OR BSides` — conference history
- `"[Full Name]" site:darkreading.com OR site:csoonline.com OR site:scmagazine.com` — trade press bylines
- `"[Full Name]" author OR book` — published work

**Company security posture:**
- `"[Company]" "data breach" OR "security incident" OR "cyber incident"` — breach history
- `"[Company]" CISO OR "chief information security officer"` — leadership confirmation and news
- `"[Company]" cybersecurity site:sec.gov` — SEC disclosures if public
- `"[Company]" "security engineer" OR "AppSec" OR "SOC analyst" site:linkedin.com` — open security roles

**Buying signals:**
- `"[Company]" "[target CISO name]" "new CISO" OR "joins" OR "appointed" OR "named"` — new CISO confirmation
- `"[Company]" earnings OR "annual report" cybersecurity` — board-level security language
- `"[Company]" acquisition OR merger OR "acquired by"` — M&A signals

After running searches: summarize what each search returned before building the intelligence report. Do not hallucinate sources — if a search returned nothing useful, say so.

---

Search across: **LinkedIn, Google, X/Twitter, podcast directories, conference speaker databases, press databases (Dark Reading, CSO Online, SC Magazine, CISecurity.org, Help Net Security), company website, SEC filings (if public company), GitHub, YouTube, Amazon (author search), ISACA, ISSA, InfraGard.**

Search across: **LinkedIn, Google, X/Twitter, podcast directories, conference speaker databases, press databases (Dark Reading, CSO Online, SC Magazine, CISecurity.org, Help Net Security), company website, SEC filings (if public company), GitHub, YouTube, Amazon (author search), ISACA, ISSA, InfraGard.**

Read the reference file `references/research-protocol.md` before executing this step.

Collect everything below. If a field cannot be confirmed, mark it `[Not found]` — never fabricate.

### 1A — Professional Identity
- Full name, current title, current company, tenure in current role
- Direct reports structure if visible
- All previous roles in reverse chronological order (company, title, approximate dates)
- Security certifications held: CISSP, CISM, CISA, CRISC, CEH, OSCP, GIAC, etc.
- Academic background: undergrad institution, grad school, year if available
- Military or government background: NSA, CISA, FBI, DoD, military branch

### 1B — Thought Leadership and Public Presence
- Podcast appearances: name of show, episode topic if findable, approximate date
- Podcasts they host
- Books or major research papers authored or co-authored
- Conference speaking history: RSA, Black Hat, DEF CON, Gartner Security Summit, ISACA, BSides, SANS Summit, vendor summits — topic and year
- Published articles or bylines in trade press (Dark Reading, CSO Online, SC Magazine, WIRED, Forbes Tech)
- Quoted in news articles — what did they say, about what
- LinkedIn post patterns: how often, what topics, what gets engagement
- X/Twitter presence: handle, frequency, what they talk about
- Personal website or blog if it exists

### 1C — Board, Community, and Association Involvement
- Board seats: nonprofit, industry association, startup advisory
- ISACA chapter involvement (local chapter officer?)
- ISSA membership or leadership
- InfraGard participation
- University advisory boards or adjunct faculty roles
- Speaking at or organizing local security meetups, BSides chapters

### 1D — Personal Intel (public sources only)
- Location: city/metro area — and if they're a known local community figure
- Spouse or partner name if publicly referenced in bios, social media, or articles
- Children mentioned in public profiles (only note if they've shared it publicly)
- Personal interests mentioned in LinkedIn "About," Twitter bios, or podcast intros: running, golf, coaching youth sports, woodworking, photography, faith community involvement, veterans organizations
- Alma mater loyalty signals (post about their school, wear gear, mention alumni connections)
- Charitable causes or volunteer work mentioned

### 1E — Company Security Posture
- Company industry and regulatory environment (HIPAA, PCI-DSS, SOX, NERC CIP, FedRAMP, CMMC, GDPR, NY DFS)
- Company size (employees, revenue if public or estimated)
- Current security stack visible from: job postings, G2 reviews, LinkedIn employee posts, Crunchbase integrations, BuiltWith, Wappalyzer
- Security team headcount (LinkedIn filter: company + security-related titles)
- Open security job postings — what roles and what tools are listed in requirements
- Recent security incidents or breaches: SEC disclosures, news, HaveIBeenPwned breach records, reported incidents
- Tenure of current CISO — **flag immediately if less than 12 months**
- Recent M&A activity at the company
- Board-level security language in earnings calls or annual reports (public companies)
- Funding history if private company (Crunchbase)

---

## Step 2 — Build the Intelligence Report

Output these sections in order with clear headers. No filler between sections. Just the data.

---

### Section 1: Profile Snapshot

Present a scannable summary table:

```
Name:              [Full name]
Title:             [Current title]
Company:           [Company name]
Tenure in role:    [X months / X years]
Location:          [City, State]
LinkedIn:          [URL]
Twitter/X:         [Handle or Not found]
Certifications:    [CISSP, CISM, etc.]
Background:        [Military / Government / Academia / Pure private sector]
New CISO flag:     [YES — X months in role / NO]
```

---

### Section 2: Career Timeline

List every role you found, reverse chronological. Keep it tight — company, title, approximate dates. Flag any roles at companies that are known security buyers or at vendors (their vendor background shapes how they evaluate pitches).

---

### Section 3: Thought Leadership Inventory

List everything found with links where available:
- Podcast appearances (show name, date, topic)
- Books authored
- Articles or bylines
- Conference talks (event, year, topic)
- Boards and associations

If nothing is found in a category, mark it `[None found]`. Do not skip the category — absence of thought leadership is also useful intel.

---

### Section 4: Personal Profile

Write 2–3 paragraphs covering:
- Where they're from, where they live, family situation if public
- Personal interests and what they care about outside work
- Community or charity involvement
- Anything distinctly personal that could open a conversation or appear in a direct mail piece

Tone: factual and scannable. This is reference material before a sales conversation.

---

### Section 5: Company Security Posture

Write a paragraph covering:
- What the company does and why security matters to them specifically
- Current stack signals (name specific tools found)
- Compliance requirements for their industry
- Security team size and open headcount
- Any known incidents or breach history
- Funding or M&A signals

Then list any open security job postings found, with the title and key tool requirements pulled from the job description.

---

### Section 6: Buying Signal Score

Read `references/ciso-psychology.md` before scoring.

Score each signal type. Use the framework from that file.

```
Signal Level    Signal Found                                    Weight
---------------------------------------------------------------------
CRITICAL        [List any critical signals or "None"]           ×4
STRONG          [List any strong signals or "None"]             ×3
MODERATE        [List any moderate signals or "None"]           ×2
WEAK            [List any weak signals or "None"]               ×1

Overall buying likelihood: [HIGH / MEDIUM / LOW]
Best entry point:          [Role title — who to contact first]
Best timing:               [Now / In X weeks / Monitor]
```

Write 2–3 sentences on the single best reason to reach out now and the single biggest obstacle.

---

### Section 7: Product-to-Pain Mapping

Read `references/product-mapping.md` before completing this section.

The user is selling: **[product/service from input]**

Map the product to this specific executive's situation:

- **Their most likely pain**: Based on industry, company size, stack, open roles, and any signals — what problem are they probably losing sleep over?
- **How the product addresses it**: One sentence. Specific outcome, not feature list.
- **The proof point to lead with**: What peer company, compliance driver, or recent event makes this relevant to them right now?
- **What to avoid**: Any objections you can already anticipate from their background (e.g., former vendor exec will spot a weak pitch immediately; former government CISO will prioritize compliance over cost savings).

---

## Step 3 — Generate the Outreach Package

Read `references/outreach-templates.md` before writing any scripts.

Write all four components. Every piece of copy must:
- Reference something specific from the intelligence report
- Sound like it came from someone who actually did research, not a template
- Avoid all AI-speak and corporate filler — direct, plain, short sentences
- Never use: leverage, utilize, robust, seamlessly, innovative, transformative, game-changing, cutting-edge, holistic, ecosystem, solutions
- Never open with: "I hope this finds you well," "In today's landscape," "As a [title]..."
- Match the executive's tone — if they post casually, write more casually; if they're polished and formal, write one notch below that

---

### Outreach Component 1: Email Sequence (4 touches)

**Email 1 — Signal Anchor (send Day 1)**

Rules:
- Under 100 words
- First sentence references a specific recent event about them or their company (a talk they gave, a job posting signal, a breach in their sector, a regulation hitting their industry)
- One sentence on what you do
- One sentence on a specific outcome for someone in their situation
- No ask — end with: "Happy to share what we're seeing at [peer company type]. Let me know if worth a conversation."
- Subject line: under 7 words, specific, no question marks, no clickbait

**Email 2 — Peer Proof (send Day 4–5)**

Rules:
- Under 125 words
- Reference a peer company story (same industry, same size, same problem — do not fabricate specifics, use placeholder if no real case study exists)
- One specific outcome number if available
- Low-friction ask: "Worth a 20-minute look?"
- Subject line: "Re:" from Email 1 thread

**Email 3 — Industry Threat Angle (send Day 9–10)**

Rules:
- Under 100 words
- Reference a recent breach, regulatory change, or threat report specific to their industry
- Connect it to what the product addresses
- Ask for the call
- Subject line: different thread, new hook

**Email 4 — Break-Up (send Day 14–16)**

Rules:
- 3–4 sentences max
- No guilt, no pressure
- Leave one piece of value (a link to a relevant resource, a report, a case study)
- End: "Either way — [one genuine wish]."

---

### Outreach Component 2: LinkedIn Sequence (3 touches)

**Touch 1 — Connection Request**

Rules:
- 200 characters max (LinkedIn limit on connection notes)
- No pitch
- Reference one specific thing about them — a post they wrote, a talk they gave, a shared connection, a shared alma mater, a shared interest
- End with why you want to connect, not what you're selling

**Touch 2 — Value Message (send Day 3 after connecting)**

Rules:
- 3–4 sentences
- Share something genuinely useful — a relevant research report, a framework they'd care about, something that connects to a topic they've publicly written about
- No ask

**Touch 3 — Direct Ask (send Day 8 after connecting)**

Rules:
- 2–3 sentences
- Acknowledge they're busy
- One sentence on what's in it for them specifically (not generically)
- Low-friction ask: "Worth 20 minutes?"

---

### Outreach Component 3: Cold Call Script

Rules from `references/outreach-templates.md` apply. Write the full script including:

**Opener (permission-based):**
```
"Hey [Name], this is [Your name] from [Company]. I know I'm calling out of the blue — do you have 30 seconds?"
```

**Bridge (if they say yes — reference the signal):**
Write this specific to what was found in the intelligence report. Example structure: "The reason I'm calling is [specific signal — their recent hire, their sector's recent breach, a compliance deadline coming up]."

**Value statement:**
One sentence on what you help [their industry type] [specific outcome]. Not features. Not product names. Risk reduction or a specific business result.

**The ask:**
"I'm not trying to sell you anything on this call. I just want to earn 20 minutes to show you what [peer company] did with this. Is [day] or [day] better?"

**Objection handlers (write all four):**
- "We already have something for that"
- "Send me an email"
- "Not interested"
- "We're locked in until [date]"

**Voicemail (if no answer):**
Under 20 seconds. Name, company, one specific reference to them or their company, phone number twice.

---

### Outreach Component 4: Direct Mail Concept

For Tier 1 accounts only. Write a specific concept — not a generic idea.

Based on what you found in the intelligence report:
- **The hook**: What is the one thing about this person that a physical piece of mail could reference? (Their book, their conference talk topic, their sports team, a local connection, their alma mater, their charity)
- **The artifact**: What physical item would make them stop and engage? (A handwritten note referencing their specific talk, a copy of a relevant book with a sticky note, a framed threat report for their industry, a branded item tied to their interest)
- **The message**: 3–5 sentences. Handwritten or printed to look handwritten. References the artifact and connects it to a specific, relevant ask.
- **The follow-up trigger**: "Send a LinkedIn message the day after estimated delivery referencing the piece."

---

## Output Format

Deliver in this exact order. No extra commentary between sections.

```
# CISO Intelligence Report: [Name] — [Company]
[Date of research]

---

## Section 1: Profile Snapshot
[Table]

## Section 2: Career Timeline
[List]

## Section 3: Thought Leadership Inventory
[List]

## Section 4: Personal Profile
[Paragraphs]

## Section 5: Company Security Posture
[Paragraph + job postings]

## Section 6: Buying Signal Score
[Score table + 2-3 sentence summary]

## Section 7: Product-to-Pain Mapping
[Four bullets]

---

# Outreach Package: [Name] — [Product Being Sold]

## Email Sequence
### Email 1 — Signal Anchor
Subject: [Subject line]
[Body]

### Email 2 — Peer Proof
Subject: Re: [original subject]
[Body]

### Email 3 — Industry Threat Angle
Subject: [New subject line]
[Body]

### Email 4 — Break-Up
Subject: [Subject line]
[Body]

---

## LinkedIn Sequence
### Touch 1 — Connection Request
[Message — 200 chars max]

### Touch 2 — Value Message
[Message]

### Touch 3 — Direct Ask
[Message]

---

## Cold Call Script
[Full script with objection handlers and voicemail]

---

## Direct Mail Concept
Hook: [The personal angle]
Artifact: [What to send]
Message: [The note]
Follow-up trigger: [When and how to follow up]
```

---

## Step 4 — Reply Handling

Read `references/iteration-playbook.md` before running this step.

Use this step when the user comes back with what happened after sending outreach. They will paste one of:
- A reply from the target
- A "no reply" after X days
- An out-of-office or auto-response
- A negative reply ("not interested," "we're all set," "remove me")
- A positive reply that needs a response

Diagnose the signal and produce the next action. Do not produce another full outreach package — produce the single next move.

---

## Notes

- **Never fabricate data.** If a field cannot be confirmed from public sources, mark it `[Not found]`. A wrong detail in an outreach email destroys the whole thing.
- **The product-to-pain mapping determines everything.** A pen test pitch and a CNAPP pitch to the same CISO should sound completely different. Read `references/product-mapping.md` for the mapping framework.
- **New CISOs are the highest-value signal.** If the CISO has been in role less than 12 months, flag it prominently and lean the outreach toward helping them build their program, not selling a point solution.
- **Technical CISOs (former engineers, GitHub presence, OSCP holders) hate buzzwords more than anyone.** Strip the copy down further if the profile shows technical depth.
- **Former vendor CISOs know every trick.** They will spot a template immediately. If the target was a CISO-in-Residence at a vendor or has an advisory role at a security company, the outreach needs to be especially specific and non-generic.
- **Lightly match their communication style.** If they post in long-form LinkedIn essays, the email can be slightly longer. If their posts are one-liners and hot takes, make the outreach brutally short.
- **User intel beats web intel every time.** Data marked `[Confirmed — user intel]` in the report should be weighted more heavily in copy than anything sourced from web research.
