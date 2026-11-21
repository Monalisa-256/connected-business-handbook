# Task lifecycle and handoffs

This diagram is useful when work is lost between departments. Each state should correspond to a visible record in the task register, with an assigned person or specialist.

```mermaid
stateDiagram-v2
  [*] --> New
  New --> NeedsDetails: Missing request information
  New --> Ready: Request complete
  NeedsDetails --> Ready: Customer or staff replies
  NeedsDetails --> Closed: Request withdrawn
  Ready --> Assigned
  Assigned --> InProgress
  InProgress --> WaitingForSystem: Tool unavailable
  WaitingForSystem --> InProgress: Verified recovery
  WaitingForSystem --> HumanFollowUp: Recovery failed
  InProgress --> DraftReady: Draft or decision prepared
  DraftReady --> Rework: Review finds error
  Rework --> InProgress
  DraftReady --> WaitingForApproval: Sensitive action
  DraftReady --> Authorized: Routine approved action
  WaitingForApproval --> Authorized: Named approval
  WaitingForApproval --> Closed: Rejected
  WaitingForApproval --> HumanFollowUp: Review overdue
  Authorized --> Executing
  Executing --> VerifyReceipt
  VerifyReceipt --> Completed: Actual result verified
  VerifyReceipt --> WaitingForSystem: Outcome unknown
  Completed --> [*]
  Closed --> [*]
  HumanFollowUp --> [*]
```

## The handoff packet

```mermaid
flowchart TB
  A[Current specialist] --> P[Handoff packet]
  subgraph PACKET[Minimum contents]
    direction LR
    T[Task ID and current status]
    S[Source and evidence]
    F[Verified facts and unknowns]
    C[Actions already attempted]
    N[Next action and due date]
    A2[Permission and approval status]
  end
  P --> PACKET
  PACKET --> NEXT[Next named owner]
  NEXT --> ACK{Accepted?}
  ACK -->|Yes| WORK[Continue task]
  ACK -->|No| ESC[Escalate to coordinator]
  WORK --> LOG[Record result]
  ESC --> LOG
```

**Practical check:** if the next person cannot understand a task from its handoff record, the workflow is not ready to run unattended.
