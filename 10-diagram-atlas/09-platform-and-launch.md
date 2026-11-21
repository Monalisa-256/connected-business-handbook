# Platform selection and safe launch

No-code platforms overlap, but their strengths and surrounding ecosystems differ. This map gives a way to shortlist them without treating it as a permanent product ranking.

```mermaid
flowchart TB
  B[Business environment] --> Q{What matters first?}
  Q -->|Visual specialist teamwork| REL[Relevance AI]
  Q -->|Many app integrations| MAKE[Make]
  Q -->|Simple app actions| ZAP[Zapier]
  Q -->|Microsoft workplace| MS[Copilot Studio + Power Automate]
  Q -->|Google workplace| GS[Google Workspace Studio]
  Q -->|Flexible workflow operations| N8N[n8n]
  Q -->|Calls and chat| VOICE[Voiceflow / ElevenLabs / Botpress]
  REL & MAKE & ZAP & MS & GS & N8N & VOICE --> SEC[Review access controls]
  SEC --> DEMO[Run same sample cases]
  DEMO --> COST[Compare cost and operational effort]
  COST --> CHOOSE[Select manageable starting platform]
```

## Launch as a series of controlled gates

```mermaid
flowchart LR
  S[Choose one job] --> MAP[Map present process]
  MAP --> SOURCE[Confirm data sources]
  SOURCE --> ROLE[Define responsibilities]
  ROLE --> BUILD[Build limited workflow]
  BUILD --> TEST[Run normal and hostile examples]
  TEST --> SIGN[Owner approves pilot]
  SIGN --> PILOT[Supervised live use]
  PILOT --> RESULT[Measure outcomes and failures]
  RESULT --> SCALE{Reliable and worthwhile?}
  SCALE -->|Yes| EXPAND[Add channel or responsibility]
  SCALE -->|Not yet| REWORK[Refine or stop]
```
