# Measurement: value, quality, cost and responsibility

An attractive response does not prove the business saved time or money. Measure real outcomes, human corrections and the actual cost of the completed process.

```mermaid
flowchart TB
  PILOT[Supervised pilot] --> COUNT[Count all requests]
  COUNT --> SUCCESS[Verified successful completions]
  COUNT --> FAILED[Failures and unresolved requests]
  COUNT --> HUMAN[Human review and corrections]
  COUNT --> MEDIA[Model, voice, document and video charges]
  COUNT --> PLAT[Platform and connection charges]
  COUNT --> QUALITY[Customer and staff feedback]
  SUCCESS & FAILED & HUMAN & MEDIA & PLAT & QUALITY --> METRIC[Cost and quality dashboard]
  METRIC --> DECIDE{Owner review}
  DECIDE -->|Strong results| MORE[Expand carefully]
  DECIDE -->|Weak quality| FIX[Improve evidence, rules, tests]
  DECIDE -->|Too costly| SIMPLIFY[Use fewer steps or different tools]
  DECIDE -->|Unacceptable risk| STOP[Pause or retire]
```

## Weekly management review

```mermaid
flowchart LR
  CASES[(Cases and tasks)] --> EXCEPT[Review exceptions]
  TOOL[(Tool activity and receipts)] --> ERROR[Investigate failed actions]
  COST[(Costs and usage)] --> SPEND[Compare cost per successful case]
  STAFF[Staff feedback] --> FRIC[Find wasted effort]
  EXCEPT & ERROR & SPEND & FRIC --> OWNER[Weekly owner review]
  OWNER --> FIX[Approve changes]
  FIX --> RETEST[Re-test affected workflows]
  RETEST --> LOG[Record change and decision]
```

**Simple dashboard rule:** show total requests, verified completions, unresolved cases, safety events, staff review minutes and total cost. Ratios alone can hide important changes in the total number of cases.
