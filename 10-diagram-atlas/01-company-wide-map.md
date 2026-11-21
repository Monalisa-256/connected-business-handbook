# Company-wide operating map

This is the widest view of a business using a digital workforce. It shows why a conversation is only the front door; the value comes from records, staff handoffs, authorized actions and completion evidence.

```mermaid
flowchart TB
  subgraph ARRIVAL[1. Work arrives]
    direction LR
    A1[Customer chat]
    A2[Telephone]
    A3[Email]
    A4[Form]
    A5[Invoice PDF]
    A6[Employee request]
    A7[Scheduled report]
  end
  subgraph INTAKE[2. Make it understandable]
    direction LR
    B1[Read text]
    B2[Transcribe audio]
    B3[Inspect image]
    B4[Extract document fields]
    B5[Identify request type]
    B6[Record source and date]
  end
  subgraph TRACK[3. Keep ownership visible]
    T1[Task ID]
    T2[Priority and due date]
    T3[Next owner]
    T4[(Task register)]
  end
  subgraph TEAM[4. Specialist team]
    direction LR
    C1[Service]
    C2[Sales]
    C3[Operations]
    C4[Finance]
    C5[Research]
    C6[Creative]
    C7[Quality review]
  end
  subgraph TRUTH[5. Get verified information]
    direction LR
    D1[(Customer records)]
    D2[(Stock and prices)]
    D3[(Accounting)]
    D4[(Approved policies)]
    D5[(Calendar)]
    D6[(Document library)]
  end
  subgraph CONTROL[6. Decide if action is safe]
    E1[Check evidence]
    E2[Check identity]
    E3[Check permission]
    E4{Human approval needed?}
    E5[Review by accountable person]
  end
  subgraph ACTION[7. Perform and prove]
    direction LR
    F1[Send approved reply]
    F2[Create case]
    F3[Update record]
    F4[Prepare report]
    F5[Record receipt]
    F6[Close or follow up]
  end
  ARRIVAL --> INTAKE --> TRACK --> TEAM
  TRACK --> T4
  TEAM <--> TRUTH
  TEAM --> E1 --> E2 --> E3 --> E4
  E4 -->|Yes| E5 --> ACTION
  E4 -->|No| ACTION
  ACTION --> T4
  T4 --> F6
```

**Owner's takeaway:** every real task needs an owner, a source of truth, permission to act and a record showing what happened. You can begin with one narrow route through this map and grow from there.

## Alternative view: division of responsibility

```mermaid
flowchart LR
  H[Human management] --> M[Work coordinator]
  M --> S[Service lead]
  M --> SALES[Sales lead]
  M --> FIN[Finance analyst]
  M --> OPER[Operations coordinator]
  M --> CRE[Creative desk]
  M --> RES[Research desk]
  S & SALES & FIN & OPER & CRE & RES --> REVIEW[Quality and risk checks]
  REVIEW --> H
  H -->|Approved authority| TOOLS[Approved business systems]
  TOOLS --> RECORD[(Auditable records)]
```
