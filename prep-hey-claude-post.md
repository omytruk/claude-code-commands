# Prepare Hey Claude Substack Post for Publication

This command helps prepare a Hey Claude Substack post from Ulysses for publication.

## Task Overview

You will help prepare a Substack post through the following steps:
1. **Initial Draft Review** (Optional) - Flow, structure, formatting
2. **Proofreading & Cleanup** - Two-tier approach
3. **SEO-Friendly URL** - Generate URL from heading
4. **Midjourney Prompt** - Create feature image prompt
5. **Cross-Linking** - Add links between posts
6. **Notion Update** - Add post to database with publish date
7. **Extract Substack Notes** - Create 6 shareable notes

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

Use **Option 1: Two-tier approach**

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

---

## Step 3: SEO-Friendly URL

Generate **one URL** based on the post heading.

**Format:** lowercase, hyphens only, 3-6 words max

Convert the heading to URL-friendly format (e.g., "Thank you Claude for keeping my plants alive!" → `thank-you-claude-keeping-plants-alive`)

---

## Step 4: Midjourney Prompt for Feature Image

**Required Parameters:**
```
--chaos 20 --ar 4:3 --sref 3083026132 --sw 100 --v 7 --stylize 200
```

**Generate 3 prompt options** that align with the post's main theme/hook.

**Structure:** `illustration of [brief scene], [parameters]`

**Prompt Principles:**
- **Less is more** — keep descriptions concise (5-10 words for scene)
- **Can be abstract** — doesn't need a person/woman in every image
- Always start with "illustration of..."
- Do NOT include artistic style descriptions (--sref handles styling)
- Avoid the word "text" (confuses Midjourney into generating text overlays)

**Scene ideas for Hey Claude:**
- Literal/relatable imagery (productivity, workspaces, plants)
- Abstract concepts (memory, connection, relief, overwhelm)
- Warm, hopeful mood

---

## Step 5: Cross-Linking Plan

**Goal:** Strengthen SEO by linking posts through existing keywords (not adding new sentences).

### A. Link TO add in NEW post:
1. Query Notion Substack Posts database to find all published Hey Claude posts
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
- **Max 3 internal links per post** — if a post already has 3 links, either suggest swapping one for better relevance or skip that post entirely
- **Paywalled resource page:** Link to `https://olenamytruk.substack.com/p/adhd-ai-os` where relevant (this is the hub for paid subscriber resources like Git repos, commands, etc.)

### C. Auto-Create Cross-Linking Task
After identifying cross-linking opportunities, automatically create a task in Notion:
- **Database:** Tasks (`2a708620-e1b0-80f9-9306-f1d6d0984dbb`)
- **Task title:** "Add cross-links to published Substack posts"
- **Plan Date:** Publish date at 1pm (use 19:00 UTC for CST timezone)
- **Project:** Link to "Substack: Hey Claude" (`2a708620-e1b0-81df-ba5c-da0514b7f74b`)
- **Page content:** Bulleted list with each cross-linking update needed (post name, exact text to link, URL to link to)

---

## Step 6: Update Notion

**Database ID:** `2a908620-e1b0-80fd-866d-ea04d0ba0a84` (Substack Posts)

**Hey Claude Publication ID:** `2a908620-e1b0-8077-9c7d-dcc26e8f00f4`

**Default Publish Date:** Tomorrow (unless user specifies otherwise)

**Create new page with:**
- Title: Post title
- Link: `https://olenamytruk.substack.com/p/[url-slug]`
- Publication: Relation to Hey Claude
- Published Date: YYYY-MM-DD format

---

## Step 7: Extract Substack Notes

**Database ID:** `2a908620-e1b0-8025-bac6-d78fdb1f9e64` (Substack Notes)

**Goal:** Extract 6 punchy, shareable notes from the post

**Note Types:**
1. **The Relatable Confession** - Personal struggle/admission
2. **The Ironic Win** - Contrast between past achievement and current challenge
3. **The ADHD Truth Bomb** - Key insight about ADHD patterns
4. **The Requirements/Framework** - Bullet list of what works
5. **The Pattern Breaker** - The transformation/breakthrough
6. **The Before/After** - Clear contrast showing change

**Format Guidelines:**
- 2-4 sentences or short paragraph
- Can include emoji if relevant to voice
- Include hook/intrigue
- Thread-style for lists (bullets with context)

**Critical: Notes must be self-contained**
- Each note must tell a complete mini-story that makes sense WITHOUT any context from the post
- Avoid referencing "the file," "this command," "the system" etc. without explaining what it is
- Test: Would a stranger scrolling Substack understand this note on its own?

**Save to Notion:**
For each note, create page with:
- Note: The full text (in title field)
- Related Post: Relation to the new post
- Publication: Relation to Hey Claude
- Used: Unchecked (false)

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
