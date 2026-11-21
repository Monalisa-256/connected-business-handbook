# Case study: a guest asks about a booking and a late arrival

**Business:** A small hotel or guesthouse. **Channels:** Email, website chat and telephone. **Objective:** Give reliable reservation information and coordinate with the front desk without inventing room availability.

## The guest's message

> “Our flight will arrive late. Can we still check in after midnight? Also, is breakfast included in our booking?”

The booking reference is provided, but the message comes from an address not yet associated with the reservation. The assistant should avoid revealing private booking details until the identity checks required by the property are satisfied.

## Information and responsibilities

| Question | Source to check | What can go wrong |
|---|---|---|
| Is the booking valid? | Property management system | Similar guest name; cancelled reservation |
| Is breakfast included? | Actual rate plan for this booking | General website policy differs from booked rate |
| Is late check-in available? | Front desk rules and night staffing | Local rules changed last week |
| Does airport transfer exist? | Approved transport arrangements | Third-party service unavailable |
| Was the answer sent? | Messaging provider receipt | Draft mistaken for sent message |

```mermaid
sequenceDiagram
  autonumber
  actor Guest
  participant Front as Guest service assistant
  participant Auth as Booking verification
  participant PMS as Property system
  participant Staff as Night manager
  Guest->>Front: Late arrival + breakfast question
  Front->>Auth: Validate permissible booking access
  Auth-->>Front: Verification required
  Front->>Guest: Request safe booking verification
  Guest->>Front: Provides required confirmation
  Front->>PMS: Read rate plan + booking status
  PMS-->>Front: Confirmed booking; breakfast included
  Front->>Staff: Check late-arrival arrangements
  Staff-->>Front: Night desk will admit guest
  Front-->>Guest: Confirmed conditions and next steps
```

## Where to keep the human

Changes to cancellation penalties, refunds, complimentary upgrades, overbooking and payment disputes should follow existing front-desk and management rules. An assistant can prepare a recommendation or offer approved alternatives, but it should not silently waive charges.

## Practical expansion

Once reservation questions work reliably, add maintenance requests: "The room's air conditioner is not working." The assistant records the room reference after appropriate verification, categorizes the issue and assigns the maintenance team. Completion is confirmed when staff actually report and verify the repair—not when the task is simply created.

**Metrics:** Wrong booking details, successful late-arrival coordination, open maintenance backlog, staff handoff time, complaint recurrence and guest feedback.

**Adaptations:** Restaurants with bookings, event venues, serviced apartments and travel accommodation.
