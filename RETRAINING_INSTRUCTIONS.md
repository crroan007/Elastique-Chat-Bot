# 🚀 Bot Retraining Instructions (Gemini Pro Spec)

Follow these exact steps to update your GoHighLevel (GHL) bot with the new "Consultative Driver" logic and Research Library.

## Phase 1: Knowledge Base Cleanup
1.  Go to **Settings > AI Chatbot > Knowledge Base**.
2.  **DELETE** all old files (especially `.md` or older `.docx` files). We want a clean slate to prevent conflicting information.

## Phase 2: Upload New Training Data
Upload the following **9 files** (all in `.docx` format) from your `Elastique - GPT_chatbot` folder:

| File Name | Purpose |
| :--- | :--- |
| `01_Science_and_Behavior.docx` | Core physiology, Rebounding, & Evidence Pillars. |
| `02_Product_Catalog.docx` | Product details & links (unchanged but essential). |
| `03_Consultation_and_Logistics.docx` | Provider matching, safety, & consultation offers. |
| `04_Research_Library.docx` | **NEW:** Full Huberman & clinical study library. |
| `05_Protocol_Templates.docx` | **NEW:** Logic for building Daily/Weekly protocols. |
| `06_Provider_Directory_Structure.docx` | **NEW:** Template for finding local therapists. |
| `07_Master_Research_Table.docx` | **NEW:** The "Brain" & "Driver" logic (Questions -> Actions). |
| `exhaustive_faq.docx` | Master FAQ (now includes Rebounding). |
| `PRODUCT_NAVIGATION_GUIDE.docx` | Logic for handling product overlaps. |

> **Tip:** Select all `.docx` files in the folder and drag-and-drop them into GHL.

## Phase 3: Update Prompts
Go to **Settings > AI Chatbot > Bot Settings** (or Custom Values, depending on your setup) and replace the text with the contents of these files:

1.  **Personality / System Prompt:**
    *   *Source File:* `personality_prompt.txt`
    *   *Key Change:* New "Extended Delta Family" tone & specific opening questions.

2.  **Goal / Instruction Prompt:**
    *   *Source File:* `goal_prompt.txt`
    *   *Key Change:* **"Driver Flow"** logic (Consult -> Build -> Suggest -> Upsell).

3.  **Additional Info / Guardrails:**
    *   *Source File:* `additional_info_prompt.txt`
    *   *Key Change:* New Evidence Pillars (including Rebounding) & Safety Rules.

## Phase 4: Test the "Driver" Flow
Once saved, open the **Bot Simulator** and test this specific flow to verify the new logic:

1.  **Say:** "Hi"
    *   *Verify:* Bot **DOES NOT** ask the 4 opening questions. It should greet you warmly.
    *   *Note:* In the simulator, the bot won't have the contact form data yet, so it might just say "Hello! How can I help you today?" This is correct.
2.  **Say:** "I want to fix my cellulite."
    *   *Verify:* Bot asks the **Driver Questions** from the table (e.g., "Is it mainly on thighs?").
3.  **Say:** "Thighs mostly. And I have a rebounder."
    *   *Verify:* Bot suggests a protocol including **Rebounding** and recommends **MicroPerle leggings**.
4.  **Say:** "Can I find a massage therapist for this?"
    *   *Verify:* Bot asks for your City/Zip to check the directory.

## Phase 5: Provider Data (Action Item)
*   **Note:** The bot currently has a *template* for provider matching (`06_Provider_Directory_Structure.docx`).
*   **To make it real:** You need to upload your actual list of providers (Name, City, Link) as a CSV or Doc to the Knowledge Base so the bot has real people to recommend.
