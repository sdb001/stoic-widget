# The Stoic Journal - Notion Setup Guide

## Quick Start

### 1. Deploy the Header Widget

```bash
cd /Users/samb/Desktop/stoic-widget
git add journal-header.html
git commit -m "Add journal header widget"
git push
```

Embed URL: `https://sdb001.github.io/stoic-widget/journal-header.html`

---

### 2. Create the Main Page

1. Create a new Notion page: **"The Stoic Journal"**
2. Add the embed at the top:
   - Type `/embed`
   - Paste: `https://sdb001.github.io/stoic-widget/journal-header.html`
   - Resize to full width, ~160px height

---

### 3. Create Daily Entries Database

1. Type `/database` → Select **"Table - Inline"**
2. Name it: **"Daily Entries"**
3. Set up properties:

| Property | Type | Configuration |
|----------|------|---------------|
| Date | Title | Rename from "Name" |
| Mood | Select | Options: 😤 Frustrated, 😔 Low, 😐 Neutral, 🙂 Good, 😊 Great |
| Virtue Focus | Select | Options: 🦉 Wisdom, 🦁 Courage, ⚖️ Justice, 🧘 Temperance |
| Morning Done | Checkbox | |
| Evening Done | Checkbox | |

4. Create a **Template**:
   - Click dropdown arrow next to "New" → "New template"
   - Name: "Daily Entry"
   - Add this content to the template page:

```
## ☀️ Morning Reflection
*Premeditatio Malorum — Prepare for the day ahead*

### What do I intend to accomplish today?


### What obstacles might I face? How will I respond?


### Which virtue will I practice today?


---

## 🌙 Evening Reflection
*Examen Conscientiae — Review the day that was*

### What went well today? When did I practice virtue?


### What am I grateful for?


### What could I have done better?


---

## 🏛️ Need Guidance?

> Write your challenge below, then use an AI button:

[Your challenge here]

```

5. Add **AI Buttons** to the template (see Step 5 below)

---

### 4. Create Virtue Goals Database

1. Type `/database` → **"Table - Inline"**
2. Name: **"Virtue Goals"**
3. Properties:

| Property | Type | Configuration |
|----------|------|---------------|
| Goal | Title | |
| Virtue | Select | 🦉 Wisdom, 🦁 Courage, ⚖️ Justice, 🧘 Temperance |
| Status | Status | Not started, In progress, Complete |

4. Add starter goals:
   - 🦉 "Practice negative visualization daily"
   - 🧘 "Respond, don't react to frustrations"
   - 🦁 "Have one difficult conversation I've been avoiding"
   - ⚖️ "Compliment someone genuinely each day"

---

### 5. Add AI Mentor Buttons

In your Daily Entry template (or a separate AI Mentor page):

1. Type `/button` → "Button"
2. Name: **🔄 Reframe This**
3. Click the button → Add action → "AI: Custom"
4. Paste this prompt:

```
You are a Stoic philosophy mentor. Reframe the text above through a Stoic lens:

1. OBSERVE: Summarize the situation objectively, without emotional language
2. CONTROL: Identify what is within my control and what is not
3. REFRAME: Offer a Stoic perspective that transforms this challenge into growth
4. PRACTICE: Suggest one concrete action I can take today
5. WISDOM: End with a relevant quote from Marcus Aurelius, Seneca, or Epictetus

Be warm but direct. Be concise.
```

Repeat for other buttons:

**🏛️ Ask the Sages**
```
Channel three Stoic philosophers on the text above:

**Marcus Aurelius** (The Emperor)
What would the philosopher-king say? Draw from Meditations.

**Seneca** (The Advisor)
What practical advice would Seneca offer? Be direct and actionable.

**Epictetus** (The Former Slave)
How would Epictetus reframe this? Focus on what is "up to us."

End with one unified insight they would all agree upon.
```

**⚖️ Dichotomy of Control**
```
Apply the Stoic Dichotomy of Control to the text above.

**✅ WITHIN MY CONTROL**
- List specific thoughts, actions, responses I can control

**❌ OUTSIDE MY CONTROL**
- List external events, others' actions, outcomes I cannot control

**🎯 VERDICT**
What ONE thing should I focus my energy on right now?

"Make the best use of what is in your power, and take the rest as it happens." — Epictetus
```

**💀 Memento Mori**
```
Apply meditation on mortality to the text above.

If this were your last year—would this still consume you?

1. PERSPECTIVE: How does mortality awareness change this problem's weight?
2. PRIORITIES: What truly matters against the backdrop of death?
3. ACTION: What would you regret NOT doing?
4. URGENCY: How can this motivate rather than paralyze?

"You could leave life right now. Let that determine what you do and say and think." — Marcus Aurelius
```

---

### 6. Create Views

**Daily Entries views:**
- **Today**: Filter → Date = Today
- **This Week**: Filter → Date is within past 7 days
- **Calendar**: Layout → Calendar
- **By Mood**: Layout → Board, Group by Mood

**Virtue Goals views:**
- **Active**: Filter → Status ≠ Complete, Group by Virtue
- **Completed**: Filter → Status = Complete

---

### 7. Final Page Structure

Your finished page should look like:

```
┌─────────────────────────────────────────────┐
│     [Embedded Quote Header Widget]          │
├─────────────────────────────────────────────┤
│                                             │
│  🌅 Today's Practice                        │
│  ┌─────────────────────────────────────┐    │
│  │ [Daily Entries - Today view]        │    │
│  └─────────────────────────────────────┘    │
│                                             │
│  📖 Journal Archive                         │
│  ┌─────────────────────────────────────┐    │
│  │ [Daily Entries - Calendar view]     │    │
│  └─────────────────────────────────────┘    │
│                                             │
│  🎯 Virtue Goals                            │
│  ┌─────────────────────────────────────┐    │
│  │ [Goals - Active view]               │    │
│  └─────────────────────────────────────┘    │
│                                             │
└─────────────────────────────────────────────┘
```

---

## Files Reference

- `journal-header.html` - Embed widget (deploy to GitHub Pages)
- `notion-template-spec.md` - Full technical spec
- `index.html` - Original quote widget (already deployed)

---

## Tips

- Set Today view as default for quick daily access
- Pin the template button for easy new entries
- Use the Calendar view for streak visualization
- Morning: Fill top section + set Virtue Focus
- Evening: Fill bottom section + check boxes
