# 📋 3-PART PROMPT UPLOAD GUIDE

Your chatbot now has **3 separate prompt sections** to paste into GoHighLevel:

---

## SECTION 1: PERSONALITY
**GHL Field:** "Personality" or "Character" or "Bot Identity"

**File to Copy:** `personality_prompt.txt`

**What it does:** Makes your bot "Élise"—an upbeat French-born wellness educator who greets with "Bonjour!" and has warm, encouraging energy.

**How to upload:**
1. Open `personality_prompt.txt`
2. Copy ALL text (Ctrl+A, Ctrl+C)
3. Paste into the "Personality" field in GHL
4. Save

---

## SECTION 2: GOAL
**GHL Field:** "Goal" or "Objectives" or "Mission"

**File to Copy:** `goal_prompt.txt`

**What it does:** Defines the 4-Step Trust Sequence (Science → Behavior → Product → Consultation) and research citation priority.

**How to upload:**
1. Open `goal_prompt.txt`
2. Copy ALL text (Ctrl+A, Ctrl+C)
3. Paste into the "Goal" field in GHL
4. Save

---

## SECTION 3: ADDITIONAL INFORMATION
**GHL Field:** "Additional Information" or "Context" or "Knowledge Base Instructions"

**File to Copy:** `additional_info_prompt.txt`

**What it does:** Specifies which training files to use, how to cite research, safety guardrails, and anti-jailbreak rules.

**How to upload:**
1. Open `additional_info_prompt.txt`
2. Copy ALL text (Ctrl+A, Ctrl+C)
3. Paste into the "Additional Information" field in GHL
4. Save

---

## ✅ FINAL CHECKLIST

After uploading all 3 sections, your bot should:
- ✅ Greet with "Bonjour!" 
- ✅ Cite research (Lee et al., RCTs, meta-analyses)
- ✅ Give 150-200 word responses
- ✅ Follow Science → Behavior → Product → Consultation order
- ✅ Have warm, upbeat French personality

---

## 🧪 TEST YOUR BOT

**Ask:** "Bonjour! Why do I get brain fog?"

**Expected Response:**
- Should greet back warmly
- Should mention the Glymphatic System
- Should cite Lee et al. 2015
- Should be 150-200 words
- Should have upbeat, encouraging tone

---

## 🛠️ TROUBLESHOOTING

**Bot not saying "Bonjour"?**
- Make sure you pasted `personality_prompt.txt` into the Personality field

**Bot still giving short responses?**
- Check that `goal_prompt.txt` is in the Goal field (it specifies 150-200 words)

**Bot not citing research?**
- Verify `additional_info_prompt.txt` is in the Additional Information field
