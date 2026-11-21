# Governance: permission checks and failure recovery

The assistant is not the final authority over sensitive actions. The company owns the rules and the external systems must enforce them.

```mermaid
flowchart TB
  INPUT[Request, document or web content] --> CLASS[Determine request and data sensitivity]
  CLASS --> USER[Identify requesting user]
  USER --> NEED[Check job-related need]
  NEED --> TOOLS[Select minimal allowed tool]
  TOOLS --> ACT{What kind of action?}
  ACT -->|Read| READ[Limited read with logging]
  ACT -->|Draft| DRAFT[Create unsent or unpublished draft]
  ACT -->|Write| WRITE[Validate target, scope and recovery]
  ACT -->|External or money| HIGH[Named accountable approval]
  READ --> CHECK[Verify factual output]
  DRAFT --> CHECK
  WRITE --> CHECK
  HIGH --> CHECK
  CHECK --> EXEC[Execute allowed step]
  EXEC --> CONF{Confirmed system result?}
  CONF -->|Yes| CLOSE[Record receipt and close]
  CONF -->|No| PAUSE[Stop and inspect before retry]
```

## Incident handling

```mermaid
flowchart LR
  ALERT[Unexpected action or disclosure] --> STOP[Pause workflow]
  STOP --> REV[Revoke excess access]
  REV --> PRESERVE[Preserve appropriate evidence]
  PRESERVE --> IMPACT[Identify affected people and records]
  IMPACT --> RESTORE[Correct or restore records if authorized]
  RESTORE --> NOTIFY[Assess legal and contractual notification]
  NOTIFY --> ROOT[Fix underlying cause]
  ROOT --> TEST[Run failing and related tests]
  TEST --> SIGN[Manager signs off restart]
```

The incident path may be shorter or longer depending on severity; a privacy breach needs professional response appropriate to the jurisdiction and the data involved.
