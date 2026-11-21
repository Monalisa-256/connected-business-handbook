# Workbook: inventory every MCP connection and app connector

A company should be able to answer, "Which assistants can touch our calendar, email, customer records and accounting systems?" This page provides a register for that question.

| Connection | Provider / owner | Business system | User or service credential | Read actions | Write actions | Approval rule | Data scope | Last tested | Revoke owner |
|---|---|---|---|---|---|---|---|---|---|
| Example: Calendar reader | Approved provider | Team calendar | Named staff account | Availability | None | Not applicable | One calendar |  | Admin |
|  |  |  |  |  |  |  |  |  |  |

## Record the scope, not just the app name

A connector labeled "Google Drive" might see one approved folder or the full account, depending on authorization and product behavior. Similarly, an assistant that can search contacts might also be able to edit or export them. List the actual operations visible to the model and verify them through testing.

## Review triggers

Review access when an employee changes roles or leaves, a model or platform changes, new tools are added, a vendor's terms change, an incident occurs, or a process owner no longer needs the connection.

## Disconnection drill

Identify the person who can disable the connection. Confirm they can find the control in the actual product. Check whether scheduled workflows remain enabled elsewhere and whether stored credentials or cached results need separate handling under your policies.

**Last access audit:** ______  **Next review:** ______  **Emergency administrator:** ______
