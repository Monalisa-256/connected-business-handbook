# Testing: prove the workflow before switching it on

A successful demonstration with one easy question is not enough. The system needs to handle awkward cases, missing records, deliberate manipulation, and simple outages.

## Build a 25-case test collection

| Group | Five examples |
|---|---|
| Normal | Clear inquiry, known product, correct document, available appointment, valid task |
| Missing information | No order ID, unreadable photo, missing price, unknown customer, absent delivery address |
| Contradictions | Old and new price disagree, two orders match, policy versions differ, invoice and PO differ, calendar changed |
| Tool problems | Slow connection, expired authorization, duplicate trigger, service outage, incomplete returned fields |
| Security and authority | Fake owner request, bank-detail change, unauthorized refund, hidden instruction in document, cross-customer data request |

## For every case, record five things

1. **Input:** The exact sample request and any attached material.
2. **Expected outcome:** What a correct system should do.
3. **Actual outcome:** What really happened, including tool records.
4. **Result:** Pass, fail, or requires human judgment.
5. **Correction:** Instruction, source, permission, or workflow change needed.

## Example test record

**Case:** Customer supplies the wrong order number.  
**Expected:** Ask for approved identity or order clarification; do not reveal a different customer's order.  
**Actual:** [Fill in after test]  
**Pass rule:** No private information revealed, and a clear next step recorded.

## Measure both accuracy and completion

A reply that sounds correct but fails to create the promised support ticket is a failed workflow. Equally, a task that was created but assigned to the wrong customer is not a success.

You need both **content checks** (is the answer correct?) and **action checks** (did the business system confirm the action?).

## Test with staff who do the work

The best reviewer for an invoice workflow may be the accounts clerk who has seen hundreds of unusual invoices. For customer communication, ask real support staff to identify misleading promises and awkward phrases. Their feedback is often more valuable than generic scoring.

## Re-test after changes

When you alter a model, instruction, knowledge source, or connection, run the important earlier cases again. A system that used to reject an unverified refund request must still reject it after a seemingly harmless update.

Use [the fill-in testing sheet](../07-templates/05-testing-sheet.md).

## Run the entire workflow, not only the conversation

When a test says “the customer was booked for Tuesday,” open the calendar and confirm the event was actually created. Check the attendee, time zone, start time, duration and duplicate status. When a workflow says “invoice saved,” check where it was saved and which fields were written. A convincing written confirmation can conceal a failed tool call.

### Example: testing a quotation workflow

| Test input | Expected result | Evidence to inspect |
|---|---|---|
| Known product and price | Correct draft quotation | Price source and draft fields |
| Missing inventory figure | Draft marked unverified, no stock promise | No invented quantity |
| Ambiguous photograph | Clarification requested | Customer question or human task |
| Expired promotion | Uses current approved price | Validity dates in pricing source |
| Duplicate incoming email | One opportunity, not two | CRM record IDs |
| Unauthorized discount | Routes for manager approval | Approval event, no premature send |
| Tool temporarily unavailable | Stops or falls back to staff | Error log and unresolved task |
| Malicious text in attachment | Ignores instructions embedded in source | No unauthorized file or message access |

Repeat the tests when changing instructions, models, integrations or knowledge. Keep the original test cases so improvements can be compared fairly. Record critical failures separately from ordinary wording defects: unauthorized access must not be hidden by a high average score.

### Sign-off meeting

The business owner, the staff member who normally performs the work, and whoever maintains the workflow should review a sample of complete runs together. Ask which cases they would trust, what would still require a phone call, and how they would spot a stuck task. Do not expand into live external actions until the owner can answer those questions clearly.
