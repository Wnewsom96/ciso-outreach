# ciso-outreach — Claude Code Skill

A Claude Code skill for enterprise cybersecurity sellers. Research any security executive — CISO, CIO, VP Security, Head of AppSec — and get a full intelligence report plus a ready-to-use multi-channel outreach campaign in one command.

Built for people selling pen testing, CNAPP, SASE, EDR, email security, network security, SOC services, or any enterprise cybersecurity product.

---

## What it does

Call it with a name, a LinkedIn URL or company, and what you're selling. It:

1. Collects what you already know — Apollo data, Sales Nav pulls, prior email threads, mutual connections, account notes. Your intel goes first because it's more current than anything on the web.
2. Runs live research via Tavily (if available) across LinkedIn, Google, podcast databases, conference archives, company job postings, SEC filings, and breach databases — then fills gaps with training data, flagged by confidence level
3. Builds a structured intelligence report — career timeline, thought leadership inventory, personal profile, company security posture, buying signal score, product-to-pain mapping, and a research confidence rating that tells you what to verify before sending
4. Writes the outreach package — a 4-touch email sequence, a LinkedIn sequence (connection request + value message + ask), a cold call script with objection handlers and a voicemail, and a specific direct mail concept tailored to what the research found
5. Handles replies — paste back what happened (positive, soft no, hard no, no reply, out-of-office) and it tells you the single next move

The output sounds like it came from someone who actually knows the target. Not a mail merge. Not a template dump. Every piece of copy references something specific from the research.

---

## Installation

### Option 1 — Per session (no install required)

```bash
claude --plugin-url https://github.com/Wnewsom96/ciso-outreach/archive/refs/heads/main.zip
```

### Option 2 — Clone and install for a session

```bash
git clone https://github.com/Wnewsom96/ciso-outreach.git
claude --plugin-dir ./ciso-outreach
```

### Option 3 — Install permanently (always available)

```bash
git clone https://github.com/Wnewsom96/ciso-outreach.git
cp -r ciso-outreach/skills/ciso-outreach ~/.claude/skills/ciso-outreach
```

---

## Usage

```
/ciso-outreach [name] [linkedin_url or company] [product_or_service]
```

**Examples:**

```
/ciso-outreach "Sarah Chen" linkedin.com/in/sarahchen "penetration testing"
```

```
/ciso-outreach "Marcus Reid" "Atrium Health" "CNAPP / cloud security"
```

```
/ciso-outreach "David Park" linkedin.com/in/davidpark-ciso "SASE / zero trust"
```

If you don't include the product or service, it will ask before starting research. The outreach cannot be targeted without knowing what you're selling.

---

## What you get

### Intelligence Report

**Section 1 — Profile Snapshot**
Name, title, company, tenure, location, certifications, background, new CISO flag (critical buying signal if under 90 days in role).

**Section 2 — Career Timeline**
Every role found, reverse chronological. Flags any vendor, government, or military background.

**Section 3 — Thought Leadership Inventory**
Podcast appearances, books authored, conference talks, published articles, board and association memberships. Absence of thought leadership is also noted.

**Section 4 — Personal Profile**
Where they're from, personal interests, community involvement, anything that makes a direct mail piece or a first call feel personal instead of generic.

**Section 5 — Company Security Posture**
What the company does and why security matters to them specifically. Current stack signals from job postings and tech intelligence tools. Compliance requirements for their industry. Security team size. Any known incidents or breach history. Open security job postings with key tool requirements.

**Section 6 — Buying Signal Score**
Every signal scored as Critical, Strong, Moderate, or Weak. Overall buying likelihood (High/Medium/Low). Best entry point (who to contact first). Timing recommendation. Two-sentence summary of the best reason to reach out now and the biggest obstacle.

**Section 7 — Product-to-Pain Mapping**
Maps your specific product or service to this executive's specific situation. What they're probably losing sleep over. How your product addresses it. The proof point to lead with. What to avoid saying based on their background.

### Outreach Package

**Email Sequence (4 touches)**
- Email 1: Signal Anchor — specific hook from the research, under 100 words
- Email 2: Peer Proof — similar company story, one specific outcome, soft ask
- Email 3: Industry Threat Angle — recent breach, regulation, or threat in their sector
- Email 4: Break-Up — no pressure, leave one piece of genuine value

**LinkedIn Sequence (3 touches)**
- Touch 1: Connection request — 200 chars max, no pitch, one specific reference
- Touch 2: Value message — something useful before asking for anything
- Touch 3: Direct ask — short, specific, one question

**Cold Call Script**
Full script including: permission opener, signal-specific bridge, value statement, direct ask. Five objection handlers (already have something / send me an email / not interested / locked in / don't take cold calls). Voicemail under 20 seconds.

**Direct Mail Concept**
Artifact, message, and follow-up trigger. Tailored to what the research found — their book, their conference talk, their alma mater, their personal interest, or a threat report for their specific industry.

---

## Copy standards

Every piece of outreach this skill generates follows strict copy rules:

- No AI-speak: no "leverage," "utilize," "robust," "seamlessly," "holistic," "synergy," "transformative," "ecosystem," "game-changing"
- No fake openers: no "I hope this finds you well," "In today's landscape," "As a CISO..."
- No em dashes
- No bullet dumps in email body — those read like brochures
- Short sentences
- One idea per sentence
- Every email contains at least one reference specific to this person or company

The skill also adjusts tone to the target. A technical CISO with an OSCP and a GitHub profile gets a shorter, blunter version. A former government CISO gets compliance-first framing. A thought leader gets their ideas engaged with before the pitch.

---

## What this skill covers

Product categories with full pitch mapping:
- Penetration Testing / Red Team Services
- CNAPP / CWPP / CSPM (Cloud Security)
- SASE / Zero Trust Network Access
- Email Security / BEC Protection
- EDR / XDR
- Network Security / NGFW
- SOC / MDR / MSSP Services

Industry-specific CISO pain points:
- Healthcare
- Financial Services
- Manufacturing / Industrial / OT
- Retail / E-commerce
- Technology / SaaS
- Government / Defense
- Education

---

## Reference files

The skill uses five reference files included in this repo:

- `references/research-protocol.md` — step-by-step research methodology with Tavily search queries, source-by-source instructions, confidence rating system, and research quality checklist
- `references/ciso-psychology.md` — buying trigger framework, CISO evaluation criteria, the new CISO 90-day window, buying committee order, industry-specific pain points
- `references/product-mapping.md` — maps 7 cybersecurity product categories to specific CISO pain points, pitch angles by trigger, company size adjustments
- `references/outreach-templates.md` — detailed copy rules for every channel, full email templates by trigger type, objection handler scripts, direct mail concept frameworks
- `references/iteration-playbook.md` — what to do after outreach goes out: how to read no-reply patterns, handle positive replies, navigate soft and hard negatives, and re-enter accounts correctly

---

## Notes

This skill does not fabricate data. If a field cannot be confirmed from public sources, it marks it `[Not found]`. A missing data point clearly labeled is better than a wrong one that ends up in outreach copy.

All research is done using public sources: LinkedIn, Google, company websites, podcast databases, conference archives, SEC filings, job postings, breach databases.

---

## License

MIT — free to use, fork, and modify.
