# Choose a small, sensible tool stack

The word *stack* simply means the set of products you use together. It should be small enough for someone in the business to understand and maintain.

## Three example setups

### A small shop using Google Workspace

- **Office apps:** Gmail, Drive, Sheets, Calendar.
- **Workflow:** Google Workspace Studio or Make.
- **Model:** One available general-purpose model in the chosen platform.
- **Record of work:** A shared task sheet or existing CRM.
- **Human control:** Owner reviews outgoing quotes and refunds.

Start with a message-to-task workflow. Add image recognition only if customer photographs are common.

### A service company using Microsoft 365

- **Office apps:** Outlook, SharePoint, Teams.
- **Workflow:** Copilot Studio and Power Automate.
- **Record of work:** Existing ticketing, lists, or CRM.
- **Specialist service:** Document extraction only where needed.
- **Human control:** Service lead approves unusual commitments.

Start with a staff-information assistant or internal case sorting.

### A company seeking distinct agent teams

- **Coordination:** Relevance AI workforce.
- **Knowledge:** Maintained company policies and catalogs.
- **Execution:** Limited connected apps or a Make scenario.
- **Review:** A named quality-checking role plus human approval.
- **Voice:** Add separately if calls are central to the business.

Start with Intake → Specialist → Reviewer. Add a live CRM connection only after the drafts are consistently correct.

## When not to combine platforms

Do not add a second orchestration product just because another tutorial looks impressive. Two products controlling the same workflow can produce duplicate tasks, unclear ownership, unexpected bills, and difficult troubleshooting.

Before adding a platform, state what the existing system cannot do and how the new one will solve it.

## A simple purchasing test

| Requirement | Must have now? | Provider verified? |
|---|---|---|
| Works with our existing accounts | Yes |  |
| Supports necessary languages | If customer-facing |  |
| Provides audit logs | Yes for actions |  |
| Can stop or restrict write actions | Yes |  |
| Offers a human handoff | Yes for customer-facing work |  |
| Supports our needed media type | Only if relevant |  |
| Exports work records | Preferably |  |
| Has predictable usage charges | Yes |  |

If a requirement is essential, do not accept an untested promise that it "should integrate." Make the provider demonstrate the exact job using a safe test account.

## The simplest workable combination often wins

Imagine a company whose staff already use Gmail, a CRM and Google Sheets. One option is to add a dedicated workforce platform, a speech provider, a second automation product and a new database. Another option is one workflow builder connected to the existing records, with a limited model step for classification and manager approval before emailing. The second may be far easier to maintain.

Each additional vendor increases billing, accounts, data access and fault investigation. Add a service only when a required modality or control is missing. If the business later needs telephone reception, connect a specialist voice tool to the established task register rather than building a separate disconnected customer history.

### Write an exit plan before subscribing

Can you export the task records, retrieve approved documents, revoke connected accounts and stop scheduled triggers? Do you know whether each service uses its own credits? If nobody owns these questions, the stack is already too complex for the team.

[Use the selection and launch diagram](../10-diagram-atlas/09-platform-and-launch.md)
