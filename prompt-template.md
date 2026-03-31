# Churn Risk Assessment — Prompt Template
### Copy this template, fill in the account data, paste into Claude

---

## How to use this template

1. Open a new Claude conversation
2. Copy the entire block below (from "You are a..." to the end)
3. Fill in every field marked with `[ ]`
4. Paste into Claude and run
5. Log the output in your CRM against the account record

**Time required:** 5–8 minutes to complete the account profile.  
**Output:** Risk tier, root cause analysis, intervention recommendation, 
and urgency level.

---

## The prompt — copy from here:
```
You are a senior Customer Success analyst supporting a B2B EdTech company 
that sells annual learning system licenses to private school networks in Brazil. 
Contracts are annual. Schools cannot switch systems mid-year. The renewal 
campaign runs July–December each year.

Your task is to assess the churn risk of the account described below, 
using the signal framework provided. Produce a structured risk assessment 
the CSM can act on immediately.

---

ACCOUNT PROFILE

Account name: [School or network name]
Segment: [Large network (5+ units) / Mid-size network (2–4 units) / Small independent]
Contract value: BRL [X]k per year
Contract term stage: [Year X of Y — e.g. "Year 3 of 3" or "Year 1 of 3"]
Renewal campaign month: [Current month — e.g. "September 2025"]
CSM assigned: [Name and tenure on account — e.g. "Ana, 2 years on account"]

---

SIGNAL SCORES
(Score each signal 0–3 using the definitions below)

CATEGORY 1 — RELATIONSHIP HEALTH

Signal 1 — CSM engagement frequency (Weight: 3)
  0 = Monthly contact, director engaged, CRM updated
  1 = Last contact 6–8 weeks ago
  2 = Last contact 9–12 weeks ago
  3 = No contact 3+ months, emails unanswered
Score: [0 / 1 / 2 / 3]
Context: [One sentence explaining the score — what specifically happened or didn't happen]

Signal 2 — NPS trajectory (Weight: 3)
  0 = NPS ≥ 65, stable or improving
  1 = NPS 50–64, or declined 8–12 pts
  2 = NPS 35–49, or declined 13–19 pts
  3 = NPS < 35, declined 20+ pts, or refused survey
Score: [0 / 1 / 2 / 3]
Context: [NPS score at last measurement, date of measurement, any notable comments]

Signal 3 — EBR completion (Weight: 2)
  0 = EBR held in H1, decision-maker present
  1 = EBR scheduled, not yet held
  2 = EBR attempted, rescheduled twice or more
  3 = No EBR held or attempted
Score: [0 / 1 / 2 / 3]
Context: [When was the last EBR, who attended, what was discussed]

Signal 4 — Complaint volume and resolution (Weight: 2)
  0 = Zero complaints, or resolved within SLA
  1 = 1–2 complaints, resolved satisfactorily
  2 = 3+ complaints, or any unresolved beyond 14 days
  3 = Active escalation open, or explicit dissatisfaction with resolution
Score: [0 / 1 / 2 / 3]
Context: [Nature of complaints if any, current resolution status]

CATEGORY 2 — PRODUCT ADOPTION

Signal 5 — Platform login frequency (Weight: 2)
  0 = Within 20% of expected baseline
  1 = 20–40% below expected baseline
  2 = 40–60% below expected baseline
  3 = >60% below baseline or zero logins in 30 days
Score: [0 / 1 / 2 / 3]
Context: [Actual login frequency vs. expected, academic calendar context]

Signal 6 — Content delivery rate (Weight: 2)
  0 = ≥ 90% of expected curriculum pace
  1 = 75–89% of expected pace
  2 = 60–74% of expected pace
  3 = < 60% of expected pace
Score: [0 / 1 / 2 / 3]
Context: [YTD delivery rate, any known reasons for gaps]

Signal 7 — Teacher training completion (Weight: 1)
  0 = ≥ 80% of teachers trained
  1 = 60–79% trained
  2 = 40–59% trained
  3 = < 40% trained or training declined
Score: [0 / 1 / 2 / 3]
Context: [Training completion rate, last training date, any blockers]

CATEGORY 3 — ORGANISATIONAL STABILITY

Signal 8 — Key contact turnover (Weight: 3)
  0 = No changes, relationships stable
  1 = Coordinator-level change, new contact onboarded
  2 = Pedagogical director change, relationship not yet established
  3 = Owner / CEO / CFO / superintendent change, no exec relationship built
Score: [0 / 1 / 2 / 3]
Context: [Who changed, when, current relationship status with new contact]

Signal 9 — School financial stability (Weight: 2)
  0 = No stress indicators, payments on time
  1 = One late payment in past 12 months, resolved
  2 = Two+ late payments or pricing concerns raised
  3 = Active default, budget cuts announced, or closure risk
Score: [0 / 1 / 2 / 3]
Context: [Payment history, any budget conversations, external financial signals]

Signal 10 — Contract term stage (Weight: 2)
  0 = 2+ years remaining on contract
  1 = Exactly 2 years remaining
  2 = Final year of contract term
  3 = Final year AND one or more other signals active at score ≥ 2
Score: [0 / 1 / 2 / 3]
Context: [Contract start date, end date, total term length]

CATEGORY 4 — COMMERCIAL SIGNALS

Signal 11 — Competitor activity (Weight: 2)
  0 = No competitor activity detected
  1 = Competitor outreach mentioned casually
  2 = Competitor demo or proposal known to have been received
  3 = School in active competitive evaluation
Score: [0 / 1 / 2 / 3]
Context: [Which competitor if known, stage of their engagement, school's stance]

Signal 12 — Renewal conversation initiation (Weight: 3)
  0 = School engaged proactively, terms under discussion
  1 = First conversation held, school receptive
  2 = Conversation deferred multiple times by school
  3 = No engagement despite outreach, or "still deciding" after October
Score: [0 / 1 / 2 / 3]
Context: [Date of last renewal conversation, school's stated position, 
any objections raised]

---

CALCULATED RISK SCORE

Total weighted score: 
[Calculate as: (S1×3)+(S2×3)+(S3×2)+(S4×2)+(S5×2)+(S6×2)+(S7×1)+(S8×3)+(S9×2)+(S10×2)+(S11×2)+(S12×3)]
[Maximum possible: 72 points]

---

ADDITIONAL CONTEXT

[Add any relevant information not captured by the signals above:
- Key upcoming events (board meeting, school anniversary, local elections)
- Recent positive developments that might offset risk signals
- CSM's overall intuition on the account
- History with this account in prior renewal cycles]

---

ASSESSMENT REQUEST

Based on the signal profile above, please provide:

1. RISK TIER
State the tier (Red / Amber / Green) and the total weighted score. 
Confirm whether the score aligns with the tier thresholds:
Red = 35–72 | Amber = 18–34 | Green = 0–17

2. PRIMARY RISK DRIVERS
Identify the 2–3 signals contributing most to the risk score. 
For each, explain why it matters in the context of this specific account — 
not just what the signal means in general.

3. INTERVENTION RECOMMENDATION
Provide a specific, time-bound action plan for the CSM. 
Include: what to do, who should be involved, in what sequence, 
and by when. Match the urgency to the risk tier.
Red = actions within 48 hours, executive involvement required.
Amber = actions within 7 days, CSM-led recovery plan.
Green = maintain cadence, identify expansion opportunity.

4. ESCALATION DECISION
State clearly: does this account require escalation to CS leadership? 
Yes or No, with one sentence of reasoning.

5. WATCH LIST
Name 1–2 specific events or signals in the next 30 days that would 
materially change the risk assessment — either upgrading or downgrading 
the tier.

---

Tone: Direct. Write for a CSM who has 3 minutes to read this and needs 
to know exactly what to do next. No hedging, no generic advice.
```

---

## Example of a completed profile (for reference)

Below is an example of what a filled-in prompt looks like before pasting 
into Claude. Use this to calibrate the level of detail expected in each 
context field.
```
Account name: Rede Norte Educação (4 units)
Segment: Large network
Contract value: BRL 890k per year
Contract term stage: Year 3 of 3
Renewal campaign month: October 2025
CSM assigned: Diego, 8 months on account

Signal 1 — CSM engagement frequency
Score: 3
Context: Last substantive contact with pedagogical director was 14 weeks 
ago. Three follow-up emails sent in September, none answered. Diego 
escalated to his manager in late September but no action was taken.

Signal 2 — NPS trajectory
Score: 2
Context: NPS was 58 at mid-year (Jun 2025), down from 71 at year-end 2024. 
Decline driven by coordinator complaints about platform stability in Q1. 
Recovery plan was discussed but never formally assigned to an owner.

Signal 3 — EBR completion
Score: 3
Context: No EBR has been held in 2025. Two attempts were made — March 
and June — both declined by the school. No exec-level engagement has 
occurred since the new superintendent joined in September.

Signal 4 — Complaint volume and resolution
Score: 2
Context: Four complaints logged in Q1 related to platform sync issues. 
All resolved technically, but no satisfaction confirmation was obtained 
from the school. One complaint was open for 19 days before resolution.

Signal 5 — Platform login frequency
Score: 1
Context: Coordinator logins are 30% below expected baseline for October. 
Likely partially explained by the superintendent transition — new 
coordinators still being onboarded.

Signal 6 — Content delivery rate
Score: 1
Context: YTD delivery at 81% of expected pace. Below target but within 
manageable range given the organisational disruption.

Signal 7 — Teacher training completion
Score: 1
Context: 68% of teachers have completed the annual training. Below target 
but not critical given the network size and transition context.

Signal 8 — Key contact turnover
Score: 3
Context: New superintendent appointed September 2025. Previous 
superintendent was a strong advocate — had been with the network 11 years. 
New superintendent has not responded to any outreach from CS or commercial 
leadership. Their background is financial, not pedagogical.

Signal 9 — School financial stability
Score: 1
Context: One late payment in August, resolved within 10 days. No further 
payment issues. No budget cut announcements observed.

Signal 10 — Contract term stage
Score: 3
Context: This is year 3 of a 3-year contract — final year. Combined with 
Signal 8 (score 3) and Signal 1 (score 3), this compounds the risk 
significantly. No renewal conversation has been initiated.

Signal 11 — Competitor activity
Score: 2
Context: A competitor (Positivo) is known to have presented to the network 
in August. Source: former coordinator now working at another Arco client. 
No formal proposal confirmed but meeting took place.

Signal 12 — Renewal conversation initiation
Score: 3
Context: No renewal conversation has been initiated. Diego attempted to 
raise renewal in his last call (August) but was told to "wait until things 
settle with the new superintendent." It is now October and there has been 
no follow-up from the school.

Total weighted score: (3×3)+(2×3)+(3×2)+(2×2)+(1×2)+(1×2)+(1×1)+(3×3)+(1×2)+(3×2)+(2×2)+(3×3) = 62

Additional context: This account was the company's longest-tenured client in the 
Northeast region. The previous superintendent was a personal reference for 
two new client acquisitions. Losing this account would have reputational 
implications beyond the contract value. The commercial leadership team is 
aware of the risk but has not yet engaged directly.
