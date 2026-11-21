# Company knowledge and the right model for the job

It helps to separate archived reference material from live records, and input understanding from the business decision.

```mermaid
flowchart TB
  Q[Question or work request] --> KIND{What fact is needed?}
  KIND -->|Policy| POL[Approved document library]
  KIND -->|Stock or price| INV[Live inventory and price source]
  KIND -->|Personal order| CRM[Permission-controlled customer record]
  KIND -->|Task progress| TASK[Task register]
  KIND -->|Public research| WEB[Current sources + source checks]
  POL & INV & CRM & TASK & WEB --> SOURCE[Source, date, version and access check]
  SOURCE --> COMPLETE{Evidence complete?}
  COMPLETE -->|Yes| MODEL[Appropriate language or reasoning model]
  COMPLETE -->|No| HUMAN[Clarify or ask source owner]
  MODEL --> OUTPUT[Answer with traceable facts]
  HUMAN --> OUTPUT
```

## Model selection by information type

```mermaid
flowchart LR
  INPUT[Incoming job] --> TYPE{Main difficulty?}
  TYPE -->|Simple sorting| LIGHT[Fast general model]
  TYPE -->|Complex comparison| STRONG[Stronger reasoning model]
  TYPE -->|Voice| STT[Speech recognition or real-time voice]
  TYPE -->|Photo| VISION[Vision model]
  TYPE -->|Scanned form| OCR[Document extraction]
  TYPE -->|Campaign visuals| ART[Image/video creation]
  LIGHT & STRONG & STT & VISION & OCR & ART --> DATA[Verified business records]
  DATA --> REVIEW[Validation and appropriate approval]
```

Do not select a costly engine because a vendor says it is "most intelligent." Select the least complex tool that achieves the required verified result.
