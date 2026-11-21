# Other no-code routes: Microsoft, Google, Zapier, and voice

You do not need to rebuild office infrastructure merely to add useful assistants. Existing business software may already contain the relevant automation tools.

## Microsoft: Copilot Studio and Power Automate

**Best starting point:** An organization already using Microsoft 365, SharePoint, Teams, and Power Platform.

A useful first job is an internal staff-policy assistant: an employee asks a leave-policy question, the assistant consults an approved handbook, and sends uncertain cases to HR. A second, more operational job might extract invoice fields into an approval queue using Power Automate and AI Builder.

Visual setup typically involves selecting knowledge sources, creating an agent, attaching suitable tools or workflows, testing conversations, and choosing how staff access it. Administrative controls and licenses matter. [Copilot Studio](https://learn.microsoft.com/en-us/microsoft-copilot-studio/) · [AI Builder in flows](https://learn.microsoft.com/en-us/ai-builder/use-in-flow-overview) · [MCP extensions](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agent-extend-action-mcp).

## Google: Workspace Studio

**Best starting point:** A business using Gmail, Google Drive, Google Docs, Sheets and Calendar.

Try a routine such as: "When a form arrives, extract the main request, add a row to a tracking sheet, and notify the responsible owner." Keep a human review step before outgoing messages. Google describes Workspace Studio as a no-code environment for automating work with Workspace apps. [Workspace Studio](https://workspace.google.com/studio/).

Do not assume Workspace Studio and Google Cloud's MCP offerings are identical. Google Workspace MCP connections may require additional configuration and administrator oversight. [Workspace MCP information](https://developers.google.com/workspace/guides/configure-mcp-servers).

## Zapier: app-based routines

**Best starting point:** A simple chain across apps such as forms, email, task boards, and spreadsheets.

Example: a new event registration creates a contact, adds a note to a sheet, and alerts the organizer. The owner should review consent and whether duplicates can occur. Zapier also documents its own MCP offering for exposing app actions to compatible tools. [Zapier help](https://help.zapier.com/) · [Zapier MCP](https://help.zapier.com/hc/en-us/articles/48308034391821-What-is-Zapier-MCP).

Products and feature names change. Prefer current official instructions over older videos showing discontinued or renamed agent interfaces.

## Voiceflow and ElevenLabs: telephone or spoken work

**Best starting point:** A receptionist-style job with a defined question set and a human transfer route.

A suitable pilot answers opening hours, service descriptions, and appointment preparation questions. Test accents, background noise, slow callers, interrupted speech, names, dates, and handoff to a person. Do not allow a spoken assistant to claim an appointment exists until the calendar returns confirmation.

[Voiceflow](https://www.voiceflow.com/) · [ElevenAgents](https://elevenlabs.io/docs/eleven-agents/overview).

## A note about WhatsApp and other messaging channels

Messaging channels often impose separate rules on customer consent, message templates, and automated replies. Availability depends on approved integrations and account setup. WhatsApp Business Platform rules are documented by [Meta](https://business.whatsapp.com/policy). A generic no-code subscription does not automatically grant unrestricted sending rights.

## Simple platform decision

If the main job is **internal documents**, start with the office suite already in use. If it is **app-to-app execution**, start with a visual automation builder. If it is **multi-specialist handoffs**, evaluate a workforce canvas. If it is **telephone reception**, choose a voice platform first.

## How to shortlist without buying five subscriptions

Start with the organization's current work environment. Microsoft-heavy organizations should evaluate Copilot Studio and Power Automate before adding an unrelated builder. Google-heavy organizations should examine Workspace Studio. Businesses spanning many apps can pilot Make, Zapier or n8n. A genuinely complex team of specialists may justify a workforce canvas, while telephone reception may justify Voiceflow or ElevenLabs.

For each option, choose one **realistic pilot task** and require the same proof: the correct data source, a draft or permitted action, human review where necessary, a verifiable result, and a clear error path. Product screenshots do not replace this test.

### Beware of feature assumptions

A tool may support voice on one channel but not another. Human transfer on web chat may not exist in a particular WhatsApp integration. An enterprise product may require administrator activation or a suitable plan. Check the specific edition, region, channel and current help documentation before relying on the workflow.

[Platform selection workshop](13-platform-decision-workshop.md)
