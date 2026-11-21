# Five MCP connection walkthroughs for business owners

These stories are not universal click-by-click instructions. They show what a **properly supported connection** should accomplish and where the owner should insist on checks. A real platform may provide these actions through built-in apps, an MCP server, a visual automation connector, or a mixture of the three.

## Walkthrough 1 — Read a calendar, but do not edit it

**Business question:** "Which appointments do we have tomorrow?"

**What to connect:** A selected business calendar through a trusted compatible tool.

**Tools to allow:** Find events or read event details. **Tools to withhold:** Delete, edit, or invite guests until there is a clear need.

**Test:** Ask for the events on a harmless test calendar. Compare titles, dates and time zone with the calendar itself. Ask about a nonexistent event: the assistant should say it cannot find it.

**What counts as success:** An accurate schedule summary based on an actual event lookup. Merely producing a plausible agenda is not enough.

## Walkthrough 2 — Create a CRM follow-up task

**Business question:** "Please remind the sales team to call this prospect on Tuesday."

**What to connect:** Approved CRM or task system; only the project or team needed.

**Tools to allow:** Search a contact, create a follow-up task. **Tools to withhold:** Delete contacts, export the entire customer list, change pricing.

**Test:** Use a synthetic prospect. Have the assistant find the right record and prepare a task. Confirm the CRM returns a task ID. Repeat the same request to see whether the workflow duplicates the task.

**What counts as success:** One task with correct owner, due date and linked contact. A good design checks for duplicates before retrying.

## Walkthrough 3 — Look up the right company document

**Business question:** "What does our current warranty policy say about replacement parts?"

**What to connect:** A restricted company knowledge source, not the owner's entire personal drive.

**Tools to allow:** Search or read approved policy documents. **Tools to withhold:** Change permissions, share publicly, delete files.

**Test:** Put an old policy and a current policy in different test folders. Confirm the assistant uses the designated current version and identifies conflicts.

**What counts as success:** Answer with a source link and policy version, or an explicit request for clarification.

## Walkthrough 4 — Find invoices, but keep payments separate

**Business question:** "Which supplier invoices are overdue for review?"

**What to connect:** A read-only invoice register and the task system.

**Tools to allow:** Search invoices and create review tasks. **Tools to withhold:** Payment release, bank-detail updates, supplier onboarding.

**Test:** Create an invented invoice that is due for review and another already approved. Confirm only the correct item is flagged and no payment changes occur.

**What counts as success:** An exception list with invoice references and a named accounts reviewer.

## Walkthrough 5 — Get a meeting briefing from several sources

**Business question:** "Summarize my next client meeting and open tasks."

**What to connect:** A test calendar, approved task board, and selected meeting notes.

**Tools to allow:** Read event, read assigned tasks, search approved notes. **Tools to withhold:** Bulk email sending, permission changes, delete.

**Test:** Include an out-of-date note and a task closed yesterday. The briefing should reflect the current task status, explain any mismatch, and link to the sources.

**What counts as success:** A useful briefing with clear evidence and no changes to business records.

## What the owner should see in the connection settings

| Question | Good answer |
|---|---|
| Who provides this connection? | A clearly identified, trusted operator |
| Which account is connected? | The intended business account |
| Which actions are available? | A readable list of exact tools |
| Can we limit those actions? | Yes, with narrowly scoped permissions or separate services |
| Can we disconnect quickly? | A clear revoke/disconnect process |
| Where do actions appear? | Logs or confirmations in the underlying business system |

## Local versus remote MCP, in plain language

A *remote* MCP service is operated somewhere else and contacted over a network. A *local* MCP service runs on a computer or internal machine. The two can have different setup, access and security requirements. A no-code business owner generally starts with vendor-supported remote connections, rather than installing software on a staff computer. Never assume local means safer: local services can also be over-permissioned.

The current [MCP specification](https://modelcontextprotocol.io/specification/2026-07-28) describes the protocol rather than guaranteeing any particular provider's trustworthiness. The [OWASP MCP checklist](https://cheatsheetseries.owasp.org/cheatsheets/MCP_Security_Cheat_Sheet.html) is a useful reminder to review permissions and server identity.

## A simple rule for all five examples

Start by **reading** the right facts. Next allow **drafting**. Then, only where needed, permit **specific actions** with verification. Never begin by giving a new connection broad permission to send messages, spend money or delete records.

## The same test should be repeated after a change

When the platform updates, a connector is replaced, or an administrator adjusts access, repeat the forbidden-action tests. A workflow that once used a search-only tool may later be given a broader action. This can happen without the visible business instructions changing.

### Read-only first is an implementation strategy

A useful rollout sequence is: read authorized records; produce grounded summaries; prepare unsent drafts; create low-risk internal tasks; add controlled reversible writes; consider external actions after repeated successful tests and documented approval. This sequencing helps an owner understand which component caused an error. Jumping directly to sending, refunds or database editing makes early mistakes hard to isolate.

### Keep a record of denial

When testing a forbidden action, note the account, tool, attempted operation, actual result and evidence. A blocked request is an important test outcome. If the assistant politely refuses while an underlying integration still has administrator privileges, the system remains overpowered.

[Practice in the permission lab](../08-deep-dives/02-mcp-permission-lab.md)
