# Stoic Widget - Development Log

## Project Overview
A "Daily Stoic Quote" widget for embedding in Notion templates. Part of a premium Stoic productivity system ("The Stoa OS").

## Specs
- **468 curated quotes** from Marcus Aurelius, Seneca, Epictetus, and Alan Watts
- **Daily rotation** based on date (same quote all day, cycles yearly)
- **Auto dark/light mode** detection
- **Museum-quality aesthetic**: Cormorant Garamond serif, monochrome palette, minimal design
- **No external dependencies** - all quotes stored locally, no API calls

## Design Philosophy
- "Modern Museum" aesthetic: Dark Academia meets Swiss Minimalism
- Color palette: Marble White (#F5F5F5), Charcoal Grey (#2F2F2F), Void Black (#000000)
- Serif typography for "scholar/intellectual" feel
- Designed to match premium Notion template aesthetic

## Deployment
- **Repository**: https://github.com/sdb001/stoic-widget
- **Live URL**: https://sdb001.github.io/stoic-widget/
- **Hosted on**: GitHub Pages (main branch, root folder)

## Notion Integration

### Manual Embed
1. Type `/embed` in Notion
2. Paste: `https://sdb001.github.io/stoic-widget/`
3. Resize to ~400-500px height

### Pro Tip
Wrap in a transparent callout block for "museum plaque" look.

### MCP Integration
Added Notion MCP server for direct Claude-to-Notion access:
```bash
claude mcp add --transport http notion https://mcp.notion.com/mcp
```

## AI Prompts for Notion Template

### Feature 1: Cognitive Reframing Engine
For Daily Journal database - rewrites complaints into objective reality.

### Feature 2: Dichotomy of Control Sorter
For Problem Solver database - separates controllable vs uncontrollable.

### Feature 3: Premeditatio Malorum
For Project Planner - negative visualization exercise.

### Feature 4: Virtue Check
For Weekly Review - grades on Wisdom, Justice, Courage, Temperance.

## Files
- `index.html` - The complete widget (single file, self-contained)

## Quote Sources
- Marcus Aurelius: Meditations (~140 quotes)
- Seneca: Letters to Lucilius, On Anger, On Providence, etc. (~137 quotes)
- Epictetus: Enchiridion, Discourses (~96 quotes)
- Alan Watts: The Wisdom of Insecurity, The Book, The Way of Zen, etc. (~97 quotes)
