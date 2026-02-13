# Create Jamie Tech Guide

This command creates a Jamie-friendly technical guide — teaching tools like Claude Code, Claude Skills, Midjourney, etc. in a way that feels doable for non-technical creatives. The goal is a guide that leaves Jamie thinking "I CAN do this" rather than "this isn't for me."

## Before Starting

Read the Hey Claude strategy file to have Jamie (the reader persona) fresh:
- `~/Documents/WRITING/Hey Claude/hey-claude-strategy.md`

---

## PHASE 1: Understand the Topic

### Step 1: Get the Topic and Any Existing Material

Ask:
> "What tool or topic do you want to create a guide for? And do you have any existing material — like notes, a draft, or something from another AI — that I should look at first?"

If they have a draft:
- Read it carefully
- Note what's useful (structure, research, ideas)
- Note what doesn't speak Jamie's language (jargon, tutorial-speak, overwhelming detail)

### Step 2: Clarify the Scope

Ask:
> "What should Jamie be able to DO after reading this guide? What's the one thing you want them to walk away with?"

The guide should have ONE clear outcome — not "everything about X" but "get started with X" or "understand what X is and try one thing."

---

## PHASE 2: Research for Accuracy

### Step 1: Gather Accurate Information

Use appropriate research tools:
- **For Claude Code / Claude features**: Use the `claude-code-guide` agent
- **For other tools**: Use WebSearch or WebFetch
- **For technical accuracy**: Verify installation steps, commands, current features

### Step 2: Identify What Jamie Actually Needs

From the research, extract:
- **Minimum viable setup** — What's the absolute simplest path to get started?
- **First "oh wow" moment** — What can they try in under 5 minutes that shows the value?
- **Common fears to address** — What might scare them off? (jargon, complexity, "breaking something")
- **Visual/easy alternatives** — Are there GUI options instead of command-line? Drag-and-drop instead of typing?

---

## PHASE 3: Draft the Guide

### Voice and Tone

Write as if you're sitting next to Jamie, walking them through it:
- Warm and direct, not formal or educational
- "I know. That's fine." energy
- Anticipate their fears and address them casually
- No jargon without immediate, plain-English explanation
- Short paragraphs, clear steps

### Structure Template

Most guides will follow this pattern (adapt as needed):

1. **What is [X], actually?**
   - Simple metaphor comparing to something they already know
   - What makes it different from alternatives they might have tried
   - Why it matters for someone like them

2. **"But I'm not technical."**
   - Address the fear directly
   - List what they DON'T need
   - List what they DO need (keep it minimal)
   - Reassure them about safety/control

3. **Getting Started: [N] Steps**
   - Numbered steps with clear actions
   - Include both Mac and Windows instructions where relevant
   - Offer visual/GUI alternatives when available (e.g., right-click instead of terminal commands)
   - Each step should be completable without confusion

4. **Your First [Conversation/Project/Creation]**
   - One specific thing to try
   - Exact prompts or inputs to use
   - What they'll see/experience
   - This is the "oh wow" moment

5. **A Few More Things to Try**
   - 3-5 simple prompts or actions
   - Organized by use case ("If you want to...")
   - Low stakes, exploratory

6. **When You're Ready for More**
   - Brief mention of advanced possibilities
   - No pressure — "that's for later"
   - Links or breadcrumbs for the curious

7. **Quick Reference**
   - Essential commands/steps in one place
   - Copy-paste friendly
   - Both platforms if applicable

### Key Principles

- **Lead with the easy way** — If there's a visual alternative to typing commands, show that first
- **Both platforms** — Always include Mac and Windows instructions
- **Actual prompts** — Don't just describe what to type; show the exact text
- **End with possibility** — Jamie should close feeling excited, not overwhelmed

---

## PHASE 4: Iterate and Finalize

### Step 1: Present the Draft

Share the complete guide and ask:
> "Here's the draft. Read through it — anything feel confusing, scary, or missing?"

### Step 2: Address Feedback

Common things to check:
- Missing steps between actions (e.g., "how do I exit before navigating?")
- Platform-specific differences not covered
- Jargon that slipped through
- Steps that assume too much knowledge

### Step 3: Save the Final Guide

Save to the Tech Guides folder:
```
~/Documents/WRITING/Hey Claude/Tech Guides/[topic-name].md
```

Use kebab-case for filenames (e.g., `getting-started-with-claude-code.md`, `intro-to-midjourney.md`)

---

## PHASE 5: Publish & Track

### Step 1: Add to Notion Substack Posts DB

After the guide is published on Substack, create an entry in the Substack Posts database:

**Data Source ID:** `2a908620-e1b0-80ad-8d78-000bc8f9d2cd`
**Publication (Hey Claude):** `https://www.notion.so/2a908620e1b080779c7ddcc26e8f00f4`

Set these properties:
- **Title:** Guide title
- **Post Type:** Tech Guide
- **Link:** Published Substack URL
- **Published Date:** Publication date
- **Publication:** Hey Claude
- **Premise:** 3-8 word core idea
- **Audience:** Builders
- **SEO Keywords:** Relevant search terms

### Step 2: Create Task to Add Guide to Master Guide

Create a Notion task reminding Olena to add this new guide to the master guide page:

**Tasks DB data source ID:** `2a708620-e1b0-807e-b3eb-000b698751cc`
**Project (Hey Claude):** `https://www.notion.so/2a708620e1b081dfba5cda0514b7f74b`

Task title: `Add [guide name] to master Claude Code guide`
Task description: Include the guide URL and a brief note about where it fits in the master guide's structure.

**Master guide:** https://olenamytruk.substack.com/p/claude-code-for-creatives

---

## What Success Looks Like

By the end of this process:
- Jamie can follow the guide from zero to "I did the thing"
- No step requires Googling or prior knowledge
- The tone feels like a friend helping, not a tutorial lecturing
- Jamie finishes thinking "This is actually for someone like me"
- Guide is tracked in Notion and queued to be added to the master guide

---

## Reference: Existing Guides

Check existing guides for consistency:
- `~/Documents/WRITING/Hey Claude/Tech Guides/`
- **Master guide:** https://olenamytruk.substack.com/p/claude-code-for-creatives
- **Individual guides:** Your first day with Claude Code, Giving Claude Code a memory, Make friends with Claude Code commands
