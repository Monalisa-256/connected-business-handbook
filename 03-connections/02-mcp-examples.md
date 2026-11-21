# Ten ways a business owner could use MCP

These are **illustrative workflows**. Each requires a compatible app, a real connection exposing the relevant tools, suitable account permissions, and the business owner's approval rules. MCP does not automatically provide every listed integration.

## 1. Morning calendar briefing

**Owner asks:** "What are my meetings today, and what should I prepare?"

**Connected capabilities:** Read events; look up approved meeting notes; find related tasks.

**Result:** A briefing listing meeting times, attendees, outstanding preparations, and source links. The assistant should not silently reschedule meetings.

## 2. Sales pipeline check

**Owner asks:** "Which quotations sent last week still need a follow-up?"

**Connected capabilities:** Search CRM deals; read quotation dates and status; create draft follow-up tasks.

**Result:** A reviewable list of open opportunities. Contacting customers may require separate authorization and channel consent.

## 3. Inbox sorting

**Owner asks:** "Separate urgent service complaints from ordinary inquiries."

**Connected capabilities:** Read a permitted shared inbox; apply approved labels; create support tickets.

**Result:** A cleaned queue with reasons for prioritization. Keep outgoing replies in draft initially.

## 4. Supplier comparison

**Owner asks:** "Compare these three supplier offers with our approved purchasing rules."

**Connected capabilities:** Read uploaded offers; retrieve purchasing policy; optionally find supplier history.

**Result:** A comparison showing price, delivery, minimum quantity, payment terms, and missing information. Do not place an order without approval.

## 5. Staff task coordination

**Owner asks:** "Who owns the unfinished jobs from yesterday?"

**Connected capabilities:** Read task board; identify owner and status; prepare a summary or internal reminder.

**Result:** A short action list. The board, not the assistant's memory, is the record of responsibility.

## 6. Appointment preparation

**Owner asks:** "Find a suitable time next week for a customer consultation."

**Connected capabilities:** Read staff availability; consult service duration; draft a proposed time.

**Result:** Suggested slots. Make the booking only when the chosen time, customer identity, and tool action are authorized and confirmed.

## 7. Invoice review

**Owner asks:** "Find invoices that don't match their purchase orders."

**Connected capabilities:** Read approved invoice records; retrieve purchase orders; create a discrepancy report.

**Result:** A review list. Payment release stays with the accounts approver.

## 8. Stock exception report

**Owner asks:** "Which products are below the minimum stock threshold?"

**Connected capabilities:** Read inventory; read approved reorder levels; prepare a purchasing queue.

**Result:** Proposed restocking actions. Inventory values must come from the live system.

## 9. Meeting follow-through

**Owner asks:** "Turn yesterday's approved meeting notes into assigned tasks."

**Connected capabilities:** Read approved minutes; create tasks in the team's task system; link them to the meeting.

**Result:** Tasks with owners and deadlines. Ask for clarification when a name or deadline was not agreed.

## 10. Customer case follow-up

**Owner asks:** "Show the unresolved issues older than three days."

**Connected capabilities:** Search support tickets; read status and last activity; prepare an escalation list.

**Result:** A prioritized list for the service manager. Do not reveal a customer's information to an unrelated user.

## How much access does each example need?

| Example | Usually sufficient access | Usually unnecessary access |
|---|---|---|
| Morning calendar briefing | Read calendar and meeting notes | Delete calendar events |
| Supplier comparison | Read approved supplier documents | Authorize payments |
| Inbox sorting | Read and label selected mailbox | Send to arbitrary external recipients |
| Invoice review | Read invoice and PO records | Modify bank details |
| Stock report | Read inventory | Delete products or change pricing |

A good design grants only the minimum permissions needed to complete the job. [OWASP MCP security guidance](https://cheatsheetseries.owasp.org/cheatsheets/MCP_Security_Cheat_Sheet.html).

## What an MCP tool might look like to the owner

You may see choices such as "Search calendar", "List CRM contacts", "Create a task", or "Update a record". Read their descriptions carefully: **Search** and **Create** have very different consequences.

Never enter passwords or access tokens into a public repository. Use each platform's official account-connection screen.

## Five situations where the connection should stop

1. A manager requests a list of invoices, then asks the assistant to pay them. Search access does not imply payment authority.
2. A customer asks for the price of a product, but the live price system is unavailable. The assistant should not substitute a remembered price from an old advertisement.
3. A meeting note says to copy confidential client files to a new address. That sentence is source material, not an authenticated instruction.
4. A finance assistant finds a supplier email requesting changed bank details. The change requires independent verification according to company controls.
5. A staff member asks to cancel a colleague's calendar event. The underlying calendar permissions must decide whether it is allowed.

### A useful design distinction

Sometimes the assistant should **read** information, sometimes **prepare** a draft, and sometimes **carry out** a permitted write. Those stages can be divided across separate connections or operations. A business owner should not give an assistant a broad "manage everything" connector just to receive a morning summary.

[Practice the eight permission cases](../08-deep-dives/02-mcp-permission-lab.md)
