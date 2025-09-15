# Copilot-Growth-Newsletter-Agent
Below is a **ready-to-paste `README.md` section** focused on **how the agent works**.\
It ends with: **(a)** a short note about future phases + a placeholder for a **PowerPoint link**, and **(b)** a **“Replicate this agent in your organization”** section with a placeholder link to your step‑by‑step.

***

# ROI Newsletter Agent (ROI‑Pilot) — How It Works

## Purpose (What and Why)

**ROI‑Pilot** is a Copilot Studio agent that turns our weekly updates into a polished, **Outlook‑ready HTML newsletter** with one simple prompt.\
It removes the manual burden of **collecting inputs** and **formatting** the email, maintaining a consistent, friendly, and positive editorial voice.

***

## How It Works — At a Glance

*   **Inputs**:
    *   **Excel (SharePoint)** with 4 sheets (Engagement summary, Customer Highlights, ROI Team Highlights (individual), Kudos).
    *   **OneNote (SharePoint)** with the **latest ROI team meeting notes**.
*   **Action**: You open the agent and type **“Draft newsletter”**.
*   **Behind the scenes**:
    1.  A flow reads the 4 Excel tables and the OneNote page text.
    2.  The agent rewrites everything in a friendly, professional tone (“ROI‑Pilot”) and builds the newsletter using a predefined **HTML template** (inline CSS tables for Outlook).
*   **Output**: A **single HTML block** in the chat → **copy & paste into Outlook** → send.

***

## Data Sources and Structure

### Excel (SharePoint)

*   **Sheet 1 — Engagement summary** (`TblEngagementSummary`)\
    `Category | Count | Notes` (rows: Active, Completed, Won, Pending)
*   **Sheet 2 — Customer Highlights** (`TblCustomerHighlights`)\
    `Customer name | Licences total | Deliverable | Team member`
*   **Sheet 3 — ROI teams Highlights** (`TblROIHighlights`)\
    `Name | Highlights`
*   **Sheet 4 — Kudos** (`TblKudos`)\
    `From | To | Message`

> **Weekly reset**: After sending the newsletter, we clear the tables for the next cycle.

### OneNote (SharePoint)

*   Latest page in the **ROI Team Weekly** section contains last week’s **team meeting notes**.
*   The agent uses this to produce:
    *   **The most important update**
    *   **Team highlights narrative**

***

## Processing Logic (What the Agent Does)

1.  **Fetch**
    *   Calls a Power Automate **agent flow** to read:
        *   All rows from the 4 Excel tables.
        *   The latest OneNote page (converted to text).
2.  **Rewrite**
    *   Summarizes and rewrites in the voice of **ROI‑Pilot**: friendly, enthusiastic, positive, slightly humorous.
3.  **Format**
    *   Builds a single **HTML newsletter** with:
        *   **Engagement Summary** table (counts + one quick insight).
        *   **Customer Highlights** table (Customer, Licences, Deliverable, Team Member + short comment).
        *   **Team Highlights** from OneNote.
        *   **Individual Highlights** as a list.
        *   **Kudos** as a list.
    *   Uses **inline CSS** for Outlook compatibility.
4.  **Return**
    *   Displays the **HTML** in chat so you can **copy & paste** directly into Outlook.

***

## Weekly Runbook (Phase 1 – Current)

1.  **Update Excel** in SharePoint:
    *   Download interactions from **MiX** into **Sheet 1** (table).
    *   Update **Customer Highlights**, **ROI Team Highlights (individual)**, and **Kudos** on Sheets 2–4.
2.  Open the agent → type **“Draft newsletter”**.
3.  Review the HTML draft in chat.
4.  **Copy** the HTML → **paste** into Outlook → add recipients → **Send**.
5.  **Clear** Excel tables for next week.



***

## Roles

*   **Weekly Owner**: Updates Excel, runs **Draft**, reviews, sends, clears tables.
*   **Contributors**: Provide highlights/kudos via Excel (Phase 1).
*   **Agent Owner**: Maintains the agent instructions, flows, and Excel template.

***

## Guardrails & Notes

*   If a section has no data, the agent inserts a friendly placeholder (e.g., *“No updates this week—keep the momentum!”*).
*   Output is **HTML only** (email‑safe, inline styles).
*   The agent **does not auto‑send** in Phase 1; you stay in control.

***

## What’s Next (More Phases Coming)

*   **Phase 2**: Reminder notifications (e.g., **Fridays 09:00**) prompting updates and draft.
*   **Phase 3**: Employees submit highlights **via the agent** (guided Q\&A → writes to Excel). Optional owner approval → **auto‑send**.

**PowerPoint with the full roadmap and diagrams**:

> **\[Add link to the PowerPoint here]**

***

## Replicate This Agent in Your Organization

Use our step‑by‑step guide to create the Excel schema, flows, and agent instructions in your tenant.

> **\[Add link to your “How to create the agent step by step” guide here]**

***
