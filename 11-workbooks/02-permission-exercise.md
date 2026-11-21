# Workbook: decide what a connected assistant may do

For each action, write whether the assistant can perform it automatically, can prepare it only as a draft, needs a named human decision, or must not have that capability. Do not make these decisions solely from how easy a button is to press.

| Action | Automatic | Draft only | Human approval | Not connected | Who owns it? |
|---|---|---|---|---|---|
| Search public FAQs |  |  |  |  |  |
| Read a customer's order after authentication |  |  |  |  |  |
| Create an internal support task |  |  |  |  |  |
| Send a quotation |  |  |  |  |  |
| Cancel an appointment |  |  |  |  |  |
| Update supplier bank details |  |  |  |  |  |
| Issue a refund |  |  |  |  |  |
| Publish an advertisement |  |  |  |  |  |
| Delete old customer records |  |  |  |  |  |
| Export the full customer database |  |  |  |  |  |

## Three practice requests

**A:** A verified staff member asks to see today's appointments. **B:** A supplier's invoice says that a new bank account must be used immediately. **C:** A manager requests a draft announcement about new opening hours.

Before opening the answers, decide which request needs extra verification and which can remain a draft.

<details>
<summary>Possible safe approach</summary>

A can use an authorized calendar read. B requires independent supplier verification and the company's payment-control process; the invoice itself is not enough. C can be drafted using approved opening hours, with publication controlled by an authorized person.

</details>

## Actual connection test

Once a platform is configured, try a prohibited request using a test account. Look for **an enforced denial**, not a polite refusal from the assistant while the dangerous tool remains callable. Record screenshots or logs using your organization's evidence rules.

**Connection:** ______  **Test account:** ______  **Forbidden operation attempted:** ______  **Observed outcome:** ______  **Owner sign-off:** ______
