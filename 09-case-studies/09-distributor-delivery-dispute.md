# Case study: a distributor resolves a late-delivery dispute

**Business:** Distributor with dispatch staff, warehouse inventory and a courier partner. **Objective:** Give verified shipment updates and coordinate an exception without accusing any party based on one message.

## The dispute

A customer says the driver never arrived. The courier system says "delivered". A proof-of-delivery photo shows a building entrance but no identifiable recipient. The warehouse confirms the parcel left the depot.

This is an evidence conflict, not a simple FAQ question. The assistant's task is to gather the records, explain what is known, and create a case for the accountable team.

```mermaid
sequenceDiagram
  autonumber
  actor Customer
  participant Service as Customer service
  participant Order as Order system
  participant Courier as Courier tracking
  participant Dispatch as Dispatch supervisor
  Customer->>Service: My order never arrived
  Service->>Order: Confirm matching order and address
  Order-->>Service: Shipped to recorded address
  Service->>Courier: Retrieve scan and delivery evidence
  Courier-->>Service: Marked delivered; image is inconclusive
  Service->>Dispatch: Open disputed-delivery case with evidence
  Dispatch-->>Service: Investigation assigned
  Service-->>Customer: Report verified facts and next update
```

## The customer-facing response

> I can confirm that the order was dispatched to the recorded delivery address. The courier's system currently marks it delivered, but the available proof does not establish who received it. I have opened an investigation with our dispatch team. We will update you through the agreed contact channel once the delivery is verified.

This avoids claiming the customer is lying and avoids issuing an unsupported refund. It also does not describe a photo as definitive when it is not.

## Who may do what?

Service can gather records and communicate approved case status. Dispatch can investigate driver and handover details. Finance can prepare a credit or adjustment after an authorized decision. The assistant cannot edit courier tracking or certify delivery from the photo.

## Important exception tests

Two orders with the same surname; wrong time zone in tracking; a courier status updated after the message; incomplete proof-of-delivery image; customer changes address after dispatch; tool returns stale cached tracking. Design the workflow to record retrieval time and route contradictions to the responsible person.

**Measures:** Case resolution time, repeat contacts, wrong-order lookups, number of escalations closed with evidence and customer complaint recurrence.
