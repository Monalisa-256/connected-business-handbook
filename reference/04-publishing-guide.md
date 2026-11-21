# Put this handbook on GitHub and keep it useful

This ZIP is a **repository starter**: its contents are ready to place in a GitHub repository, but the ZIP itself is not a live online repository. No account connection or publication has been performed on your behalf.

## Publish using the GitHub website

1. Download the ZIP and unzip it on your computer.
2. Sign in to GitHub.
3. Create a new repository and choose a suitable name, such as `business-workforce-handbook`.
4. Decide whether it should be **public** or **private**. Use private if you plan to add internal policies, customer examples or account-specific materials.
5. If you are uploading this prepared folder, it is simplest to create the repository **without another README** first.
6. Open the repository's page, choose **Add file** → **Upload files**, and upload the unzipped Markdown files and folders using the browser's supported upload method. Keep the folder structure intact.
7. Commit the uploaded files with a short description, such as "Add business workforce handbook."
8. Open `README.md` in the repository. GitHub renders the links, tables, expandable sections and Mermaid diagrams.

If your browser does not preserve nested folders in one upload, use the automatic workflow method in [the updating guide](../IMPORTING-UPDATES.md), or upload them in smaller groups. **For first-time publication, do not upload the ZIP alone if you want individual chapters to be browsable in GitHub.** Once the separate import workflow is installed, future editions can be uploaded as `handbook-update.zip`, which is automatically unpacked. See [the updating guide](../IMPORTING-UPDATES.md).

## Easier first-time publication with the extractor workflow

Create an empty repository, install the separately supplied file at `.github/workflows/import-handbook.yml`, then upload `handbook-update.zip` at the repository root. GitHub Actions extracts the Markdown, adds the chapter folders, generates `FILE-INVENTORY.md`, and removes the temporary ZIP. This is the recommended method because it does not require you to move 130 files in the browser. Follow [the complete setup instructions](../IMPORTING-UPDATES.md).

## Make it yours

- Replace fictional examples with **anonymized** cases from your business.
- Add your chosen platform and product constraints to the project templates.
- Keep actual credentials, access tokens, payroll details and personal information out of the repository.
- Create a private record of the organization's real connections and approval owners.
- Check whether you want to add a license before inviting others to reuse or modify the text. Without an explicit license, standard copyright rules apply.

## Maintenance schedule

| Frequency | What to do |
|---|---|
| Monthly | Check external links and major feature changes |
| Quarterly | Review model-family and platform comparisons |
| After a workflow failure | Update the relevant scenario, safeguards and tests |
| After a company policy change | Update the real knowledge source; revise illustrative notes if necessary |
| Before public sharing | Review every example for private or commercially sensitive content |

## How to suggest a change

Open the chapter that needs improvement, propose a clear edit, and explain the real scenario it solves. Prefer concrete examples, verified references, and plain language over broad product claims.

## What these diagrams can and cannot do

Mermaid diagrams render as diagrams in GitHub Markdown. Expandable `<details>` sections open and close in the browser. Those are useful reading interactions, not a running software interface. To operate calendars, CRMs, mailboxes or payments, build the described workflows in a real platform with correct permissions.

## Maintain the repository after publication

Do not allow useful guidance to become a frozen sales presentation. Assign a person to review the vendor-specific chapters each quarter and whenever a major product change affects permissions, billing, integrations or model names. Keep the research reference date visible, and document substantial edits in the change log.

**Review checklist:** Open the README in GitHub and confirm the diagrams render; follow links to the major chapters; verify that internal relative paths resolve; try the expandable examples; check official vendor links; confirm there are no customer names, personal data, secret tokens or internal account URLs in the public content.

### Keep real operating documents private

The blank permission registers, testing forms and job cards can be published as examples. Completed versions containing sensitive customers, employee data, financial information or account details should be stored in the company's private workspace, not contributed to this public handbook.

### Suggested contribution workflow

1. Open an issue describing the section and business situation that need improvement.
2. Name the source or personal testing evidence behind a factual claim.
3. Make a focused change to one or a small group of Markdown files.
4. Check diagrams, links and examples in the GitHub preview.
5. Request review from an owner of the subject matter.
6. Record the review date for any fast-changing product guidance.

A reader should always be able to distinguish **what a vendor documents**, **what the handbook recommends**, and **what a fictional example illustrates**.

## Future editions without duplicate folders

Follow [the handbook ZIP updating guide](../IMPORTING-UPDATES.md). Upload the next complete edition as `handbook-update.zip` at the repository root. The workflow validates and unpacks it, updates the Markdown inventory, removes old managed chapters, and deletes the temporary ZIP. Keep the workflow file separate from the handbook archive.
