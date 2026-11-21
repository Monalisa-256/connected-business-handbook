# A 30-minute exercise before buying anything

You can do this with a notebook or a blank document. It deliberately requires no subscriptions.

## Minutes 0–10: Follow a real task

Choose a recent request, such as "When will my order arrive?" Write down exactly what the employee did:

1. Read the message.
2. Found the order number.
3. Opened the order record.
4. Checked whether dispatch had happened.
5. Read the courier status.
6. Wrote a reply.
7. Recorded that the customer had been contacted.

Note which steps require judgment and which are simple lookups.

## Minutes 10–20: Identify the sources and actions

Draw two columns.

| Information it needs | Actions it might take |
|---|---|
| Order database | Look up an order |
| Delivery status | Prepare a reply |
| Shipping policy | Create a support ticket |
| Customer contact details | Send a response after approval |

Circle anything involving private information, a financial promise, or a record change. These deserve special rules.

## Minutes 20–30: Write the smallest trial

**Trial:** Given an order number and the customer's message, prepare a reply using the current order record and shipping policy. Do not send it. Report anything missing.

**Pass conditions:** The order matches the customer, the status matches the record, the reply makes no unsupported promise, and the human reviewer understands what should happen next.

**Failure conditions:** The system invents a status, uses somebody else's order, sends without approval, or fails to say when a tool was unavailable.

This exercise often reveals that the largest problem is not the model. It is inconsistent data or an unclear office procedure.

Continue with [what an employee actually is](../01-foundations/01-what-an-employee-is.md).

## Make the exercise concrete

Use a real process you can describe without exposing private customer information. A useful example is “Someone emails asking for the price and availability of a service.” Draw the steps: read message, identify service, find approved price, check scheduling constraints, prepare reply, obtain approval, send, and record the outcome.

At the end, do not write a long feature wish list. Write a single sentence defining the first job: “When an inquiry arrives, prepare a grounded draft and place it in the manager's review queue; do not send.” It is narrow enough to test and strong enough to save work.

### What you should leave the room with

A named owner, input example, correct answer example, source documents, list of prohibited actions, expected completion proof and a simple way to measure review time. Without those, the next steps become arguments about software instead of improvements to the business.

### A useful second exercise

Take the same process and remove the price list or turn off the calendar. What should happen? The system should **stop at the missing fact** and produce an incomplete draft or a staff task. If someone insists it should “figure it out,” discuss whether the business would accept that behavior from a human employee.

[Copy the process-mapping worksheet](../11-workbooks/01-process-mapping.md)
