# Customer journey: inquiry, sale, issue and recovery

A strong customer process remembers the case ID, not just the last message. This prevents customers from repeating the same complaint to several departments.

```mermaid
flowchart TB
  ENTRY[Customer reaches business] --> TYPE{What do they need?}
  TYPE -->|Buy| LEAD[Create or find prospect]
  TYPE -->|Existing order| ORDER[Verify order identity]
  TYPE -->|Complaint| CASE[Create support case]
  TYPE -->|Appointment| CAL[Read calendar]
  LEAD --> PRODUCT[Verify product and current price]
  PRODUCT --> QUOTE[Prepare quotation]
  QUOTE --> APPROVE[Commercial approval if needed]
  APPROVE --> SEND[Send verified quotation]
  SEND --> FOLLOW[Planned follow-up]
  ORDER --> TRACK[Check actual order status]
  TRACK --> ANSWER[Explain verified status]
  CASE --> POLICY[Find applicable support policy]
  POLICY --> EVIDENCE[Gather photos, transaction or receipt]
  EVIDENCE --> RESOLVE{Routine solution possible?}
  RESOLVE -->|Yes| DRAFT[Prepare response]
  RESOLVE -->|No| HUMAN[Specialist investigation]
  CAL --> SLOT[Offer real availability]
  SLOT --> BOOK[Authorized booking]
  FOLLOW & ANSWER & DRAFT & HUMAN & BOOK --> LOG[Update customer and task record]
```

## Customer-service escalation

```mermaid
sequenceDiagram
  autonumber
  actor Customer
  participant Service as Front desk
  participant Records as Business records
  participant Staff as Human specialist
  Customer->>Service: My order was delivered damaged
  Service->>Records: Find matching order using permitted identifier
  Records-->>Service: Confirmed purchase + relevant policy
  Service->>Customer: Please share a clear photograph if appropriate
  Customer-->>Service: Photo of damage
  Service->>Staff: Case summary, image reference, policy, unanswered questions
  Staff-->>Service: Approved resolution or next step
  Service-->>Customer: Verified next step and case reference
```

The diagram intentionally avoids automatic refunding. Payment and return decisions remain subject to business policy and authority.
