# UPLOAD GUIDE: PERFECTING YOUR BOT

You have 30 minutes to perfect this bot. Here is exactly where to put the new files I created for you.

## 1. THE BRAIN (System Prompt)
**File:** `system_prompt_exhaustive.txt`
**Where to put it:**
1.  Go to your **GoHighLevel Dashboard**.
2.  Navigate to **Automation > Chatbots > [Your Bot]**.
3.  Find the **"Bot Settings"** or **"General"** tab.
4.  Look for the **"System Prompt"** or **"Persona Instructions"** field.
5.  **Paste the entire content** of `system_prompt_exhaustive.txt` into this field.
6.  *Tip: This gives the bot its personality, rules, and "Golden Rules" for safety.*

## 2. THE KNOWLEDGE (Training Materials)
**Files:**
1.  `master_training_materials.md` (The "One Source of Truth")
2.  `comprehensive_product_catalog.md` (The "Product Brain")

**Where to put them:**
1.  In the same **Chatbot Settings**, find the **"Knowledge Base"** or **"Training"** tab.
2.  Select **"Add Source"** or **"Upload Document"**.
3.  **Upload BOTH files.**
    *   *Note: If GHL requires PDF or Text, you can rename these files to .txt or print them to PDF.*
4.  These files contain **EVERYTHING**: The Consultant Manual, The Science, The Protocols, and the detailed Product Logic.

## 3. THE PRODUCT DATABASE (Structured Data)
**File:** `ghl_knowledge_base.json` (Existing file, already ready)
**Where to put it:**
1.  In the **"Knowledge Base"** section, look for an option to **"Import FAQs"** or **"Import JSON"**.
2.  Upload `ghl_knowledge_base.json`.
3.  This allows the bot to pull specific product details (Price, URL, Image) accurately when asked specific questions like "How much are the leggings?".

## 4. THE VISUALS (Product Tiles)
**File:** `ghl_product_tiles.json` (Existing file, already ready)
**How to use it:**
1.  Keep this file open on your computer.
2.  When you are building **Workflows** or **Canned Responses** in GHL, copy the HTML code from this file to show beautiful product cards in the chat.

---

## QUICK CHECKLIST
- [ ] **System Prompt** updated with `system_prompt_exhaustive.txt`.
- [ ] **Master Training** uploaded (`master_training_materials.md`).
- [ ] **FAQs** imported (`ghl_knowledge_base.json`).
- [ ] **Test:** Ask the bot "How do I reduce cellulite?" and see if it mentions MicroPerle and recommends a product.
