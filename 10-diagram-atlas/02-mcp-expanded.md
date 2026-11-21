# MCP connection: how work crosses the boundary

The left side is the person and the assistant. The right side is the business service that really owns the data. The assistant can request an operation, but the service must decide whether that operation is allowed.

```mermaid
flowchart LR
  subgraph PERSON[Person]
    O[Owner's request]
    ID[Who is asking?]
  end
  subgraph ASSISTANT[Assistant application]
    CHAT[Interpret request]
    LIST[Discover tool descriptions]
    CHOOSE[Select appropriate tool]
    PROMPT[Reusable work instructions]
    RESOURCE[Optional readable resources]
  end
  subgraph BOUNDARY[Permission boundary]
    AUTH[Account authorization]
    SCOPES[Allowed operations and data scope]
    GATE{Approval required?}
    HUMAN[Person approves or declines]
  end
  subgraph MCP[MCP service]
    SERVER[Trusted MCP server]
    READ[Read a record]
    DRAFT[Create a draft]
    WRITE[Change a record]
    SEND[Send externally]
  end
  subgraph SYSTEM[Real business records]
    CRM[(CRM)]
    DRIVE[(Document storage)]
    CAL[(Calendar)]
    MAIL[(Mail service)]
  end
  O --> CHAT
  ID --> AUTH
  CHAT --> LIST --> CHOOSE
  PROMPT --> CHAT
  RESOURCE --> CHAT
  CHOOSE --> AUTH --> SCOPES --> GATE
  GATE -->|Yes| HUMAN --> SERVER
  GATE -->|No and permitted| SERVER
  SERVER --> READ & DRAFT & WRITE & SEND
  READ --> CRM
  DRAFT --> DRIVE
  WRITE --> CAL
  SEND --> MAIL
  SYSTEM --> SERVER --> CHAT
```

## Ordinary owner request, detailed sequence

```mermaid
sequenceDiagram
  autonumber
  actor Owner
  participant Chat as Assistant host
  participant Scope as Permission control
  participant MCP as Connected MCP service
  participant Cal as Calendar
  Owner->>Chat: Find a free appointment next Tuesday
  Chat->>Scope: May this account read availability?
  Scope-->>Chat: Read availability only
  Chat->>MCP: Search approved calendar
  MCP->>Cal: Query actual times
  Cal-->>MCP: Free and occupied intervals
  MCP-->>Chat: Availability data
  Chat-->>Owner: Offered free slots, not bookings
  Owner->>Chat: Book 2:30 pm for this client
  Chat->>Scope: May I create this event?
  alt Authorized with required approval
    Scope-->>Chat: Create allowed after review
    Chat->>MCP: Create approved event
    MCP->>Cal: Write event
    Cal-->>MCP: Event ID and confirmed time
    MCP-->>Chat: Receipt
    Chat-->>Owner: Booking confirmed with event ID
  else Not authorized
    Scope-->>Chat: Denied
    Chat-->>Owner: I can prepare a request for staff
  end
```

**Remember:** An MCP connection is neither the calendar nor the language model. It gives an approved way for an application to request functions provided by the calendar service.
