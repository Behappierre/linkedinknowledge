# SKILL: LinkedIn Knowledge Base - Post Documentation & Strategy

## Purpose
This skill governs how to document LinkedIn post performance, update the knowledge base, score posts, interpret demographics, and apply strategic lessons for Olivier Andre's LinkedIn thought leadership programme.

**Read this file completely before taking any action on any LinkedIn task.**

---

## Step 0: Always Read the Latest Files First

Before doing anything - drafting a post, documenting analytics, answering a strategy question - fetch the current state of the knowledge base:

```
1. github:get_file_contents → 02-performance-analysis/linkedin-knowledge-base-addendum-january-2026.md
2. github:get_file_contents → 02-performance-analysis/_CURRENT-RANKINGS.md
```

**The addendum** is the living record. It contains:
- All posts from Post 14 onwards with scores and lessons
- The current all-time performance ranking (authoritative)
- The quotable insights database (Platinum / Gold / Silver tiers)
- Strategic contacts and their engagement history
- Every confirmed writing rule and content lesson

**`_CURRENT-RANKINGS.md`** is the standalone quick-reference rankings file. It contains the full post table with impressions, reactions, comments, scores, and links to individual analysis files. It must be updated whenever a new post is documented, whenever a post reaches its final impression count, or whenever a ranking changes. It is separate from the addendum by design — the addendum contains the analytical detail; this file contains the ranked table and structural failure patterns.

The files in `/mnt/project/` are static copies and will be outdated. Always read from GitHub.

---

## Step 1: Understand the Repository Structure

```
linkedinknowledge/
├── 00-skill/
│   └── SKILL.md                          ← You are here
├── 02-performance-analysis/
│   ├── linkedin-knowledge-base-addendum-january-2026.md  ← PRIMARY LIVING DOCUMENT
│   ├── _CURRENT-RANKINGS.md                              ← STANDALONE RANKINGS TABLE
│   ├── [post-name]-post-analysis-[month]-2026.md         ← Individual post analyses
│   └── demographics-of-followers.md
├── 03-execution-plans/
├── 04-templates/
└── 05-network/
    └── network-contacts-reference.md     ← Industry connections with strategic intelligence overlay
```

**Three-layer documentation model:**

| Layer | File | Contents |
|-------|------|----------|
| Ranked table | `_CURRENT-RANKINGS.md` | All posts ranked by impressions, scores, links to analyses |
| Living summary | `linkedin-knowledge-base-addendum-january-2026.md` | Post summaries, lessons, quotes, contacts |
| Full detail | `[topic]-post-analysis-[month]-[year].md` | Complete analytics, demographics, reactor analysis |

**The network contacts reference** (`05-network/network-contacts-reference.md`) is the single source of truth for the broader follower and connection network. The addendum Strategic Contacts table covers active engagers only; the network file covers the full passive audience.

---

## Step 2: Identify the Task Type

**Task A: Document a new post with analytics**
→ Follow the Post Documentation Protocol (Section 3)

**Task B: Draft a new post**
→ Follow the Post Drafting Protocol (Section 4)

**Task C: Answer a strategy question**
→ Read the addendum, apply the framework, answer from current data

**Task D: Update the knowledge base with new lessons or contacts**
→ Update the addendum directly, note the date

**Task E: Network / contacts work**
→ Read `05-network/network-contacts-reference.md` for the full connection picture. Cross-reference the addendum Strategic Contacts table for active engagers. Update the network file when new connections are added or warm inbound contacts are promoted to active strategic contacts.

---

## Section 3: Post Documentation Protocol

### 3.1 What You Need Before Starting

To document a post, you need:
- The full post text
- Analytics data: impressions, members reached, reactions, comments, reposts, saves, sends, profile views, followers gained
- Demographics: full seniority breakdown, top companies with percentages, top locations with percentages, industry breakdown, company size breakdown
- Names of notable reactors and commenters with their roles/companies
- Any comment thread content

If any of this is missing, ask for it before proceeding.

### 3.2 File Creation and Update Sequence

**Always complete in this order:**

**First:** Create the individual post analysis file
```
02-performance-analysis/[topic-slug]-post-analysis-[month]-[year].md
```

Example slugs: `eu-telematics-tsi`, `heathrow-announcement`, `railway-within-railway`

Use `github:push_files` for new files (no SHA required).

**Second:** Update the addendum to add the post summary and any new lessons, contacts, or quote database entries.

To update the addendum, you must first fetch its current SHA:
```
github:get_file_contents → 02-performance-analysis/linkedin-knowledge-base-addendum-january-2026.md
```
Use the `sha` value from the response in your `create_or_update_file` call. SHA changes with every commit — always fetch fresh.

**Third:** Update `_CURRENT-RANKINGS.md` to insert the new post at the correct rank position.

Fetch current SHA before updating:
```
github:get_file_contents → 02-performance-analysis/_CURRENT-RANKINGS.md
```

**Fourth (if relevant):** If the post generated new warm inbound connections or promoted a passive follower to active contact, update `05-network/network-contacts-reference.md` accordingly.

### 3.3 Individual Post Analysis File Structure

Every analysis file must contain these sections in order:

1. **The Post (Final Version)** - complete post text verbatim, plus visual description
2. **The Strategic Setup** - why this post was written, what it was designed to achieve, any planted quotes or multi-post architecture
3. **Performance Metrics** - all numbers from analytics
4. **Demographics** - full breakdown with interpretation
5. **The Standout Numbers** - 3-5 demographic facts that are strategically significant, with explanation of why
6. **Reactor Analysis** - named reactors with roles, why each matters, what their engagement signals
7. **Comment Thread** - full content of any self-comments and external comments
8. **Post Development Notes** - any source verification, framing decisions, visual choices made during drafting
9. **Scoring** - score out of 10 with explicit reasoning for points earned and deducted
10. **Performance Tier Classification** - which tier (see Section 5) and why
11. **Strategic Value Beyond Metrics** - what the post achieved that impression counts don't capture
12. **Lessons Learned** - new lessons specific to this post
13. **Follow-Up Actions** - numbered list of concrete next steps
14. **All-Time Ranking Update** - the full updated table showing where this post sits

### 3.4 Addendum Update Protocol

When updating the addendum, add:

**In the Posts section:** A summary entry for the new post with:
- Date, score, all key metrics on one line each
- Demographic highlights (seniority total, notable company %, new sectors)
- Key reactors (name, role, why significant)
- Comment thread summary
- Context (if second post on same day, if part of a series, etc.)
- Link to full analysis file

**In the Lessons section:** Any new confirmed lessons from this post. Only add a lesson if it is either:
- New (not previously documented)
- A significant confirmation of an existing rule with new evidence

**In the Quotable Insights Database:** Any new quotes that meet Gold or Platinum standard (see Section 6).

**In the Strategic Contacts table:** Any new contacts who engaged for the first time, or status updates for existing contacts.

**In the Performance Summary:** Update the period total.

**In the All-Time Ranking:** Insert the new post at the correct position.

**At the bottom:** Update the "last updated" date and list what was changed.

### 3.5 `_CURRENT-RANKINGS.md` Update Protocol

When updating `_CURRENT-RANKINGS.md`:

- Insert the new post at the correct rank in the main table
- Update performance tiers if the new post changes tier boundaries
- Add any new structural failure pattern if documented
- Update the correction/update log at the top with today's date and a one-line summary
- Update the footer "last updated" date and post count

---

## Section 4: Post Drafting Protocol

### 4.1 Before Writing Anything

1. Read the addendum to know: current lessons, available quotes in the database, what has worked, what has failed
2. Identify which post template applies (see 4.3)
3. Confirm you have a borrowed credibility quote - if not, pause and ask where the insight is coming from

### 4.2 Absolute Writing Rules (Never Break These)

- **No em dashes (—).** Ever. Use comma, colon, full stop, or rephrase.
- **Never qualify borrowed credibility.** No "I paraphrase", "not exact words", "roughly". Direct quote or full anonymisation, nothing in between.
- **No bullet points in the post body.** Prose only. Lists in natural language: "three things matter: X, Y, and Z."
- **Maximum 4 hashtags.** Specific and industry-relevant. No generic tags (#Innovation, #Leadership, #DigitalTransformation).
- **Post Tuesday-Thursday, 7-9am GMT.** Never post twice on the same day by choice.
- **End with an engagement question.** Never end with a statement or a thank-you.

### 4.3 Post Templates

**Template A: Borrowed Credibility + Operational Insight** (default, highest performing)
Structure: Operator quote → "I assumed X, but learned Y" → Concrete operational details → Orchestration insight → Engagement question

**Template B: Real-Time Observation** (when experiencing a problem in the moment)
Structure: Where you are right now → The specific problem with visual evidence → Orchestration insight → Invitation for explanation

**Template C: Conference/Event Insight**
Structure: Executive quote from event → Context → Why it matters → Orchestration angle → Engagement question

**Template D: Named Framework / Policy Analysis**
Structure: Most senior available quote → Framework with named layers → Why current approach fails → Orchestration solution → Engagement question

**Template E: Planted Quote Activation** (for major announcements)
Structure: Quote planted in earlier post → "I didn't mention it at the time but..." → The announcement → Orchestration positioning → Rail/sector equivalent question

### 4.4 Opening Hook Rules

**Good openings:**
- Direct operator quote in quotation marks
- A shocking specific number
- A surprising dialogue ("Tuesdays and Thursdays." That was the answer when...)
- Real-time scene ("Currently on a Pendolino to Glasgow...")
- Technical surprise with specific detail
- Scenario hook with precise operational detail ("A bus runs four minutes late. The operator knows. The authority finds out at month end.")

**Bad openings (rewrite immediately if you see these):**
- "Proud to have represented..."
- "Delighted to announce..."
- "I recently attended..."
- "Fascinating discussion about..."
- Any opening that puts context before insight

### 4.5 The Engagement Question

The final line must invite response. Good patterns:
- Cross-sector comparison: "Does any other sector have such an extreme [ratio]?"
- Scaling challenge: "For those moving beyond pilots: what breaks first, [A], [B], or [C]?"
- Fragmentation reveal: "Who owns [the X layer] in your organisation - and are they talking to each other?"
- Provocative gap: "If we can build this in 8 hours, why doesn't it exist already?"
- Accountability gap: "The question is not only who holds each contract. It is who is accountable for the journey between them."

### 4.6 Visual Selection

Priority order:
1. Real photo from real location (authentic, stops scrolling)
2. Data visualisation / chart (precision targeting)
3. Metaphor image (thought leadership)
4. Nothing (last resort)

Never use AI-generated composite images. Real photos always beat renders.

---

## Section 5: Scoring Methodology

Score every post out of 10 using this framework:

### Base Score: Impressions Tier

| Tier | Impressions | Base Score |
|------|-------------|------------|
| Viral | 15,000+ | 8 |
| Strong | 3,000-15,000 | 7 |
| Good | 1,500-3,000 | 6 |
| Standard | 800-1,500 | 5 |
| Underperforming | Below 800 | 3 |

### Adjustments (add or subtract from base)

**Add points:**
- Seniority (expanded formula — see Section 6) above 60%: +0.5
- Seniority (expanded formula) above 70%: +1.0
- Named senior reactor (MD, CEO, Route Director, Minister): +0.5 each, max +1.5
- Substantive comment from operator or decision-maker: +0.5 each, max +1.0
- New sector opened (new industry category at 5%+): +0.5
- Client company appeared in demographics: +0.5
- Record metric achieved (NR reach, Brussels, new geography): +0.5
- Quoted source approved post by reacting: +0.5
- Post is part of a successful multi-post arc: +0.5

**Subtract points:**
- Paraphrase qualifier used: -1.0
- No engagement question: -0.5
- Bullet points in body: -0.5
- Em dash used: -0.5
- Corporate amplification (repost of colleague/company content): -1.5
- Recruitment content amplified: automatic 2/10 regardless of other factors
- Posted Friday afternoon or weekend: -0.5
- Two posts on same day (second post): -0.5

**Note on historical scores:** Posts documented before April 2026 used the old seniority formula (Senior + Director + VP only). Posts from April 2026 onwards use the expanded formula (see Section 6). Historical scores are not retroactively changed but should be interpreted as using the old formula — actual seniority quality for those posts was higher than the % figure suggests.

### Score Interpretation

| Score | Meaning |
|-------|---------| 
| 10/10 | Perfect: viral + complete engagement stack + strategic targeting |
| 9/10 | Excellent: strong impressions + senior engagement + lessons confirmed |
| 8-8.5/10 | Very good: solid performance + quality audience + strategic value |
| 7-7.5/10 | Good: on-target with minor weaknesses or circumstantial constraints |
| 6-6.5/10 | Acceptable: content quality sound but execution or timing limited it |
| Below 6 | Underperforming: identify the specific failure and document it |

---

## Section 6: Demographic Interpretation Rules

### Seniority Calculation

**EXPANDED FORMULA (effective April 2026):**

**Always use:** Senior % + Director % + VP % + CXO % + Partner % + Owner %

LinkedIn now provides a more granular seniority breakdown. All decision-maker levels must be included in the seniority total. Never exclude CXO, Partner, or Owner — these categories contain people with significant budget authority and commissioning influence.

**Why the expansion matters:**
- CXO includes CEOs, CTOs, CDOs, CFOs — the most senior commissioning layer
- Partner includes consulting partners and equity partners at advisory firms — key influencers in procurement
- Owner includes SME founders and proprietors — not enterprise targets but signals breadth
- The old formula (Senior + Director + VP only) systematically understated real seniority quality by 7-12 percentage points depending on post type

**Targets by post type (expanded formula):**
- Thought leadership / precision posts: 68-75%
- Technical standards posts: 62-68% (engineers pull Entry level up, acceptable)
- Viral awareness posts: 62-68% (broad reach dilutes seniority, acceptable)
- Corporate amplification posts: typically 38-52% (algorithm deprioritises)

**Benchmarks for the scoring adjustments in Section 5:**
- Above 60% (expanded) = above the minimum threshold: +0.5
- Above 70% (expanded) = excellent quality audience: +1.0

### Network Rail Reach Benchmarks

| NR % | Assessment |
|------|-----------|
| 2-4% | Normal |
| 5-7% | Good targeting |
| 7-9% | Excellent |
| 9%+ | Exceptional - record-level |

Current record by percentage: ~10% (Railway Within Railway, January 2026)
Current record by absolute viewers: ~2,145 (Helpston/Override Drift, March 2026 — 4.2% of 51K)

### Geographic Signals

| Geography | What it signals |
|-----------|----------------|
| Brussels 2%+ | EU policy audience reached - significant for UK-EU rail content |
| Glasgow 3%+ | Scotland rail community engaged - useful for NR Scotland / ScotRail content |
| Netherlands 5%+ | NS (Nederlandse Spoorwegen) territory - relevant for fleet content |
| Amsterdam + Rotterdam combined 10%+ | Direct NS audience reach |
| London 25%+ | Announcement or commuter content resonating with London hub |
| Manchester 3%+ | Northern England/Bee Network audience — relevant for TfGM/GMCA content |

### Industry Category Notes

- "Truck Transportation" = rail industry (LinkedIn taxonomy error - rail companies miscategorised)
- "Rail Transportation" = pure rail companies correctly categorised
- Combined Truck Transportation + Rail Transportation = total rail audience
- Airlines and Aviation appearing at 5%+ = airport/aviation sector channel opened
- Civil Engineering appearing at 5%+ = infrastructure community reached
- Public Relations and Communications Services at 5%+ = public affairs and lobbying community engaged (first confirmed at Post 27, March 2026)
- Government Relations Services at 2%+ = policy lobbying community — useful signal for GBR and regulatory content

### Company Size Signals

- 10,001+ at 30%+ = enterprise decision-makers dominant (good)
- 1-50 employees at 20%+ = small consultancies and independents dominant (weaker for BD)

---

## Section 7: Quotable Insights Database - Tier Definitions

### Platinum Tier
Criteria: Visceral, specific, operational. Could open a viral post immediately. From a named practitioner in a senior role at a recognisable organisation. Captures a problem in a way that makes the reader nod and say "that's exactly it."

Current Platinum quotes are in the addendum. Add new ones only when all criteria are clearly met.

### Gold Tier
Criteria: Strong authority (Minister, MD, COO, CEO, Chief Engineer). Clearly attributable. Directly relevant to orchestration, GBR, digital rail, or cross-sector coordination themes. Could open a 3,000+ impression post.

### Silver Tier
Criteria: Good supporting evidence. May not be strong enough to open a post alone but works as validation or supporting quote within the body. Includes practitioner comments that extended an argument usefully.

### Pending Tier (not in addendum, track separately)
Insights heard in conversation that haven't yet been confirmed as quotable or permission hasn't been granted.

---

## Section 8: Strategic Contacts Protocol

### Engagement Level Definitions

| Level | Definition |
|-------|-----------| 
| Intellectual partnership | 4+ engagements, escalating substance, contributing frameworks or new intelligence |
| Active relationship | 2-3 engagements, substantive comments, mutual awareness established |
| Monitoring | 1 engagement (reaction or comment), potential noted |
| Pending | Tagged or messaged, awaiting response |

### Relationship Between the Addendum Contacts Table and the Network File

These are two different layers of the same network:

- **Addendum Strategic Contacts table** (`02-performance-analysis/linkedin-knowledge-base-addendum-january-2026.md`): Active engagers only. People who have reacted, commented, or been messaged. Tracked by engagement count and status. This is the action layer.
- **Network contacts reference** (`05-network/network-contacts-reference.md`): The full passive audience. Warm inbound contacts who connected after posts but have never spoken. Sector-grouped with post trigger identification and CRM-ready CSV. This is the intelligence layer.

When a warm inbound contact (◆ in the network file) engages publicly for the first time, promote them: add to the addendum Strategic Contacts table as Monitoring, and update their row in the network file from ◆ to ★.

### When to Update Contact Status

Update the Strategic Contacts table (addendum) when:
- A contact engages for the first time (add as Monitoring)
- A contact's engagement count increases (update count)
- A contact moves from reaction to substantive comment (note the escalation)
- A DM conversation has been initiated (note in Status column)
- A contact has been converted to a business conversation (flag separately)

Update the network contacts reference when:
- New connections are added (add to appropriate sector table and CSV)
- A warm inbound contact is promoted to active strategic contact (change ◆ to ★)
- A post trigger is identified for an existing connection

### Priority Actions to Track

Always note in the post analysis and addendum if any of these are pending:
- Leon Kong DM follow-up (standing priority until resolved)
- Any quoted source who hasn't responded to their tag within 24 hours
- Rail press profile views that could become editorial pitches

---

## Section 9: The Planted Quote Pattern

This is an advanced technique proven by the Heathrow announcement post (February 24, 2026).

**When to use:** When a major announcement (contract win, product launch, industry event) is imminent but not yet public.

**How it works:**
1. In an earlier post (1-4 weeks before announcement), include a quote that will be relevant to the upcoming announcement - but do not make the connection explicit
2. On announcement day, open with "I didn't mention it at the time but..."
3. Complete the connection between the planted quote and the announcement

**Requirements:**
- The planted quote must be genuine and stand alone in the earlier post (not feel like setup)
- The gap must be 1-4 weeks (too short = feels staged, too long = readers forgot)
- The announcement must be genuinely significant (not every press release justifies this)
- The "didn't mention it at the time" line must appear early in the announcement post

**Proven example:** Heidi Alexander "airspace above Heathrow" quote planted in George Bradshaw Address post (Feb 17), activated in Heathrow announcement post (Feb 24).

---

## Section 10: Post Timing and Sequencing Rules

- **Optimal posting window:** Tuesday-Thursday, 7-9am GMT
- **Never post twice on the same day by choice**
- **Never post on Sunday** — confirmed ceiling regardless of content quality (Underground/Solar, March 2026: 953 impressions despite 64.1% seniority)
- **If forced to post twice on the same day:** first post always wins the engagement race; put the strategically more important content first
- **Minimum gap between posts:** 48 hours recommended, 24 hours absolute minimum
- **Series posts:** space 5-7 days apart to maintain momentum without diluting each post

---

## Section 11: Common Failure Modes (Check Before Every Post)

| Failure | Symptom | Fix |
|---------|---------|-----|
| Paraphrase penalty | "I paraphrase", "not exact words" | Use direct quote or full anonymisation |
| Corporate preamble | Post opens with "Proud to..." | Lead with insight, put context second |
| Closed ending | Post ends with statement or thanks | Add engagement question as final line |
| Algorithm split | Two posts same day | Never post twice by choice |
| Sunday posting | Posted on Sunday | Never post Sunday — no distribution window |
| Friday ceiling | Precision content posted Friday | Never post precision content on Friday |
| Recruitment amplification | Resharing colleague job ad | Never. Score: 2/10 automatic |
| Bullet points | List items with - or bullet | Rewrite in prose |
| Em dash | — character anywhere | Comma, colon, or rephrase |
| Too many hashtags | 5+ hashtags | Maximum 4, all specific |
| No visual | Text-only post | Add photo, chart, or relevant image |
| Vague attribution | "A stakeholder said..." | Name + title + company, or full anonymisation |
| ABM miss | Target organisation absent from demographics | Check if post framing was too generic; named operator/geography content needed |

---

## Quick Reference: Before Posting Checklist

- [ ] Opens with borrowed credibility quote or strong scenario hook (not corporate preamble)?
- [ ] No "I paraphrase" or equivalent qualifier?
- [ ] No em dashes?
- [ ] No bullet points in body?
- [ ] Contains 2+ specific numbers or operational details?
- [ ] States the orchestration insight (coordination not technology)?
- [ ] Visual included?
- [ ] Maximum 4 hashtags, all specific?
- [ ] Named people @ tagged in body text?
- [ ] Ends with engagement question?
- [ ] Posting Tuesday-Thursday 7-9am GMT?
- [ ] Not the second post today?
- [ ] Not Sunday?

---

## Quick Reference: After Posting Checklist

- [ ] Monitor first 2 hours, reply to any comments within 5 minutes
- [ ] If no engagement after 30 minutes, post self-comment with additional context
- [ ] DM anyone @ tagged who hasn't engaged after 1 hour
- [ ] Check analytics at 24 hours (not before)
- [ ] Document in GitHub within 48 hours of posting (individual file + addendum + `_CURRENT-RANKINGS.md`)
- [ ] Note any pending follow-up actions (DMs, replies, pitch opportunities)
- [ ] If new connections came in after post, check against network contacts reference and add warm inbound entries

---

*Skill version: 1.3*
*Created: February 25, 2026*
*Updated: March 20, 2026 — added `_CURRENT-RANKINGS.md` to Step 0 and file creation sequence (Section 3.2); added Section 3.5 (`_CURRENT-RANKINGS.md` update protocol); added three-layer documentation model to Step 1; added Sunday posting to failure modes and Before Posting checklist.*
*Updated: April 3, 2026 — SENIORITY FORMULA EXPANDED. Section 6 updated: seniority calculation now includes Senior + Director + VP + CXO + Partner + Owner. Section 5 scoring thresholds updated accordingly (above 60% = +0.5; above 70% = +1.0 under expanded formula). Historical posts scored under old formula (Senior + Director + VP only) — scores not retroactively changed. New industry signals added: Public Relations and Communications Services, Government Relations Services. ABM miss added to failure modes. Scenario hook added to opening hook options.*
*Based on: 27+ posts documented, 17+ months of performance data*
*Maintainer: Update this file when new absolute rules are confirmed or major new patterns are validated*
