# Churn Early-Warning Framework
### An AI-assisted operational protocol for B2B EdTech CS teams

---

## What this is

This framework helps Customer Success teams in annual-contract EdTech businesses 
identify accounts at risk of non-renewal **6–8 weeks before they confirm churn**.

It was designed for businesses where:
- Revenue is recognised on annual contracts per school or institution
- Clients cannot switch systems mid-year (high switching cost once adopted)
- The renewal campaign runs on a fixed seasonal window (e.g. Jul–Dec)
- CS teams manage large portfolios with limited time per account

The framework defines **12 observable pre-churn signals**, weights them by 
predictive strength, and uses Claude (Anthropic's AI) as the diagnostic engine. 
A CSM fills in a structured account profile, pastes it into Claude, and receives 
a risk tier, root cause analysis, and recommended intervention — in under 60 seconds.

---

## The problem it solves

In annual-contract EdTech businesses, churn is almost never a surprise in hindsight. 
The signals are there weeks or months earlier — a coordinator who stops responding, 
an NPS that dropped at mid-year with no follow-up, a new superintendent who was 
never engaged by CS leadership.

The problem is not a lack of signals. It is a lack of systematic attention to them 
across a large portfolio. A CS team managing 80–100 accounts cannot manually track 
12 signals per account in parallel. This framework makes that tractable by:

1. Defining exactly which signals to monitor and at what frequency
2. Giving each signal a weight based on its correlation with eventual churn
3. Providing a single structured prompt that synthesises all signals into 
   a risk assessment and action recommendation

---

## Framework structure

| File | What it contains |
|---|---|
| `signals.md` | 12 churn signals with definitions, weights, thresholds, and data sources |
| `prompt_template.md` | The Claude prompt template a CSM runs for any account |
| `sample_outputs/account_red.md` | Example output for a high-risk (Red) account |
| `sample_outputs/account_amber.md` | Example output for a medium-risk (Amber) account |
| `sample_outputs/account_green.md` | Example output for a healthy (Green) account |

---

## How to use it

**Step 1 — Monitor signals weekly**  
Use `signals.md` as your account review checklist. For each account in your 
portfolio, note the current status of each signal. Flag any that have crossed 
the warning threshold.

**Step 2 — Run the diagnostic for at-risk accounts**  
Open `prompt_template.md`. Fill in the account's data for each of the 12 signals. 
Paste the completed prompt into Claude.

**Step 3 — Act on the output**  
Claude returns a risk tier (Red / Amber / Green), the top risk drivers, a 
recommended intervention, and the urgency level. The CSM owns the action. 
The framework owns the consistency.

**Step 4 — Escalate Red accounts immediately**  
Any account scoring Red should be escalated to CS leadership within 24 hours. 
Do not wait for the next weekly review.

---

## Risk tier definitions

| Tier | Meaning | Required action |
|---|---|---|
| 🔴 Red | High churn probability. Multiple signals active. Intervention urgent. | Escalate to CS lead within 24h. Executive engagement required. |
| 🟡 Amber | Moderate risk. 1–2 signals active. Monitoring and proactive outreach needed. | CSM-led recovery plan within 7 days. Weekly check-in cadence. |
| 🟢 Green | Low risk. No material signals active. Healthy engagement. | Maintain standard cadence. Identify expansion opportunity. |

---

## Signal categories

The 12 signals are organised into 4 categories:

- **Relationship health** — quality and frequency of engagement between the 
  school and the CS team
- **Product adoption** — how actively the school is using the learning system
- **Organisational stability** — leadership and structural changes at the school 
  that affect the renewal decision
- **Commercial signals** — financial and competitive indicators

Full definitions, weights, and thresholds in `signals.md`.

---

## Design principles

**Signals over gut feel.** Every signal in this framework is observable and 
documentable. CSM intuition is valuable — but it does not scale across a 
portfolio of 80+ accounts and cannot be reviewed by a manager. This framework 
makes risk visible and auditable.

**Early is the only time that matters.** A churn intervention at week 2 of 
a 6-week warning window has a materially different success rate than one at 
week 5. The framework is designed to surface risk early enough for the 
intervention to work.

**AI as inference layer, not replacement.** Claude synthesises the signal 
profile and generates the recommendation. The CSM owns the relationship, 
the context, and the execution. The framework is a tool, not a substitute 
for judgment.

---
