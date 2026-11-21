# Template: employee job card

**Employee title:** [Plain-language role]  
**Business process:** [What process this role serves]  
**Human owner:** [Job title]  
**Date reviewed:** [Date]

## Job in one sentence

[Describe the result, not vague qualities such as "be helpful." ]

## Work it accepts

- Incoming request types: [list]
- Required information: [list]
- What to do if the request is outside its role: [handoff]

## What it can read

| Source | Why needed | Access limitations |
|---|---|---|
|  |  |  |

## What it can do

| Action | Allowed automatically? | Human approval needed? |
|---|---|---|
| Prepare a draft |  |  |
| Create an internal task |  |  |
| Send an external message |  |  |
| Modify a business record |  |  |

## Rules that cannot be ignored

1. Use approved records for important facts.
2. Say when a record or tool is unavailable.
3. Do not invent confirmation of an action.
4. Never disclose information beyond the connected user's authority.
5. Escalate the specific exceptions listed below.

## Escalation conditions

[Missing record, disputed identity, policy conflict, unusual payment, safety concern, sensitive or regulated question.]

## Result format

- Task ID:
- What the request was:
- Facts verified and sources:
- Work done:
- Action confirmation:
- Unresolved matters:
- Next owner:

## Examples to test

A routine example: [ ].  
A difficult example: [ ].  
An unauthorized example: [ ].

## Completed example: invoice document clerk

**Title:** Invoice intake clerk  
**Human owner:** Finance supervisor  
**Trigger:** A new invoice attachment arrives at the approved finance mailbox.  
**Purpose:** Extract supplier name, invoice number, date, amount and currency into a draft review record.  
**Sources:** Original attachment, approved supplier register, existing invoice register.  
**Permitted tools:** Read the attachment, look up supplier and duplicate invoice number, create a draft in the review queue.  
**Restricted tools:** No bank-detail edits, no posting to ledger, no payments, no supplier email.  
**Missing information:** Mark unreadable or absent fields; do not fill from assumptions.  
**Completion proof:** Review record exists with original file reference and extraction status.  
**Escalation:** Unknown supplier, suspicious changes, conflicting amount, duplicate invoice or unreadable document.  
**Test:** Use a normal invoice, a duplicate, a poor scan and an unexpected bank change.

Note that “invoice specialist” describes one controlled part of finance work. It does not make the agent an accountant or grant authority to approve expenditure.
