# Prepare Hey Claude Substack Post for Publication

This command helps prepare a Hey Claude Substack post from Ulysses for publication.

## Task Overview

You will help prepare a Substack post through the following steps:
1. **Initial Draft Review** (Optional) - Flow, structure, formatting
2. **Proofreading & Cleanup** - Three-tier approach
3. **SEO-Friendly URL** - Generate URL from heading
4. **Midjourney Prompt** - Create feature image prompt
5. **Cross-Linking** - Add links to new post (premise-based matching)
6. **Notion Update** - Add post to database with Draft Link, Premise, Audience, SEO Keywords

---

## Step 1: Read the Ulysses Post

**Default location:** `~/Library/Mobile Documents/X5AZV975AG~com~soulmen~ulysses3/Documents/Projects/326364fcbab7438fabb5ce008d2e6f33-ulproject/`

**Hey Claude Project ID:** `326364fcbab7438fabb5ce008d2e6f33-ulproject`

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
- Overall coherence of narrative/story

Provide concise feedback on these issues.

### B. Structure & Headings
Check if the post has:
- Title (H1) and subtitle (H3)
- Section headings (H2) that break up the content (if needed for longer posts)
- Clear story or narrative structure

Suggest headings if missing, or propose improvements to existing structure.

### C. Formatting Review
Review and suggest improvements for:
- **Bold text** - Should highlight key concepts, frameworks, important phrases
- *Italic text* - Should emphasize words or concepts for readability
- Ensure formatting supports the conversational, scannable Hey Claude voice

**After completing this step:** The draft should have clear structure, consistent voice, and readable formatting. Now ready for detailed proofreading.

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
- **Current text:** What it says now
- **Issue:** Why it could be improved
- **Suggestion:** Specific recommendation with before/after

Focus on:
- Clarity and flow
- Repetition
- Missing links or placeholders
- Paragraph length (break up long ones)
- Strengthening conclusion/CTAs
- Subtitle alternatives

**Voice Guidelines for Hey Claude:**
- Tone: Conversational, vulnerable, hopeful, self-deprecating humor
- Style: Short paragraphs, bold headings, direct address, authentic
- Avoid: Corporate jargon, victimization narrative
- Embrace: Personal stories, practical solutions, "tested on myself first" approach

### TIER 3: Writing Strength Check

Scan for these patterns that weaken writing and suggest stronger alternatives:

| Pattern | Rule | Example |
|---------|------|---------|
| **just/actually/literally** | Remove unless essential to meaning | "I just wanted to..." → "I wanted to..." |
| **very/really + adjective** | Replace with stronger word | "very big" → "gigantic"; "really tired" → "exhausted" |
| **Telling feelings** | Show what you're ACTUALLY feeling/thinking | "I felt overwhelmed" → "My chest tightened" |
| **"said" + reaction** | Replace with telling action | "Claude said and I stared" → "Claude made me stare in disbelief" |
| **I realized/wondered/noticed** | Remove — make it obvious from context | "I realized I was stuck" → "I was stuck" |
| **I was thinking** | Replace with what you were ACTUALLY doing | "I was thinking about it" → "I was torturing myself" |

**Format:** Present findings in a table with Current → Suggested replacement. Only flag instances that genuinely weaken the writing — some uses are intentional.

---

## Step 3: SEO-Friendly URL

Generate **one URL** based on the post heading.

**Format:** lowercase, hyphens only, 3-6 words max

Convert the heading to URL-friendly format (e.g., "Thank you Claude for keeping my plants alive!" → `thank-you-claude-keeping-plants-alive`)

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
--chaos 30 --ar 4:3 --sref 531726471 --sw 200 --stylize 300
```

### Framework: Mine the Post First, Then Go Abstract

**Step 4a: Extract the post's own visual language**
Before inventing metaphors, ask: "What images does the post itself create?"
- What comparisons or metaphors does the author use? (e.g., running vs. book-writing, treasure slipping through fingers)
- What physical scenes are described?
- Use THESE first — they're already connected to the content.

**Identify the core visual metaphor.** What's the ONE image that would make someone immediately get the post? Often the most literal representation of the central metaphor is the strongest choice — don't shy away from it. (Example: A post about "idea graveyard" → a tombstone with "idea" on it.)

**Step 4b: Define the emotional core (optional — only if using people)**
If the image will include a person, ask: "What does [the feeling] look like in a body?"
- Posture tells the story: sitting vs. standing, head in hands vs. looking ahead
- Example: "hesitant at starting line" ≠ "collapsed next to starting line, head in hands"

**Note:** Skip this step if going with an object-focused or symbolic image.

**Step 4c: Define the premise in 3-6 words**
What is this post actually about? Strip it down to the core idea.

**Step 4d: Identify 3 visual approaches**
1. **Visual punchline** — The most literal representation of the core metaphor (object, scene, or symbol — NOT necessarily a person)
2. **Scene from the post** — A specific moment or image described in the narrative
3. **Abstract/emotional** — A more interpretive representation

**Avoid defaulting to "person doing X."** Consider object-only images, scenes without people, or symbolic representations. The image should capture the *idea*, not illustrate an action.

**Step 4e: Write initial prompts with minimal words**
- Describe WHAT you see, not how it feels
- 5-10 words max for the scene
- Example: "two friends hold hands" NOT "two friends sitting quietly creating safe space for each other"
- Always start with "illustration of..."

**Step 4f: Interpretation check (for each prompt)**
Ask: "What could someone think of when they see this prompt?"
- List 3-5 possible interpretations
- If any contradict the premise (e.g., romantic when you mean friendship), revise the prompt
- Add clarifying words to steer toward the right interpretation
- Do NOT use negative words (e.g., "not romantic") — Midjourney doesn't handle negatives well

**Example:**
- Initial: `robot hugging a woman`
- Interpretations: romantic couple, protection, comfort, friendship, sci-fi movie scene
- Problem: "romantic couple" contradicts premise
- Revised: `robot and woman as friends, warm embrace` or `friendly robot comforting a woman`

**Step 4g: Final prompts**
Generate 3 prompt options combining scene + parameters.

**Structure:** `illustration of [brief scene] [parameters]`

**Key Principles:**
- **Literal first** — start with the obvious visual, not abstract metaphors
- **Less is more** — keep descriptions concise (5-10 words for scene)
- Do NOT include artistic style descriptions (--sref handles styling)
- Avoid the word "text" (confuses Midjourney into generating text overlays)

---

## Step 5: Cross-Linking Plan

**Goal:** Strengthen SEO by adding relevant internal links to the new post using premise-based semantic matching.

### Process:

**Step 5a: Query existing posts with premises**
1. Query Notion Substack Posts database (`2a908620-e1b0-80fd-866d-ea04d0ba0a84`)
2. Retrieve all Hey Claude posts with their **Premise** field
3. Display premises in a table for reference

**Step 5b: Define new post premise**
Create a 3-8 word premise for the new post that captures its core idea.

**Step 5c: Identify cross-link opportunities (premise-based)**
1. Compare new post content and premise against existing post premises
2. For each potential link, assign a **semantic match score (1-10)**
3. Only recommend links with score **8 or higher**
4. Look for natural anchor text in the new post content that could link to relevant previous posts

**Step 5d: Present recommendations**
For each recommended link:
| Anchor Text | Links To (Post) | Premise Match | Score |
|-------------|-----------------|---------------|-------|
| [text from new post] | [previous post title] | [why it connects] | [8-10] |

**Cross-linking principles:**
- **Semantic-based matching** — match on core meaning, not keyword coincidence
- **8+ threshold** — only recommend strong semantic matches
- **Natural anchor text** — link existing phrases, don't add new sentences
- **Quality over quantity** — typically 0-2 links per new post
- **Paywalled resource page:** Link to `https://olenamytruk.substack.com/p/adhd-ai-os` where relevant (hub for paid subscriber resources)

---

## Step 6: Update Notion

**Database ID:** `2a908620-e1b0-80fd-866d-ea04d0ba0a84` (Substack Posts)

**Hey Claude Publication ID:** `2a908620-e1b0-8077-9c7d-dcc26e8f00f4`

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
- This link is needed so the `/create-hey-claude-social-content` command can read the post content before publication
- Ask: "What's the Substack draft link for this post? (You can find it in Substack's editor under Share → Copy link)"

**Create new page with:**
- **Title:** Post title
- **Link:** `https://olenamytruk.substack.com/p/[url-slug]`
- **Draft Link:** The draft preview URL from Substack (URL field)
- **Publication:** Relation to Hey Claude
- **Published Date:** YYYY-MM-DD format
- **Premise:** 3-8 word core idea of the post (from Step 5b)
- **Audience:** Target persona(s) - e.g., "ADHD", "ADHD, Writers", "Artists"
- **SEO Keywords:** Comma-separated list of keywords to optimize for (from research or post content)

**Field descriptions:**
- **Draft Link** — Substack's preview link that works before publication. Used by social content command to read post content.
- **Premise** — Used for semantic cross-linking between posts. Should capture the core "what this post is about" in a way that can be compared to other posts.
- **Audience** — Primary persona(s) this post is written for. Options: ADHD, Writers, Artists (can combine).
- **SEO Keywords** — Terms people might search for that this post addresses. Used for discoverability and future SEO optimization.

---

## Workflow

1. Ask user which Ulysses document to work with (or auto-detect most recent)
2. Ask for publish date (default: tomorrow)
3. Read the post content
4. **Ask if they need the optional Initial Draft Review** (Step 1.5) - if yes, complete it before proceeding
5. Execute remaining steps **one at a time**, getting user confirmation before moving to next step
6. Mark each step complete in a todo list as you go
7. Summarize what was completed at the end
8. **Remind user** to run `/create-hey-claude-social-content` to create the week's social media content

---

## Important Notes

- **Use TodoWrite** to track progress through all steps
- **One step at a time** - don't rush ahead without user confirmation
- **ADHD-friendly** - keep responses concise, use clear formatting, offer intelligent defaults
- **Conversational tone** - this is a collaborative process
- The user may skip steps or request modifications - be flexible!
