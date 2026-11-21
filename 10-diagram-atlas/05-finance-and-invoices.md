# Finance workflow: from invoice to approved payment

Invoice extraction, expense coding, accounting approval and bank payment are different operations. Combining them without checks can create costly failures.

```mermaid
flowchart TB
  IN[Invoice email or upload] --> EX[Extract number, date, supplier, currency, lines]
  EX --> DUP{Duplicate invoice?}
  DUP -->|Yes| HOLD1[Exception: suspected duplicate]
  DUP -->|No| SUP[Check supplier master]
  SUP --> BANK{Bank details changed?}
  BANK -->|Yes| HOLD2[Independent supplier verification]
  BANK -->|No| PO[Match approved purchase order]
  PO --> GOODS[Compare delivery or service receipt]
  GOODS --> TOTAL[Check amounts in accounting system]
  TOTAL --> MATCH{All required checks pass?}
  MATCH -->|No| HOLD3[Document discrepancy and owner]
  MATCH -->|Yes| DRAFT[Prepare payable entry]
  HOLD1 & HOLD2 & HOLD3 --> FIN[Human finance investigation]
  DRAFT --> FIN
  FIN --> APPROVE{Authorized approval?}
  APPROVE -->|No| REJECT[Hold or return]
  APPROVE -->|Yes| PAY[Separate payment execution]
  PAY --> CONFIRM[Confirm bank transaction]
  CONFIRM --> RECON[Reconcile accounting record]
  RECON --> END[Close with audit trail]
```

## Separation of duties

```mermaid
flowchart LR
  A[Document reader] --> B[Draft ledger record]
  B --> C[Finance verifier]
  C --> D[Authorized approver]
  D --> E[Payment operator or banking control]
  E --> F[Independent reconciliation]
```

**Owner's check:** the entity that extracts an invoice must not silently become the entity that approves and pays it. Independent confirmation is especially important when a supplier requests new account details.
