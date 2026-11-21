# Large end-to-end illustrations

These are deliberately wide diagrams. Open this file on GitHub and expand the diagram area or use the repository's source view if your screen is small. Every illustration is text-based Mermaid, so there are no image files to maintain.

## One company, many incoming channels, one controlled task system

```mermaid
flowchart LR
 subgraph PEOPLE[Incoming requests]
 C1[Website chat]
 C2[Shared email]
 C3[Voice notes and calls]
 C4[Photographs and scans]
 C5[Internal staff forms]
 end
 subgraph INTAKE[Understand and register]
 T1[Read and classify text]
 T2[Transcribe spoken requests]
 T3[Extract image or document details]
 T4[Create task ID, source and priority]
 end
 subgraph TEAM[Specialists]
 S1[Sales and quotations]
 S2[Customer service]
 S3[Finance document review]
 S4[Operations and delivery]
 S5[Research and reporting]
 end
 subgraph RECORDS[Trusted business records]
 D1[(Catalog and inventory)]
 D2[(CRM and orders)]
 D3[(Calendar and tasks)]
 D4[(Approved policies)]
 end
 subgraph CONTROL[Check and close]
 P1[Check facts and missing items]
 P2{Restricted action?}
 P3[Named human approval]
 P4[Connected app action]
 P5[Verify action receipt]
 P6[(Task history and management review)]
 end
 C1 --> T1
 C2 --> T1
 C3 --> T2
 C4 --> T3
 C5 --> T1
 T1 --> T4
 T2 --> T4
 T3 --> T4
 T4 --> S1
 T4 --> S2
 T4 --> S3
 T4 --> S4
 T4 --> S5
 S1 <--> D1
 S2 <--> D2
 S3 <--> D4
 S4 <--> D3
 S5 <--> D4
 S1 --> P1
 S2 --> P1
 S3 --> P1
 S4 --> P1
 S5 --> P1
 P1 --> P2
 P2 -->|yes| P3
 P2 -->|no| P4
 P3 -->|approved| P4
 P3 -->|rejected| P6
 P4 --> P5
 P5 --> P6
```

The arrows show responsibility and information flow; an actual deployment will require specific working integrations. Checking the output may involve opening the calendar, CRM or accounting system rather than trusting the assistant's statement.

## The entire journey of a customer quotation

```mermaid
sequenceDiagram
  autonumber
  actor Customer
  participant Inbox as Shared inbox
  participant Intake as Intake coordinator
  participant Sales as Sales specialist
  participant Catalog as Approved catalog
  participant Stock as Live inventory
  participant Review as Human manager
  participant Send as Email service
  participant Tasks as Task register
  Customer->>Inbox: Request quote + photograph
  Inbox->>Intake: Incoming message ID
  Intake->>Tasks: Create quotation task
  Intake->>Sales: Product request and source
  Sales->>Catalog: Search approved product and price
  Catalog-->>Sales: Current product and price reference
  Sales->>Stock: Check available quantity
  Stock-->>Sales: Verified stock result or error
  alt Information missing or ambiguous
   Sales->>Tasks: Mark waiting for facts
   Sales-->>Customer: Request clarification through approved route
  else Verified draft ready
   Sales->>Review: Draft with item, price and terms
   alt Manager rejects
    Review->>Tasks: Reason and revision request
   else Manager approves
    Review->>Send: Send approved text to verified recipient
    Send-->>Tasks: Send receipt or failure
    Tasks-->>Customer: Follow-up if needed
   end
  end
```

## What an MCP connection should and should not be allowed to do

```mermaid
flowchart TB
 subgraph REQUEST[Business owner's request]
 A[Find tomorrow's available appointment slots]
 B[Prepare three reminder drafts]
 C[Cancel every team meeting]
 end
 subgraph HOST[Assistant application and permission boundary]
 H[Discover available actions]
 J{Allowed operation and account?}
 K[Require relevant human approval]
 end
 subgraph MCP[Trusted connected service]
 R[Read calendar]
 D[Create reminder draft]
 W[Change/delete calendar event]
 end
 subgraph RESULTS[Verified outcome]
 X[Show sourced availability]
 Y[Show draft only]
 Z[Reject unauthorized change]
 end
 A --> H
 B --> H
 C --> H
 H --> J
 J -->|read allowed| R
 J -->|draft allowed| D
 J -->|restricted| K
 K -->|not approved| Z
 K -->|approved and authorized| W
 R --> X
 D --> Y
 W --> M[Check calendar change receipt]
```

## Month-end results without hiding failures

```mermaid
flowchart TD
 S[(Task records)] --> G[Group by workflow and outcome]
 L[(Action receipts)] --> G
 B[(Platform and model bills)] --> Cost[Calculate actual costs]
 H[(Human review times)] --> Cost
 G --> K{Was the task correctly completed?}
 K -->|yes| Success[Verified successes]
 K -->|no| Failures[Rework and failure log]
 Failures --> Cost
 Success --> Rate[Correct completion rate]
 Cost --> Unit[Cost per correct completion]
 Rate --> Decision{Expand, fix or stop?}
 Unit --> Decision
 Decision -->|Expand| New[One new workflow or channel]
 Decision -->|Fix| Repair[Improve data, steps and permissions]
 Decision -->|Stop| Retire[Return work to staff or standard software]
```

For a narrower view, read the [MCP atlas](02-mcp-expanded.md), [task handoffs](03-task-life-and-handoffs.md), [customer workflows](06-sales-and-service.md), and [cost monitoring](10-cost-and-monitoring.md).
