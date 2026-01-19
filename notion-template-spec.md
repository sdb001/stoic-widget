# The Stoic Journal - Notion Template Spec

## Page Structure

```
📜 The Stoic Journal
├── [Embed: Daily Quote Widget]
├── 🌅 Today's Practice (linked view of Daily Entries, filtered to today)
├── 📖 Journal Archive (full Daily Entries database)
├── 🎯 Virtue Goals (Goals database)
└── 🏛️ AI Stoic Mentor (AI buttons page)
```

---

## Database 1: Daily Entries

**Properties:**

| Property | Type | Options/Notes |
|----------|------|---------------|
| Date | Title | Format: "January 19, 2025" |
| Mood | Select | 😤 Frustrated, 😔 Low, 😐 Neutral, 🙂 Good, 😊 Great |
| Virtue Focus | Select | 🦉 Wisdom, 🦁 Courage, ⚖️ Justice, 🧘 Temperance |
| Morning Complete | Checkbox | |
| Evening Complete | Checkbox | |
| Created | Created time | Auto |

**Page Content Template:**

```markdown
## ☀️ Morning Reflection
*Premeditatio Malorum — Prepare for the day ahead*

### What do I intend to accomplish today?
[Write here]

### What obstacles might I face? How will I respond?
[Write here]

### Which virtue will I practice today?
[Select Virtue Focus property above]

---

## 🌙 Evening Reflection
*Examen Conscientiae — Review the day that was*

### What went well today? When did I practice virtue?
[Write here]

### What am I grateful for?
[Write here]

### What could I have done better? What will I improve tomorrow?
[Write here]

---

## 🏛️ Stoic Mentor
*Need guidance? Use these AI tools:*

[🔄 Reframe This] [🏛️ Ask the Sages] [⚖️ Dichotomy of Control]
```

---

## Database 2: Virtue Goals

**Properties:**

| Property | Type | Options/Notes |
|----------|------|---------------|
| Goal | Title | The goal text |
| Virtue | Select | 🦉 Wisdom, 🦁 Courage, ⚖️ Justice, 🧘 Temperance |
| Status | Status | Not started, In progress, Complete |
| Target Date | Date | Optional |
| Reflections | Text | Notes on progress |

**Default Goals (pre-populate):**

1. 🦉 Wisdom: "Practice negative visualization daily"
2. 🧘 Temperance: "Respond, don't react to frustrations"
3. 🦁 Courage: "Have one difficult conversation I've been avoiding"
4. ⚖️ Justice: "Compliment someone genuinely each day"

---

## Database 3: Wisdom Archive (Optional)

For saving AI mentor responses worth keeping.

| Property | Type |
|----------|------|
| Insight | Title |
| Type | Select (Reframe, Sage Wisdom, Dichotomy) |
| Original Challenge | Text |
| Date | Date |

---

## AI Mentor Page

### Header
```
╔═══════════════════════════════════════════════════════════╗
║                                                           ║
║                    🏛️ THE STOIC MENTOR                    ║
║                                                           ║
║       "Most journals listen. This one talks back."        ║
║                                                           ║
╚═══════════════════════════════════════════════════════════╝
```

### Instructions Callout
> Write your challenge, frustration, or dilemma below. Then click one of the mentor buttons to receive Stoic guidance.

### Input Area
```
───────────────────────────────────────
What's on your mind?

[Your text here]

───────────────────────────────────────
```

### AI Buttons (see prompts below)

---

## AI Button Prompts

### 🔄 Reframe This
```
You are a Stoic philosophy mentor. Reframe the text above through a Stoic lens:

1. OBSERVE: Summarize the situation objectively, without emotional language
2. CONTROL: Identify what is within my control and what is not
3. REFRAME: Offer a Stoic perspective that transforms this challenge into an opportunity for growth
4. PRACTICE: Suggest one concrete action I can take today
5. WISDOM: End with a relevant quote from Marcus Aurelius, Seneca, or Epictetus

Keep the tone warm but direct. Be concise.
```

### 🏛️ Ask the Sages
```
You are channeling three Stoic philosophers. Based on the text above, provide wisdom from each:

**Marcus Aurelius** (The Emperor)
As a leader who faced constant challenges, what would Marcus say about this situation? Draw from Meditations.

**Seneca** (The Advisor)
As a practical philosopher who dealt with politics, wealth, and exile, what advice would Seneca offer? Be direct and actionable.

**Epictetus** (The Former Slave)
As someone who found freedom through philosophy despite external bondage, how would Epictetus reframe this? Focus on what is "up to us."

End with one unified insight they would all agree upon.
```

### ⚖️ Dichotomy of Control
```
Apply the Stoic Dichotomy of Control to the text above.

Create two columns:

**✅ WITHIN MY CONTROL (Focus here)**
- List thoughts, actions, and responses I can control
- Be specific and actionable

**❌ OUTSIDE MY CONTROL (Release these)**
- List external events, others' actions, outcomes I cannot control
- Explain why energy spent here is wasted

**🎯 VERDICT**
Based on this analysis, what is the ONE thing I should focus my energy on right now?

Quote Epictetus: "Make the best use of what is in your power, and take the rest as it happens."
```

### 💀 Memento Mori
```
Apply the Stoic meditation on mortality (Memento Mori) to the text above.

Consider: If this were your last year, month, or week—would this challenge still consume you?

1. PERSPECTIVE: How does awareness of limited time change the weight of this problem?
2. PRIORITIES: What truly matters when viewed against the backdrop of mortality?
3. ACTION: What would you regret NOT doing if you spent too long on this worry?
4. URGENCY: How can mortality awareness motivate rather than paralyze?

"You could leave life right now. Let that determine what you do and say and think." — Marcus Aurelius
```

### 🔥 Amor Fati
```
Apply Amor Fati (love of fate) to the text above.

The Stoics taught that we should not merely accept what happens, but love it—seeing every event as necessary and beneficial.

1. ACCEPTANCE: Restate this situation as a neutral fact, stripped of judgment
2. NECESSITY: How might this challenge be exactly what was needed for growth?
3. OPPORTUNITY: What strength, skill, or wisdom can ONLY be developed through this difficulty?
4. EMBRACE: Write an affirmation that transforms resistance into acceptance

"Do not seek for things to happen the way you want them to; rather, wish that what happens happen the way it happens: then you will be happy." — Epictetus
```

---

## Views to Create

### Daily Entries Database Views

1. **Today** (Default)
   - Filter: Date = Today
   - Layout: Page view

2. **This Week**
   - Filter: Date is within past week
   - Layout: Table
   - Sort: Date descending

3. **Calendar**
   - Layout: Calendar by Date

4. **By Mood**
   - Layout: Board by Mood property

### Virtue Goals Database Views

1. **Active Goals**
   - Filter: Status ≠ Complete
   - Group by: Virtue

2. **Completed**
   - Filter: Status = Complete
   - Sort: Completed date descending

---

## Styling Notes

- Use `---` dividers between sections
- Use callout blocks (grey ▫️) for instructions
- Use quote blocks for Stoic quotes
- Corner decoration can be added with: `╔═══╗` style boxes
- Keep color minimal: grey callouts, no colored backgrounds
- Font: Notion default (Serif option if available)

---

## Embed Widget

Embed URL: `https://sdb001.github.io/stoic-widget/journal-header.html`

The widget displays:
- Daily Stoic quote (rotates by date)
- Minimal, museum aesthetic
- Auto dark/light mode

Recommended size: Full width, 200px height
