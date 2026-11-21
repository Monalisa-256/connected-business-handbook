# How the same building blocks apply to 15 industries

The purpose of this table is not to suggest one universal workflow. It shows how the **same few capabilities** are rearranged around different records, customers, and risks.

| Business | A familiar incoming request | Capabilities and handoff | Important boundary |
|---|---|---|---|
| Retail shop | "Is this item in stock?" with photo | Vision → catalog lookup → reply draft | Stock must come from current inventory |
| Online store | "My parcel is late" | Message intake → order/courier lookup → case | Verify customer before sharing order details |
| Restaurant | "Can six of us book for Friday?" | Language → live reservation availability → booking confirmation | Suggested times are not confirmed bookings |
| Hotel | "Can I check in early?" | Guest inquiry → booking lookup → front-desk review | Do not guarantee rooms before staff confirmation |
| Property agency | "Show me houses under this budget" | Listing search → qualification → viewing preparation | Listings and availability must be current |
| Consultancy | "Can you draft a proposal?" | Brief intake → research → writing → approval | Terms and fees require owner approval |
| Law office | "What documents should I bring?" | Approved intake guide → document checklist | No unauthorized legal advice |
| Medical practice | "When is the next appointment?" | Scheduling lookup → patient verification → staff booking | No autonomous diagnosis or prescribing |
| School administration | "Where is the fee policy?" | Policy search → answer with source | Protect student and family data |
| Logistics company | "Where is shipment 238?" | Tracking lookup → exception report → support | No invented delivery estimates |
| Manufacturing | "This machine looks damaged" with photo | Image intake → maintenance ticket → technician | Safety decisions require qualified human inspection |
| Agricultural cooperative | "What does this crop photo suggest?" | Image description → expert referral | Do not present visual guesses as definitive treatment |
| Accounting practice | "Read these receipts" | Document extraction → expense list → review | No automatic fund release |
| Construction company | "Summarize today's site report" | Voice/photo intake → task log → supervisor review | Site safety and compliance need accountable experts |
| Nonprofit organization | "Which grants require reports this month?" | Grant-document search → deadline tracker → manager | Verify contractual deadlines with original agreements |

## Three stories in more depth

<details>
<summary><strong>Restaurant: a booking request arrives as a voice note</strong></summary>

A caller asks for a table for six on Friday evening. Speech recognition identifies party size and approximate time. The assistant checks the actual reservation system. If no time is available, it offers only verified alternatives. The booking is not considered complete until the reservation provider confirms it. Staff handle special accessibility needs, unusual event requests and conflicting records.

**Possible no-code first version:** A voice or chat assistant that gathers the reservation details and sends them to reception for confirmation.

</details>

<details>
<summary><strong>Construction: a daily site update</strong></summary>

A supervisor provides three photographs and a voice note describing completed work, material delays and next steps. A transcription and document assistant drafts the daily site report. A site manager corrects facts, confirms measurements, and signs off before the report enters official project records.

**Possible no-code first version:** A form with media attachments and a draft report in a shared folder.

</details>

<details>
<summary><strong>Professional services: a new client inquiry</strong></summary>

A prospective client sends an email describing a problem and attaching a PDF. Intake collects basic facts and identifies missing information. A specialist drafts a response or proposal from approved company material. The responsible professional reviews scope, suitability, price and obligations before sending.

**Possible no-code first version:** Inbox classification, intake checklist and review queue; no automatic acceptance of clients.

</details>

## How to adapt an example to any other business

Replace five things: **the incoming request, the source of truth, the specialist who owns the task, the allowed action, and the point where a person decides**. The rest of the workflow design can often stay similar.

## Why industry labels can mislead

Two companies in the same industry may have very different systems and risks. A retail business handling only general product questions is not comparable to one managing regulated products, customer credit and large returns. A clinic scheduling appointments is not the same as a system making clinical decisions. A construction report organizer is not a certified site inspector.

When adapting an example, first write what the business is **actually allowed and qualified to do**. Identify the human owner, source of truth and verification process. Then select a workflow pattern. The technical path from "photo plus voice note" to "structured report" can be reused widely, but the professional judgment behind the report may not be transferable.

### Expanded standalone cases

The [case-study collection](../09-case-studies/01-retail-voice-photo-sales.md) includes detailed examples for retail, consulting, clinics, hospitality, construction, invoices, schools, agriculture, delivery, marketing, nonprofit reporting and manufacturing. Each includes specific failure cases so the reader can distinguish business risk from an attractive demonstration.
