Automating Your Personal Newsletter with Copilot
Purpose
This guide explains how to create and automate a personal newsletter using Microsoft Copilot. The newsletter summarizes your recent work highlights—customer engagements, ROI contributions, and kudos—by searching across your communications. It helps you stay organized and share updates with your team effortlessly.

The Prompt
Replace Fernando Berdugo Manzano with your name in the prompt below:
You are an AI assistant tasked with creating a personal newsletter for [your name].
Search across my communications from the last 14 days in Microsoft Teams chats, Outlook emails, meeting transcripts, documents, and MIX if available.
Extract and summarize the following:

1. **Customer Highlights**
   - Identify mentions of customer names, engagements, deliverables, or success stories.
   - Include context like project name, outcome, and any metrics or impact shared.

2. **ROI Highlights**
   - Capture any ROI-related achievements, advisory sessions, or analytics insights I contributed to.
   - Include references to tools (e.g., Super User Report, Copilot Dashboard) and measurable impact if mentioned.

3. **Kudos**
   - Find messages or emails where I expressed appreciation or recognition to colleagues.
   - Include sender, recipient, and reason for kudos.

Format the output as:
**Customer Highlights:** [bullet list with short summaries]
**ROI Highlights:** [bullet list with short summaries]
**Kudos:** [bullet list with From → To → Message]

Rules:
- Ignore duplicates and irrelevant chatter.
- Prioritize actionable insights and positive outcomes.
- Keep each bullet concise (max 20 words).
- If no data found for a section, write “No updates for this category.”

Input Variables:
- DateRange = Last 14 days
- Sources = Teams, Outlook, Transcripts, Documents, MIX


How to Automate It
You can schedule this prompt to run automatically every two weeks (every 15 days) using Copilot Automate Prompt:
Step-by-Step


Open Copilot Automate Prompt

Go to your Copilot dashboard and select Automate Prompt.



Create a New Automation

Click New Automation and paste the prompt above into the Prompt field.



Set Input Variables

DateRange: Last 14 days
Sources: Teams, Outlook, Transcripts, Documents, MIX



Configure Recurrence

Choose Frequency: Every 15 days
Select Start Date: Next Friday
Time: Pick a convenient hour (e.g., 9:00 AM).



Output Destination

Choose where the newsletter should appear:

Email (send to yourself or your team)
OneNote (shared section for team contributions)
Word file in SharePoint (for collaborative editing)





Save and Activate

Click Save and Activate. Copilot will now run this prompt automatically every two weeks.
