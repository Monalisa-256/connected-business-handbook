# Template: connected-tool permission register

Keep this in a private business workspace rather than a public repository if it contains account names or system details. Never include passwords, tokens or other secrets.

| Connected tool | Human owner | Purpose | May read | May change | Approval required | Review date |
|---|---|---|---|---|---|---|
| Example: Test calendar | Office manager | Find available slots | Selected test calendar | Nothing | N/A | [date] |
| [Tool 2] |  |  |  |  |  |  |
| [Tool 3] |  |  |  |  |  |  |

## Before adding a connection

- [ ] Provider and operator identity verified.
- [ ] Official vendor documentation reviewed.
- [ ] Only necessary permissions granted.
- [ ] The business has a process to revoke access.
- [ ] Logs show who did what.
- [ ] External data-sharing and retention terms checked.
- [ ] One harmless query tested and verified.
- [ ] One failure scenario tested.
- [ ] Named staff member responsible for ongoing review.

## Change and removal log

| Date | Change | Approved by | Tested by | Result |
|---|---|---|---|---|
|  |  |  |  |  |

## Account departure checklist

When an employee leaves or changes role, review the accounts and connected tools they controlled, transfer ownership where appropriate, remove permissions, and verify any ongoing workflows still have an accountable owner.

## Add these columns before production

| Additional field | Why it matters |
|---|---|
| Service provider / connection name | Identifies exactly which integration holds access |
| Signed-in business account | Differentiates a limited staff account from an owner's account |
| Actual exposed actions | “CRM integration” may include read, create, edit and delete tools |
| Data categories | Customers, employee details, bank records, pricing, etc. |
| Grant date and expiry/review date | Prevents indefinite forgotten access |
| Who approved access | Records accountable authority |
| Last negative-permission test | Confirms forbidden actions are still blocked |
| Revoke procedure | Makes emergency containment possible |

### Review exercise

Imagine a calendar connector suddenly adds a “delete event” tool during a platform update. Would the business notice? Would that operation automatically become available to the assistant? Who can disable it? Record the answers here. Do not accept “the prompt says no” as the only safeguard.
