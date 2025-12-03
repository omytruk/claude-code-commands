# Prepare The Cheshire Cat Lab Substack Post for Publication

This command helps prepare The Cheshire Cat Lab Substack post from Ulysses for publication.

## Task Overview

You will help prepare a Substack post through the following steps:
1. **Initial Draft Review** (Optional) - Flow, structure, headings, formatting, contractions
2. **Proofreading & Cleanup** - Two-tier approach
3. **Add Closing Elements** - Comment CTA and Subscribe button
4. **SEO-Friendly URL** - Generate URL from heading
5. **Midjourney Prompt** - Create feature image prompt
6. **Cross-Linking** - Add links between posts
7. **Notion Update** - Add post to database with publish date
8. **Extract Substack Notes** - Create 6 shareable notes

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

**Voice Guidelines for The Cheshire Cat Lab:**
- Tone: Exploratory, curious, philosophical, wonder-filled
- Style: Literary essay format, thoughtful, inviting readers to explore ideas
- Focus: Human imagination, impossible things, creativity, achieving the impossible
- Structure: Use section headings to break up longer essays
- Formatting: Use **bold** for key terms and frameworks, *italics* for conceptual emphasis
- Contractions: Use sparingly - prefer full forms in narration/analysis ("was not," "does not"), contractions in personal/dialogue moments
- Purpose: Book-related content, excerpts, ideas-in-progress, establishing foundational concepts
- Inspiration: Alice in Wonderland themes, "believing impossible things before breakfast"

---

## Step 2: Add Closing Elements

Before finalizing the post, remind the user to add these two elements at the end:

**1. Comment CTA:**
```
I'm curious, what thoughts or ideas did this post spark for you? Please share in the comments!
```

**2. Subscribe Button:**
Add Substack subscribe button with this caption:
```
If you enjoyed reading this post, subscribe to The Cheshire Cat Lab—it will tell me there's interest out there in my humble attempts to write and that I should continue.
```

**Note:** These cannot be set as defaults in Substack, so they must be manually added to each post before publishing.

---

## Step 3: SEO-Friendly URL

Generate **one URL** based on the post heading.

**Format:** lowercase, hyphens only, 3-6 words max

Convert the heading to URL-friendly format (e.g., "Believing Impossible Things Before Breakfast" → `believing-impossible-things-before-breakfast`)

---

## Step 4: Midjourney Prompt for Feature Image

**Required Parameters:**
```
--chaos 20 --sref 988536430 --sw 100 --v 7 --stylize 200 --ar 4:3
```

**Generate 3 prompt options** that align with the post's main theme/hook - scene descriptions only (style is already applied via --sref).

**Structure:** `illustration of [conceptual scene description], [mood/atmosphere], [parameters]`

**Scene Focus for The Cheshire Cat Lab:**
- Abstract/conceptual imagery
- Imagination and wonder themes
- Alice in Wonderland vibes (White Queen, impossible objects, etc.)
- Creative exploration, impossible things
- Dreamlike, philosophical
- Whimsical yet contemplative

**Important:**
- Always start prompts with "illustration of..."
- Do NOT include artistic style descriptions (the --sref handles styling)
- Avoid the word "text" in prompts (confuses Midjourney into generating text overlays)

---

## Step 5: Cross-Linking Plan

**Goal:** Strengthen SEO by linking posts through existing keywords (not adding new sentences).

### A. Link TO add in NEW post:
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

### C. Auto-Create Cross-Linking Task
After identifying cross-linking opportunities, automatically create a task in Notion:
- **Database:** Tasks (`2a708620-e1b0-80f9-9306-f1d6d0984dbb`)
- **Task title:** "Add cross-links to published Substack posts"
- **Plan Date:** Publish date at 1pm (use 19:00 UTC for CST timezone)
- **Project:** Link to "Substack: The Cheshire Cat Lab" (`2a708620-e1b0-81e0-bda1-dbe20f5f0fe4`)
- **Page content:** Bulleted list with each cross-linking update needed (post name, exact text to link, URL to link to)

---

## Step 6: Update Notion

**Database ID:** `2a908620-e1b0-80fd-866d-ea04d0ba0a84` (Substack Posts)

**The Cheshire Cat Lab Publication ID:** `2a908620-e1b0-80a0-a6d7-d08075879a85`

**Default Publish Date:** Tomorrow (unless user specifies otherwise)

**Create new page with:**
- Title: Post title
- Link: `https://thecheshirecatlab.substack.com/p/[url-slug]`
- Publication: Relation to The Cheshire Cat Lab
- Published Date: Tomorrow's date (YYYY-MM-DD format)

---

## Step 7: Extract Substack Notes

**Database ID:** `2a908620-e1b0-8025-bac6-d78fdb1f9e64` (Substack Notes)

**Goal:** Extract 6 concise, philosophical notes from the post

**Note Style (based on validated examples):**
- Concise insights that stand alone
- Philosophical but accessible
- Capture key concepts or stories
- 1-3 sentences typically
- Should spark curiosity and wonder
- More literary/contemplative than Hey Claude notes

**Examples of what works:**
- "Imagination is the mental freedom to conceive alternatives, generate possibilities and envision what doesn't yet exist."
- "Roger Bannister didn't break 4-minute mile because he was stronger than others. He did it because he was the only one who believed it was possible."
- "Lewis Carroll stuttered all his life—except when speaking to children about Alice in Wonderland. He imagined a world where his stutter didn't exist, then made it real."

**Types to extract:**
- Core definitions/frameworks
- Historical examples with insight
- Key arguments or theses
- Story moments with revelation
- Contrasts that illuminate
- Invitations to think differently

**Save to Notion:**
For each note, create page with:
- Note: The full text (in title field)
- Related Post: Relation to the new post
- Publication: Relation to The Cheshire Cat Lab
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
- **Closing elements reminder** - Always remind user to add comment CTA and subscribe button before publishing
