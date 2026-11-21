# Multimodal information: six entrances, one task register

This map illustrates why voice, image, document and video handling are separate skills, even when a single app presents them in the same conversation.

```mermaid
flowchart TB
  subgraph INPUT[Different customer and staff inputs]
    direction LR
    TEXT[Typed message]
    VOICE[Voice recording]
    PHONE[Live call]
    IMAGE[Product or damage photo]
    DOC[Invoice or scanned form]
    VIDEO[Video clip]
  end
  subgraph PROCESS[Prepare and interpret]
    direction LR
    T1[Language and request]
    T2[Speech transcript]
    T3[Turn-taking and live transfer]
    T4[Visible details and uncertainty]
    T5[Fields and document layout]
    T6[Supported video observations]
  end
  TEXT --> T1
  VOICE --> T2
  PHONE --> T3
  IMAGE --> T4
  DOC --> T5
  VIDEO --> T6
  T1 & T2 & T3 & T4 & T5 & T6 --> TEST{Key facts reliable?}
  TEST -->|No| CLARIFY[Request confirmation or human check]
  TEST -->|Yes| CASE[Create verified case record]
  CLARIFY --> CASE
  CASE --> LOOKUP[Check relevant business systems]
  LOOKUP --> ROUTE[Route to correct specialist]
  ROUTE --> DECIDE{Evidence and permissions sufficient?}
  DECIDE -->|No| REVIEW[Human review or more evidence]
  DECIDE -->|Yes| OUT[Prepare suitable response]
  REVIEW --> OUT
  OUT --> CHANNEL{Return channel}
  CHANNEL --> EMAIL[Email or text]
  CHANNEL --> SPEAK[Voice response]
  CHANNEL --> REPORT[Document or report]
  EMAIL & SPEAK & REPORT --> LOG[Record outcome]
```

## Understanding versus creating

```mermaid
flowchart LR
  PHOTO[Incoming product photograph] --> VISION[Image understanding] --> MATCH[Compare with catalog]
  NOTE[Incoming voice note] --> SPEECH[Speech recognition] --> REQUEST[Structured request]
  IDEA[Approved campaign brief] --> IMAGEGEN[Image creation] --> ART[Visual concept]
  SCRIPT[Approved script] --> VOICEGEN[Speech generation] --> NARRATION[Recorded narration]
  ART & NARRATION --> EDIT[Human creative review]
  MATCH & REQUEST --> OPER[Verified business operation]
```

An image maker is not necessarily a reliable visual inspector, and a natural voice generator is not necessarily a telephone receptionist. Test each job with its actual inputs and required outputs.
