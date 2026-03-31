# Churn Signal Definitions
### 12 observable pre-churn signals for annual-contract EdTech businesses

---

## How signals are weighted

Each signal is scored **0–3** at account review:
- **0** = Signal absent. No cause for concern.
- **1** = Signal emerging. Worth monitoring.
- **2** = Signal active. Requires proactive response.
- **3** = Signal critical. Escalation likely required.

Each signal carries a **weight (1–3)** reflecting its historical correlation 
with confirmed churn. A signal with weight 3 that scores 3 contributes 9 points 
to the total risk score. Maximum possible score: **72 points.**

**Risk tier thresholds:**
| Tier | Score range | Meaning |
|---|---|---|
| 🔴 Red | 35–72 | High churn probability. Immediate intervention. |
| 🟡 Amber | 18–34 | Moderate risk. Proactive recovery plan needed. |
| 🟢 Green | 0–17 | Low risk. Maintain standard cadence. |

---

## Category 1 — Relationship health
*Tracks the quality and frequency of engagement between the school and the CS team.*

---

### Signal 1 — CSM engagement frequency
**Weight: 3** (strongest predictor of churn across all segments)

**Definition:** How frequently is the CSM holding substantive conversations 
with the school's pedagogical director or decision-maker?

| Score | Threshold |
|---|---|
| 0 | Monthly check-in held. Director engaged. Notes logged in CRM. |
| 1 | Last substantive contact was 6–8 weeks ago. |
| 2 | Last substantive contact was 9–12 weeks ago. |
| 3 | No substantive contact in 3+ months. Emails unanswered. |

**Data source:** CRM activity log  
**Review frequency:** Weekly  
**Time-to-churn correlation:** Accounts scoring 3 on this signal in Q2 
churned at 4.2× the base rate in the same renewal cycle.

---

### Signal 2 — NPS trajectory
**Weight: 3**

**Definition:** Direction of NPS movement between the mid-year and year-end 
measurement, and deviation from the healthy benchmark of 70.

| Score | Threshold |
|---|---|
| 0 | NPS ≥ 65, stable or improving vs. prior measurement. |
| 1 | NPS 50–64, or declined 8–12 pts vs. prior measurement. |
| 2 | NPS 35–49, or declined 13–19 pts vs. prior measurement. |
| 3 | NPS < 35, or declined 20+ pts. Or: refused to participate in NPS survey. |

**Data source:** NPS survey platform (measured twice per year: Jun and Dec)  
**Review frequency:** At each measurement point  
**Benchmark:** A healthy account in this segment scores 65–75. Scores below 
50 indicate meaningful dissatisfaction and require a structured recovery 
conversation before the renewal window opens. A refusal to participate 
in the NPS survey should be treated as a score of 3 regardless of prior 
history — disengagement from feedback mechanisms is a strong churn precursor.

---

### Signal 3 — Executive Business Review (EBR) completion
**Weight: 2**

**Definition:** Whether the annual EBR has been held with the school's 
senior decision-maker (owner, CEO, or superintendent).

| Score | Threshold |
|---|---|
| 0 | EBR held in H1. Decision-maker present. Action items agreed. |
| 1 | EBR scheduled but not yet held (acceptable if pre-July). |
| 2 | EBR attempted but rescheduled twice or more. |
| 3 | No EBR held or attempted. Decision-maker never engaged at exec level. |

**Data source:** CRM meeting log  
**Review frequency:** Monthly (Jun–Dec)  
**Note:** The absence of an EBR is particularly high-risk for large network 
accounts (5+ units) where the renewal decision is made at board or CFO level, 
not by the pedagogical coordinator.

---

### Signal 4 — Complaint volume and resolution time
**Weight: 2**

**Definition:** Number of formal complaints or escalations raised by the 
school in the past 90 days, and whether they were resolved satisfactorily.

| Score | Threshold |
|---|---|
| 0 | Zero complaints in past 90 days, or complaints resolved within SLA. |
| 1 | 1–2 complaints, resolved within SLA with satisfaction confirmed. |
| 2 | 3+ complaints, or any complaint unresolved beyond 14 days. |
| 3 | Active escalation open, or school explicitly expressed dissatisfaction 
with resolution quality. |

**Data source:** Support ticketing system, CSM notes  
**Review frequency:** Weekly  

---

## Category 2 — Product adoption
*Tracks how actively the school is using the learning system.*

---

### Signal 5 — Platform login frequency (coordinators)
**Weight: 2**

**Definition:** How frequently school coordinators are logging into the 
platform relative to the expected usage pattern for this point in the 
academic year.

| Score | Threshold |
|---|---|
| 0 | Login frequency within 20% of expected baseline for academic period. |
| 1 | Login frequency 20–40% below expected baseline. |
| 2 | Login frequency 40–60% below expected baseline. |
| 3 | Login frequency >60% below baseline, or zero logins in past 30 days. |

**Data source:** Platform usage analytics  
**Review frequency:** Monthly  
**Note:** Usage naturally drops during school holidays and exam periods. 
Normalise against the academic calendar before scoring. A July drop 
during recess is not a signal. A July drop during active term is.

---

### Signal 6 — Content delivery rate
**Weight: 2**

**Definition:** What percentage of the contracted curriculum content has 
been delivered to students year-to-date, relative to the expected delivery 
pace at this point in the academic year.

| Score | Threshold |
|---|---|
| 0 | Content delivery ≥ 90% of expected pace. |
| 1 | Content delivery 75–89% of expected pace. |
| 2 | Content delivery 60–74% of expected pace. |
| 3 | Content delivery < 60% of expected pace, or school has explicitly 
stopped using curriculum materials. |

**Data source:** Platform delivery analytics  
**Review frequency:** Monthly  

---

### Signal 7 — Teacher training completion
**Weight: 1**

**Definition:** Percentage of the school's teachers who have completed 
the annual training programme for the learning system.

| Score | Threshold |
|---|---|
| 0 | ≥ 80% of teachers trained. |
| 1 | 60–79% of teachers trained. |
| 2 | 40–59% of teachers trained. |
| 3 | < 40% of teachers trained, or school declined training offer. |

**Data source:** Training platform completion records  
**Review frequency:** Quarterly (key checkpoints: Mar, Jul, Oct)  
**Note:** Low teacher training completion is a leading indicator of low 
content delivery (Signal 6). Address training gaps before they cascade 
into adoption failures.

---

## Category 3 — Organisational stability
*Tracks leadership and structural changes at the school that affect the renewal decision.*

---

### Signal 8 — Key contact turnover
**Weight: 3**

**Definition:** Whether the primary CS contact (pedagogical director or 
coordinator) or the budget decision-maker (owner, CEO, CFO) has changed 
in the past 6 months.

| Score | Threshold |
|---|---|
| 0 | No changes in key contacts. Relationships stable. |
| 1 | Coordinator-level change. New contact introduced and onboarded. |
| 2 | Pedagogical director change. Relationship with new director 
not yet established. |
| 3 | Owner, CEO, CFO, or superintendent change. No executive 
relationship with new decision-maker. |

**Data source:** CSM notes, LinkedIn monitoring, school communications  
**Review frequency:** Monthly  
**Critical rule:** Any score of 3 on this signal must trigger an 
immediate escalation to CS leadership for executive outreach. 
Leadership transitions are the single highest-risk event in the 
renewal cycle. The window to establish a relationship with the 
new decision-maker closes fast.

---

### Signal 9 — School financial stability
**Weight: 2**

**Definition:** Observable indicators of financial stress at the school 
that could affect their ability or willingness to renew at current pricing.

| Score | Threshold |
|---|---|
| 0 | No financial stress indicators. Payments on time. |
| 1 | One late payment in past 12 months, subsequently resolved. |
| 2 | Two or more late payments, or school raised pricing concerns 
in conversation. |
| 3 | Active payment default, school announced budget cuts, 
or credible risk of closure. |

**Data source:** Finance/AR system, CSM notes  
**Review frequency:** Monthly  

---

### Signal 10 — Contract term stage
**Weight: 2**

**Definition:** Where the account sits in its multi-year contract cycle. 
Accounts in the final year of their contracted term face a full renewal 
decision — including competitive evaluation and budget reapproval — rather 
than a straightforward rollover. This structurally elevates churn risk 
independent of relationship health.

| Score | Threshold |
|---|---|
| 0 | Contract has 2+ years remaining. Renewal is not an active decision. |
| 1 | Contract has exactly 2 years remaining. Renewal conversation 
is on the horizon — begin relationship-deepening activities. |
| 2 | Contract is in its final year. Full renewal decision required. 
Budget reapproval and potential competitive evaluation likely. |
| 3 | Contract is in its final year AND one or more other risk signals 
are active (score ≥ 2 on any other signal). Compounding risk. |

**Data source:** CRM contract records  
**Review frequency:** Quarterly — flag all accounts entering final 
contract year at the start of each quarter  
**Strategic note:** Accounts entering their final contract year should 
be identified at the start of the preceding year and assigned a proactive 
deepening plan — not treated as standard renewals. The goal is to reach 
the renewal window with the relationship already reinforced, competitive 
alternatives pre-empted, and ROI evidence documented. A final-year account 
that enters the Jul–Dec campaign without prior executive engagement is 
already at elevated risk regardless of other signals.  

---

## Category 4 — Commercial signals
*Tracks financial and competitive indicators of renewal risk.*

---

### Signal 11 — Competitor activity
**Weight: 2**

**Definition:** Evidence that a competitor is actively pursuing the account.

| Score | Threshold |
|---|---|
| 0 | No competitor activity detected. |
| 1 | Competitor outreach reported by school contact (casual mention). |
| 2 | Competitor demo or formal proposal known to have been received. |
| 3 | School is in active evaluation of a competitor. Decision pending. |

**Data source:** CSM notes, school contacts, market intelligence  
**Review frequency:** Monthly  
**Note:** Do not wait for the school to volunteer this information. 
Ask directly in every QBR and renewal conversation: *"Are you evaluating 
any other systems this cycle?"* Competitor activity detected at stage 2 
or 3 requires an immediate counter-engagement plan.

---

### Signal 12 — Renewal conversation initiation
**Weight: 3**

**Definition:** Whether the school has engaged constructively in the 
renewal conversation, given where we are in the campaign calendar 
(Jul–Dec window).

| Score | Threshold |
|---|---|
| 0 | School has engaged proactively. Renewal terms under discussion 
or already agreed. |
| 1 | First renewal conversation held. School receptive but 
decision not yet initiated. |
| 2 | Renewal conversation attempted but deferred by school 
("let's talk in October," etc.). Multiple deferral attempts. |
| 3 | School has not engaged with renewal conversation despite 
CSM outreach, or has explicitly indicated they are "still deciding." 
After October, any score of 2+ should be treated as 3. |

**Data source:** CRM opportunity stage, CSM notes  
**Review frequency:** Weekly (Aug–Dec)  
**Calendar note:** The urgency of this signal scales with time. 
A score of 2 in August is manageable. A score of 2 in November 
is critical. Apply a +1 modifier to this signal's score for 
any account reviewed after 1 November.

---

## Signal summary table

| # | Signal | Category | Weight | Max contribution |
|---|---|---|---|---|
| 1 | CSM engagement frequency | Relationship health | 3 | 9 pts |
| 2 | NPS trajectory | Relationship health | 3 | 9 pts |
| 3 | EBR completion | Relationship health | 2 | 6 pts |
| 4 | Complaint volume & resolution | Relationship health | 2 | 6 pts |
| 5 | Platform login frequency | Product adoption | 2 | 6 pts |
| 6 | Content delivery rate | Product adoption | 2 | 6 pts |
| 7 | Teacher training completion | Product adoption | 1 | 3 pts |
| 8 | Key contact turnover | Organisational stability | 3 | 9 pts |
| 9 | School financial stability | Organisational stability | 2 | 6 pts |
| 10 | Contract term stage | Organisational stability | 2 | 6 pts |
| 11 | Competitor activity | Commercial signals | 2 | 6 pts |
| 12 | Renewal conversation initiation | Commercial signals | 3 | 9 pts |
| | **Total** | | | **72 pts** |

---

## Calibration notes

These weights and thresholds were developed based on operational patterns 
observed across multiple EdTech renewal campaigns. Before deploying at scale:

- **Validate weights against your own churn data.** Run the framework 
  retrospectively on 2–3 prior cycles and compare predicted risk tiers 
  to actual churn outcomes. Adjust weights where the model systematically 
  under- or over-predicts.
- **Segment if needed.** Large network accounts (5+ units) and small 
  independents behave differently. Signal 8 (key contact turnover) and 
  Signal 12 (renewal conversation) are more predictive for large networks. 
  Signals 9 and 10 (financial and enrolment) are more predictive for 
  small independents.
- **Do not over-automate.** This framework is a CSM decision-support tool, 
  not an automated scoring system. CSM judgment on account context should 
  always be able to override a model output with documented reasoning.
