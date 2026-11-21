# Write job descriptions that an assistant can follow

A useful instruction is like a good employee handbook: it says what the work is, what information is reliable, what is outside the job, and who takes over when a problem arises.

## Seven questions to answer for every role

| Question | Example for a quotation preparer |
|---|---|
| What is the job? | Draft accurate quotations for standard products |
| What triggers it? | Sales inquiry assigned by intake |
| What facts can it use? | Current catalog and approved price list |
| What can it change? | Only a draft quotation and a task note |
| What cannot it decide? | Discounts, credit terms, delivery guarantees |
| What is the result? | Draft with items, quantities, prices, missing information |
| When does it escalate? | Unknown product, unusual terms, missing stock, price conflict |

## A sample role description

> **Role:** Customer Inquiry Clerk  
> **Purpose:** Turn incoming customer messages into complete, correctly classified tasks.  
> **Allowed sources:** The incoming message, approved customer FAQ, and selected CRM lookup.  
> **Allowed actions:** Create or update a support task in the assigned workspace.  
> **Not allowed:** Issue refunds, promise delivery dates, change account details, or send external messages without approval.  
> **When unsure:** State exactly what is missing and assign the task to the support lead.  
> **Completion:** A task exists with an ID, status, customer reference, summary, evidence and next owner.

The final sentence matters because it says how to tell whether the job really finished.

## Business rules should live in two places

**Inside the instructions:** Explain the policy in words so the assistant can understand when to ask for help.

**Inside the connected tool or approval process:** Enforce the same limits as actual permissions. If the job cannot send refunds, it should not have a refund tool available in the first place.

## One general assistant or several specialists?

Use one role if the workflow is short and all steps have the same data and permissions. Split the work when steps require different records, expertise, risk levels, or review rules.

For example, an intake clerk and a quotation preparer can be separate because the intake clerk should not have access to sales pricing exceptions. A separate "friendly wording agent" is probably unnecessary if it only repeats the writer's work.

## How instructions improve over time

When a test fails, identify the actual cause before changing the words:

- Wrong information: update or restrict the source.
- Missing action: add an approved connection.
- Confusing handoff: specify fields and owner.
- Too much freedom: reduce permissions.
- Poor wording: improve the instructions and examples.

Record changes and retest earlier examples so a fix for one task does not break another.

Use the [employee job card](../07-templates/02-employee-job-card.md) and [handoff template](../07-templates/03-instructions-and-handoffs.md).

## A job contract that staff can recognize

A role is much easier to evaluate when it resembles an ordinary work assignment. Consider an appointment coordinator. Its job is not “manage relationships”; it is “find authorized calendar openings, prepare an appointment option, and record whether the customer accepted.” It must know which calendar is authoritative, whose appointments it may see, which hours are bookable, and whether it can send messages itself. If any of those details are missing, the job description is unfinished.

A useful role contract has three parts. **Inputs** describe what arrives: a message, relevant customer reference, and requested time. **Outputs** describe what counts as completed work: proposed slots or a booked meeting with a verified calendar ID. **Boundaries** define what it must never do, including exposing another customer's calendar details or inventing availability.

### Example division of work: proposal request

| Responsible party | Specific responsibility | Proof of completion |
|---|---|---|
| Intake | Identify customer, need, deadline and attached files | Task exists with source reference |
| Research | Retrieve approved capability and service information | Linked source documents |
| Proposal writer | Prepare a first draft using verified facts | Draft document version |
| Reviewer | Check price, terms, missing information and scope | Review record with findings |
| Account manager | Approve final client-facing offer | Named approval and sent-message receipt |

If the writer cannot find an approved fee schedule, the correct output is a flagged incomplete proposal. It should not fill gaps with plausible-looking figures. This single rule does more to protect a business than a page of encouraging adjectives.

## Changing the rules safely

Treat instructions as a managed business document. Record who changed the rule, why, which version is in use, and which tests must be repeated. When a role gains a new connection—for example, permission to create a calendar event—test that additional power separately. Keep the previous working configuration long enough to recover if the change creates errors.
