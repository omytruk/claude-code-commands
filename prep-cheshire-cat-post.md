# Prepare The Cheshire Cat Lab Substack Post for Publication

This command helps prepare The Cheshire Cat Lab Substack post from Ulysses for publication.

## Task Overview

You will help prepare a Substack post through the following steps:
1. **Initial Draft Review** (Optional) - Flow, structure, headings, formatting, contractions
2. **Proofreading & Cleanup** - Three-tier approach
3. **SEO-Friendly URL** - Generate URL from heading (with duplicate check)
4. **Midjourney Prompt** - Create feature image prompt
5. **Cross-Linking** - Add links between posts
6. **Notion Update** - Add post to database with Draft Link, Premise, Audience, SEO Keywords

---

## Step 1: Read the Ulysses Post

**Default location:** `~/Library/Mobile Documents/X5AZV975AG~com~soulmen~ulysses3/Documents/Projects/3fdd49b6001145a796bc6704fc280765-ulproject/`

**The Cheshire Cat Lab Project ID:** `3fdd49b6001145a796bc6704fc280765-ulproject`

1. Find the most recently edited document in the Main-ulgroup folders (check `Metadata.plist` for `lastEditingDate`)
2. Read the `Content.xml` file to get post content
3. Extract title and subtitle from the XML

---

## Step 1.5: Initial Draft Review (Optional)

**Use this step if the post is a rough draft that needs structural work before detailed proofreading.**

Ask the user if they need this initial review. If yes, perform the following in order:

### A. Flow & Language Check
Read the full draft and identify:
- Flow issues (abrupt transitions, missing bridges between sections)
- Language inconsistencies (tone shifts, unclear phrasing)
- Overall coherence of argument/narrative

Provide concise feedback on these issues.

### B. Structure & Headings
Check if the post has:
- Title (H1) and subtitle (H3)
- Section headings (H2) that break up the content logically
- Clear narrative or argumentative structure

Suggest headings if missing, or propose improvements to existing structure.

### C. Formatting Review
Review and suggest improvements for:
- **Bold text** - Should highlight key terms, frameworks, structural elements (e.g., "First," "Second")
- *Italic text* - Should emphasize conceptual ideas and key concepts
- Ensure formatting is purposeful and guides the reader through the argument

### D. Contractions Consistency
Check for consistent contraction usage:
- **Full forms** in narration/analysis ("was not," "does not," "cannot")
- **Contractions** in personal moments and dialogue ("I'm," "can't," "wasn't")
- Flag any inconsistencies and suggest corrections

**After completing this step:** The draft should have clear structure, consistent voice, and purposeful formatting. Now ready for detailed proofreading.

---

## Step 2: Proofreading & Cleanup

Use the **three-tier approach**:

### TIER 1: Minor Fixes
Create a quick list of:
- Typos
- Grammar errors
- Punctuation issues
- Spacing problems

Format as a simple numbered list the user can quickly scan and fix.

### TIER 2: Substantial Edits
For each substantial suggestion, provide:
- **Location:** Which section/paragraph
- **Issue:** Why it could be improved
- **Suggestion:** Specific recommendation with before/after

Focus on:
- Clarity and flow
- Repetition
- Missing links or placeholders
- Paragraph length (break up long ones)
- Strengthening conclusion/CTAs
- Subtitle alternatives

**Voice Guidelines for The Cheshire Cat Lab:**
- Tone: Exploratory, curious, philosophical, wonder-filled
- Style: Literary essay format, thoughtful, inviting readers to explore ideas
- Focus: Human imagination, impossible things, creativity, achieving the impossible
- Structure: Use section headings to break up longer essays
- Formatting: Use **bold** for key terms and frameworks, *italics* for conceptual emphasis
- Contractions: Use sparingly - prefer full forms in narration/analysis ("was not," "does not"), contractions in personal/dialogue moments
- Purpose: Book-related content, excerpts, ideas-in-progress, establishing foundational concepts
- Inspiration: Alice in Wonderland themes, "believing impossible things before breakfast"

### TIER 3: Writing Strength Check

Scan for these patterns that weaken writing and suggest stronger alternatives:

| Pattern | Rule | Example |
|---------|------|---------|
| **just/actually/literally** | Remove unless essential to meaning | "I just wanted to..." → "I wanted to..." |
| **very/really + adjective** | Replace with stronger word | "very big" → "gigantic"; "really tired" → "exhausted" |
| **Telling feelings** | Show what you're ACTUALLY feeling/thinking | "I felt overwhelmed" → "My chest tightened" |
| **I realized/wondered/noticed** | Remove — make it obvious from context | "I realized I was stuck" → "I was stuck" |
| **I think/I believe** | State directly or show through evidence | "I think imagination is key" → "Imagination is key" |
| **There is/There are** | Restructure for stronger subject | "There are four conditions" → "Four conditions exist" |

**Format:** Present findings in a table with Current → Suggested replacement. Only flag instances that genuinely weaken the writing — some uses are intentional for the contemplative voice.

---

## Step 3: SEO-Friendly URL

Generate **one URL** based on the post heading.

**Format:** lowercase, hyphens only, 3-6 words max

Convert the heading to URL-friendly format (e.g., "Believing Impossible Things Before Breakfast" → `believing-impossible-things-before-breakfast`)

### Check for Duplicate URLs

Before finalizing the URL:

1. Query the Notion Substack Posts database (`2a908620-e1b0-80fd-866d-ea04d0ba0a84`)
2. Extract all existing URL slugs from the **Link** field
3. Check if the proposed URL slug already exists
4. If duplicate found: warn the user and suggest an alternative

**This prevents 404 errors and SEO conflicts from duplicate URLs.**

---

## Step 4: Midjourney Prompt for Feature Image

**Required Parameters:**
```
--chaos 20 --sref 988536430 --sw 100 --v 7 --stylize 200 --ar 4:3
```

### Framework: Mine the Post First, Then Go Abstract

**Step 4a: Extract the post's own visual language**
Before inventing metaphors, ask: "What images does the post itself create?"
- What comparisons or metaphors does the author use?
- What physical scenes or moments are described?
- What abstract concepts could be visualized?
- Use THESE first — they're already connected to the content.

**Identify the core visual metaphor.** What's the ONE image that would make someone immediately get the post? For Cheshire Cat, lean toward the conceptual and dreamlike.

**Step 4b: Define the emotional/conceptual core**
What is the feeling or idea at the heart of this piece?
- Wonder? Discovery? Paradox? Possibility?
- What visual would evoke that state of mind?

**Step 4c: Define the premise in 3-6 words**
What is this post actually about? Strip it down to the core idea.

**Step 4d: Identify 3 visual approaches**
1. **Literal from the text** — A specific image or metaphor used in the post
2. **Conceptual/symbolic** — An abstract representation of the core idea
3. **Alice in Wonderland-adjacent** — Dreamlike, impossible, whimsical interpretation

**Scene Focus for The Cheshire Cat Lab:**
- Abstract/conceptual imagery
- Imagination and wonder themes
- Alice in Wonderland vibes (White Queen, impossible objects, etc.)
- Creative exploration, impossible things
- Dreamlike, philosophical
- Whimsical yet contemplative

**Step 4e: Write initial prompts with minimal words**
- Describe WHAT you see, not how it feels
- 5-10 words max for the scene
- Always start with "illustration of..."

**Step 4f: Interpretation check (for each prompt)**
Ask: "What could someone think of when they see this prompt?"
- List 3-5 possible interpretations
- If any contradict the premise, revise the prompt
- Add clarifying words to steer toward the right interpretation
- Do NOT use negative words — Midjourney doesn't handle negatives well

**Step 4g: Final prompts**
Generate 3 prompt options combining scene + parameters.

**Structure:** `illustration of [brief scene] [parameters]`

**Key Principles:**
- **Conceptual first** — lean into abstract and symbolic for this publication
- **Less is more** — keep descriptions concise (5-10 words for scene)
- Do NOT include artistic style descriptions (--sref handles styling)
- Avoid the word "text" (confuses Midjourney into generating text overlays)

---

## Step 5: Cross-Linking Plan

**Goal:** Strengthen SEO by linking posts through existing keywords (not adding new sentences).

### A. Links TO add in NEW post:
1. Query Notion Substack Posts database to find all published Cheshire Cat Lab posts
2. Use **WebFetch** to read the actual published content from Substack (not Ulysses—Substack has the most current versions)
3. Identify natural connection points in the new post where previous posts should be referenced
4. Provide specific location and suggested link text

### B. Links to ADD to PREVIOUS posts (after publication):
1. Use **WebFetch** to read each published post from Substack
2. Search for existing keywords in previous posts that relate to the new post's themes
3. Suggest linking those keywords to the new post URL
4. Only suggest links where keywords naturally exist—don't add new sentences

**Cross-linking principles:**
- SEO-focused: link existing keywords, don't add filler sentences
- Natural flow - if no keyword match exists, skip that post
- Use descriptive anchor text (the keyword itself)
- Typically 0-2 links per post (quality over quantity)
- Consider thematic connections (not just chronological)

---

## Step 6: Update Notion

**Database ID:** `2a908620-e1b0-80fd-866d-ea04d0ba0a84` (Substack Posts)

**The Cheshire Cat Lab Publication ID:** `2a908620-e1b0-80a0-a6d7-d08075879a85`

**Default Publish Date:** Tomorrow (unless user specifies otherwise)

### Creating the Notion Entry

Use `notion-create-pages` with the data_source_id:
```json
{
  "parent": {"data_source_id": "2a908620-e1b0-80fd-866d-ea04d0ba0a84"},
  "pages": [{"properties": {"Title": "Post title", ...}}]
}
```

### Before creating the Notion entry:

**Ask the user for the Draft Link:**
- Substack provides a draft preview link that works before the post is published
- Ask: "What's the Substack draft link for this post? (You can find it in Substack's editor under Share → Copy link)"

**Create new page with:**
- **Title:** Post title
- **Link:** `https://thecheshirecatlab.substack.com/p/[url-slug]`
- **Draft Link:** The draft preview URL from Substack (URL field)
- **Publication:** Relation to The Cheshire Cat Lab
- **Published Date:** YYYY-MM-DD format
- **Premise:** 3-8 word core idea of the post (from Step 4c)
- **Audience:** Target persona(s) - e.g., "Writers", "Creatives", "Thinkers"
- **SEO Keywords:** Comma-separated list of keywords to optimize for

**Field descriptions:**
- **Draft Link** — Substack's preview link that works before publication.
- **Premise** — Used for semantic cross-linking between posts. Should capture the core "what this post is about."
- **Audience** — Primary persona(s) this post is written for.
- **SEO Keywords** — Terms people might search for that this post addresses.

---

## Workflow

1. Ask user which Ulysses document to work with (or auto-detect most recent)
2. Ask for publish date (default: tomorrow)
3. Read the post content
4. **Ask if they need the optional Initial Draft Review** (Step 1.5) - if yes, complete it before proceeding
5. Execute remaining steps **one at a time**, getting user confirmation before moving to next step
6. Mark each step complete in a todo list as you go
7. Summarize what was completed at the end

---

## Important Notes

- **Use TodoWrite** to track progress through all steps
- **One step at a time** - don't rush ahead without user confirmation
- **ADHD-friendly** - keep responses concise, use clear formatting, offer intelligent defaults
- **Conversational tone** - this is a collaborative process
- The user may skip steps or request modifications - be flexible!
