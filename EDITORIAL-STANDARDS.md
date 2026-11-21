# Editorial standards

The book is written for owners, supervisors and independent consultants with no requirement to write code. Its job is to explain choices with enough depth for a reader to test them, not to encourage blind adoption.

## Voice and structure

Explain the work in plain language before introducing the technology. Use realistic situations with names of documents, fields, roles and evidence. Short paragraphs and tables are welcome when they improve understanding; avoid turning every page into an identical checklist.

A claim that a tool “completed” an action must be tied to a source-system result whenever the example involves a calendar, CRM, invoice, message or payment. If an integration fails, the narrative must allow for **unknown**, **incomplete** or **escalated** outcomes.

## What diagrams mean

Every diagram is a Mermaid code block inside Markdown. GitHub renders these as native diagrams. They describe a possible workflow rather than a working application. A flow arrow does not prove that two products are already connected. Complex diagrams should include a sentence telling the reader what to follow first.

## Evidence labels

- **Documented:** Confirmed in official standards or product documentation as of the reference date.
- **Illustrative:** A fictional business situation, draft process or example numbers.
- **Recommended:** Guidance based on business-control principles and stated trade-offs.
- **To verify:** Details such as licensing, quotas, languages, current models and regional support that readers must check for their own account.

## Boundaries

Do not present the handbook as a replacement for legal, accounting, medical or security professionals. Do not assume an application-level message to “never do X” is equivalent to a tool-level permission restriction. Do not publish sensitive customer or company records in a public repository.

## Keeping the book current

The original research date is 21 November 2026. Review model catalogs, connector availability and billing claims more often than conceptual lessons. Add or correct sources instead of silently altering historical wording. See the [research register](reference/05-research-method-and-feature-checks.md).
