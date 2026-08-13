# Research Protocol — Step-by-Step CISO Intelligence Gathering

This file is a reference for the `/ciso-outreach` skill. Read it before executing Step 1 (Deep Research).

---

## Before You Start

Write down what you know from the user's input AND from the Step 0 intake:
- Name
- Company
- LinkedIn URL (if provided)
- Email (if provided)
- Product or service being sold
- Any intel the user already provided (Apollo data, Sales Nav pull, prior contact, mutual connection, account notes)

User-provided intel goes first. Flag it as `[Confirmed — user intel]` in the report. It's more current and more specific than anything you will find online.

Open each source below in order. Move through them systematically. Collect everything, mark gaps as `[Not found]`. Do not skip a source because you assume it will be empty.

Total time budget for research: 20–35 minutes per target.

---

## Live Search Tool Usage

If Tavily or any web search tool is available, run searches first — before using training data to fill in gaps. Training data is a fallback for what search doesn't find, not the primary source.

**Priority order for each research category:**
1. Run the specified search queries
2. Pull the top 3–5 results per query and read the relevant sections
3. If a search returns nothing useful, note it and move on — do not fabricate
4. Fill any remaining gaps with training data and mark those fields `[Training data — verify]`

Fields marked `[Training data — verify]` in the report are lower confidence. Flag them to the user before they send outreach — a wrong detail in an email destroys the whole thing.

---

---

## Research Order and What to Look For

### Step 1 — LinkedIn (5–8 minutes)

If a LinkedIn URL was provided, go there first. If not, search `[Name] [Company] site:linkedin.com` in a web search.

Collect from their profile:

**Work history:**
Read every position listed — company name, title, dates. Reverse-chronological. Flag any roles at:
- Security vendors (they know how security sales works)
- Government agencies (NSA, CISA, FBI Cyber Division, DoD, DHS)
- Military (especially signals intelligence or cyber units)
- Big Four consulting (Deloitte, KPMG, PWC, EY — compliance-heavy backgrounds)

**Certifications:**
Check the "Licenses and Certifications" section. CISSP, CISM, CISA, CRISC, CEH, OSCP, GIAC certifications (GSEC, GPEN, GCIH, etc.). A GIAC or OSCP means technical depth — adjust copy accordingly.

**Education:**
School name, degree, graduation year if shown. Note if they went to a notable military academy (West Point, Naval Academy, Air Force Academy) or if they went to a school in the same state as the company — local loyalty is a conversation opener.

**Activity feed:**
Scroll their posts for the last 6 months. Note:
- What topics they post about most
- Tone — formal? conversational? technical?
- What gets the most engagement (comments vs. likes)
- Any direct questions they've asked or frustrations they've shared
- Any recent event they spoke at or attended

**Connections section:**
Look at mutual connections. A mutual connection is always a better first move than a cold outreach.

**LinkedIn job postings (their company):**
Filter LinkedIn jobs by their company. Look specifically for:
- Security Engineer, Cloud Security, AppSec, SOC Analyst, Threat Intelligence, GRC postings
- What tools are listed in the requirements section
- How long the posting has been open (30+ days = they're struggling to fill it)

---

### Step 2 — Google: Name + Company (5–8 minutes)

Run these searches in order:

1. `"[Full Name]" "[Company]"` — general news, press mentions, interviews
2. `"[Full Name]" CISO` — security-specific coverage
3. `"[Full Name]" site:darkreading.com OR site:csoonline.com OR site:scmagazine.com OR site:helpnetsecurity.com`
4. `"[Full Name]" podcast`
5. `"[Full Name]" RSA OR "Black Hat" OR ISACA OR DEF CON OR BSides`
6. `"[Full Name]" author OR book`
7. `[Company] breach OR incident OR "data breach" OR "security incident"` — look for any reported incidents in the last 3 years

For each result, open the first 3–5 links that look relevant. Skim for quotes, topics they're associated with, and any personal context (hometown mentioned in a bio, a cause they mentioned, a story they shared).

---

### Step 3 — Company Security Posture (5–8 minutes)

**Start with the company website:**
- What does the company do?
- Who are their customers?
- What industry?
- What compliance logos are on the site (HIPAA, SOC 2, FedRAMP, PCI-DSS, ISO 27001)?

**Crunchbase or PitchBook (if private company):**
Search the company name. Note: funding history (total raised, last round, date), investor names (some investors require portfolio companies to meet security standards), headcount range.

**LinkedIn company page:**
- Total employee count
- Filter by "Security" in the employees section — how many security-titled people work there?
- Recent company posts — has the company commented on any security topics?

**BuiltWith or Wappalyzer (if a web company):**
Look up the company's domain to identify their tech stack. You may find tools relevant to what you're selling: CDN, cloud provider, identity providers (Okta, Azure AD), security tools already in place.

**SEC EDGAR (if public company):**
Search for the company's annual 10-K filing. Search "cybersecurity" in the filing to find:
- Board-level cyber risk disclosures
- Any disclosed incidents in the last 2 years
- Any mention of their security governance structure

For the most recent proxy or earnings call: search `[Company] earnings call transcript site:seekingalpha.com OR site:fool.com`. Search the transcript for "security," "cyber," "CISO," or "risk."

**HaveIBeenPwned and public breach databases:**
Go to haveibeenpwned.com, search the company's primary email domain. Note any breached data sets.

Search `"[Company]" data breach site:databreaches.net` for any past incidents documented in the breach database.

---

### Step 4 — Podcast and Conference Databases (3–5 minutes)

**Run this search:**
`"[Full Name]" podcast OR "interviewed on" OR "episode"`

Common cybersecurity podcasts to check:
- CISO Series (David Spark)
- Darknet Diaries
- Security Now
- Risky Business
- CyberWire Daily
- SANS Internet Stormcast
- Smashing Security
- Security Weekly
- The Privacy Advisor Podcast
- Hacking Humans

If you find an episode, click through. Get:
- The episode title and topic
- The date
- Any notable quotes or positions they took

**Conference databases:**
- RSA Conference speaker search: `"[Full Name]" site:rsaconference.com`
- Black Hat speaker archive: `"[Full Name]" site:blackhat.com`
- DEF CON archives: `"[Full Name]" site:defcon.org`
- ISACA speaker search: `"[Full Name]" site:isaca.org`
- SC Awards: `"[Full Name]" site:scmagazine.com/sc-awards`

If you find a talk, note: the topic, the year, the event. If the talk was recorded and publicly posted, the YouTube title or abstract often includes what position they argued.

---

### Step 5 — X/Twitter and GitHub (3–5 minutes)

**X/Twitter:**
Search `[Full Name] CISO site:twitter.com` or `[Full Name] site:x.com`. Look at:
- What topics they're vocal about
- Whether they engage with vendor content (good sign) or seem hostile to it (adjust approach)
- Recency — are they still active?
- Any frustrations vented publicly (a complaint about alert fatigue, staffing, a vendor, a framework)

**GitHub:**
Search the person's name on GitHub. A GitHub profile signals a technical CISO — one who still writes code or reviews code. If they have a GitHub profile:
- Look at their public repos — what are they building or contributing to?
- Any security tools they've open-sourced?

If a GitHub profile exists, note it and flag: this person responds to technical specifics, not marketing language. Do not use phrases like "holistic security posture" or "comprehensive visibility." Get technical or get out of their inbox.

---

### Step 6 — Board, Association, and Personal Intel (3–5 minutes)

**Board and advisory roles:**
Search `"[Full Name]" "board of directors" OR "advisory board" OR "board member"`. LinkedIn often lists these in the "Volunteer" or "Experience" section. Also check Crunchbase for any company where they're listed as an advisor.

**ISACA / ISSA / ISC2:**
Search `"[Full Name]" ISACA chapter OR ISSA OR "(ISC)2"`. Local chapter involvement (officer, program chair, speaker) signals they're embedded in the security community — and that other chapter members know them.

**Personal interests:**
Check LinkedIn's "About" section. Check X/Twitter bio. Check any podcast episode introductions (hosts often introduce guests with personal context — "John is a marathon runner and father of two who..."). Check any interview bios. Look for:
- Sports they play or watch (local team loyalty matters for direct mail)
- Running, cycling, obstacle races (many security professionals)
- Coaching youth sports
- Faith community involvement (some explicitly mention church, synagogue, mosque in bios)
- Veterans organizations
- Charitable causes
- Alma mater pride (do they post about their school? wear school gear in photos?)

**Hometown and location:**
LinkedIn shows their location. Has their bio on any other site mentioned where they grew up? Homeownership-level familiarity with their city (knowing a local event, a local sports team, a local institution) makes direct mail and the first call more credible.

---

## After Research — Before Writing Anything

Ask yourself three questions:

1. **What does this person actually care about — based on what they've written, said, and done publicly?**
   Not "what do CISOs care about generically." This specific person, based on evidence.

2. **What is the strongest signal in this account?**
   New CISO? Sector breach? Job posting gap? Compliance deadline? Name the single most urgent trigger.

3. **If I were this person, what would make me respond to an email from a stranger?**
   The answer is almost always: something specific, something I haven't heard before, or something that makes me feel like this person actually paid attention. Not a feature pitch.

If you can't answer all three questions, you don't have enough research yet. Go back to Step 2 and Step 3 — the company posture and personal intel sections are where the most actionable material hides.

---

## Research Quality Checklist

Before moving to the intelligence report, verify:

- [ ] At least 3 data points from the executive's LinkedIn activity (posts, comments, article shares)
- [ ] Career history goes back at least 10 years or to beginning of career
- [ ] Company compliance environment identified (at least one applicable framework)
- [ ] At least one concrete buying signal scored (even if it's only Weak)
- [ ] Personal interest or hook identified for direct mail (or explicitly marked [Not found])
- [ ] No fabricated data — every claim has a source you can point to

If any box above is unchecked, note it explicitly in the intelligence report. A missing data point clearly labeled is better than a wrong data point that gets used in outreach copy.

---

## Research Confidence Rating

At the end of the intelligence report, output a confidence rating before handing off to the outreach package:

```
Research Confidence Rating
--------------------------
Profile depth:         [High / Medium / Low]
Company posture:       [High / Medium / Low]
Buying signals:        [High / Medium / Low]
Personal intel:        [High / Medium / Low]

Fields marked [Training data — verify]: [list them]
Fields marked [Not found]: [list them]

Recommended: Before sending Email 1, verify [list the highest-risk gaps].
```

**High** = confirmed from live search or user-provided intel with a clear source.
**Medium** = confirmed from training data or a source that may be outdated.
**Low** = inferred from partial signals, no direct confirmation found.

Low-confidence fields should not be referenced in outreach copy. Flag to the user that these sections need manual verification.
