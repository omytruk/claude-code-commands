# Create Hey Claude Social Media Content

This command creates a week's worth of social media content to promote a Hey Claude Substack post across LinkedIn, Substack Notes, and Bluesky.

---

## Strategy & Context

### Platform Sub-Personas

Before creating content, understand who we're speaking to on each platform:

**Bluesky Jamie** — The younger/more online version. Openly curious about AI and creative identity. May be ADHD/neurodivergent or just a creative overthinker who senses AI can do more for them. Tech-curious but not technical. Looking for community and validation. Ready to engage with vulnerable content directly.

**Substack Jamie** — The writer/creator version. Already exploring their creative side, reading other writers. More open about struggles (neurodivergence, self-doubt, creative blocks, wanting to build but not knowing where to start). Looking for "people like me." Appreciates longer, more reflective content.

**LinkedIn Jamie** — The professional version. In a corporate or freelance role, sensing AI could do more for them than they're currently doing with it. May be hiding ADHD struggles or simply feeling like they're not "technical enough" to build with AI. Scrolling during a break between meetings. NOT ready to publicly engage with vulnerable content — needs professional framing as entry point.

### Why This Approach

**LinkedIn** (3 posts/week: Day 1, Day 2, Day 5)
- Goal: Drive traffic to Substack (NOT grow LinkedIn following - Olena already has a solid network)
- Audience: Professional/AI/leadership network (ex-colleagues from EPAM, coaches, tech/transformation folks)
- **Include link directly in post** (not first comment) — tested and confirmed this doesn't hurt engagement
- **KEY INSIGHT:** LinkedIn Jamie is in "professional mode" — use adjacent professional topics with data hooks as a "Trojan horse" to lead them to vulnerable Substack content
- What works: Data hooks on ALL posts, professional framing, "AI productivity" language that hides the real message about emotional safety

**Substack Notes** (5 notes/week, one per day)
- Goal: Drive traffic to posts AND grow following
- Audience: Writers, creatives, neurodivergent folks already on Substack
- Critical insight: For accounts under 100 subscribers, *commenting on others' Notes* is more valuable than posting your own. Notes have long staying power (2-3 weeks).
- **Linked note always on Day 4 (Monday)**
- What works: Contrarian/challenging beliefs, emotional/inspirational, community builders

**Bluesky** (5 posts/week)
- Goal: Drive traffic to posts AND grow following
- Audience: Younger (70% under 34), tech-savvy, ex-Twitter refugees, strong neurodivergent community
- Constraint: 300 character limit (tight!)
- What works: Authenticity over virality, niche focus, meaningful engagement

### Voice & Tone Guidelines

**What Olena's voice sounds like:**
- Conversational, vulnerable, hopeful
- Self-deprecating humor
- Honest and mid-thought (not polished conclusions)
- Personal ADHD stories connected to practical insights
- How she'd actually say it to a friend

**AVOID (formulaic patterns that feel manufactured):**
- Rhetorical question hooks ("The real reason?", "Want to know why?")
- Before/after templates ("I used to... Then I started...")
- Labels ("Hot take:", "Unpopular opinion:", "Thread:")
- Manufactured punchiness
- Generic inspirational language

**AI Cliché Phrases to AVOID:**
- "Here's the truth"
- "Turns out" (especially multiple times)
- "Let me be clear"
- "Here's the thing"
- "The reality is"
- "What most people don't realize"
- "This is why"
- "Here's what I learned"
- "Game-changer"
- "The secret is"

Mix short and long sentences for natural rhythm. If a phrase sounds like something an AI would write, cut it.

**EMBRACE:**
- Mid-thought observations
- Incomplete sentences if that's how the thought lands
- Specific details from her actual experience
- Questions that invite real conversation
- Her actual vocabulary and rhythm

---

## Task Overview

You will create promotional content for a published post through the following steps:
1. **Identify the post** - Query Notion for most recent post, read Jamie persona, read full content from Ulysses
2. **Confirm schedule and create task shells** - Confirm dates with user, create empty Notion tasks upfront
3. **Create Bluesky posts** (5 posts for the week) + Jamie check → update Notion tasks
4. **Create Substack Notes** (5 notes for the week) + Jamie check → update Notion tasks
5. **Create LinkedIn posts** (3 posts) + Jamie check → update Notion tasks

**IMPORTANT:**
- Work through ONE platform at a time. Don't present all content at once - it's overwhelming.
- Create task shells FIRST, then update them as each platform's content is finalized. This ensures content is saved even if the session is interrupted.

---

## Step 1: Identify the Post

**Do NOT ask the user** for post details. Query Notion directly:

1. **Query Notion Substack Posts** (`2a908620-e1b0-80fd-866d-ea04d0ba0a84`) sorted by Published Date descending, limit 1 to get the most recent post:
   - Post title
   - Post URL (Link field)
   - Published date
   - Premise
   - Audience

2. **Read the Jamie persona** from `~/Documents/WRITING/Hey Claude/hey-claude-strategy.md` to have the full persona fresh in mind.

3. **Read the post content directly from Ulysses** (NOT via WebFetch, which only returns summaries):
   - Navigate to the Hey Claude Ulysses project: `~/Library/Mobile Documents/X5AZV975AG~com~soulmen~ulysses3/Documents/Projects/326364fcbab7438fabb5ce008d2e6f33-ulproject/`
   - Find the most recent `.ulysses` folder (use Glob to find, sort by modification time)
   - Read `Content.xml` inside to get the full post content

4. **Present to user**: Show what post was found and the publish date, confirm this is correct before proceeding.

---

## Step 2: Confirm Schedule and Create Task Shells

### Confirm the schedule FIRST

**Present the proposed schedule with actual dates** and ask user to confirm before creating any tasks.

**Default schedule:** 5 consecutive weekdays starting from publish day (typically Wednesday, Thursday, Friday, Monday and Tuesday - but flexible and to be confirmed based on actual publish date and the date when the user is working on the content)

Example:
```
Here's the proposed schedule for your social media content:

| Date | Day | Content |
|------|-----|---------|
| Dec 17 | Day 1 (Publish) | LinkedIn Post 1 (Substack preview) + Bluesky link post + Substack Note (standalone - emotional) |
| Dec 18 | Day 2 | LinkedIn Post 2 (AI/Framework PDF) + Bluesky standalone + Substack Note (standalone - emotional) |
| Dec 19 | Day 3 | Bluesky link post + Substack Note (restack) |
| Dec 22 | Day 4 | Bluesky standalone + Substack Note (with link) |
| Dec 23 | Day 5 | LinkedIn Post 3 (Selfie) + Bluesky link post + Substack Note (standalone - AI/practical) |

Does this look correct? Any dates need adjustment?
```

**Only proceed after user confirms.**

### Create task shells in Notion

After schedule is confirmed, create 5 empty task shells using `notion-create-pages`:

**Database:** Tasks (data_source_id: `2a708620-e1b0-807e-b3eb-000b698751cc`)

**For each task:**
- **Task title:** `Hey Claude Social Media: [Mon DD]` (e.g., "Hey Claude Social Media: Dec 17")
- **Plan Date:** The corresponding date (use Plan Date, NOT Due Date)
- **Project:** Hey Claude — **IMPORTANT: Use full URL format for relation fields, NOT just the page ID**

```json
{
  "parent": {"type": "data_source_id", "data_source_id": "2a708620-e1b0-807e-b3eb-000b698751cc"},
  "pages": [
    {
      "properties": {
        "Task": "Hey Claude Social Media: Dec 17",
        "date:Plan Date:start": "2024-12-17",
        "date:Plan Date:is_datetime": 0,
        "Project": "https://www.notion.so/2a708620e1b081dfba5cda0514b7f74b"
      }
    }
  ]
}
```

**Note:** The Project field requires the full Notion URL (e.g., `https://www.notion.so/2a708620e1b081dfba5cda0514b7f74b`), not just the page ID. Using only the ID will cause a validation error.

---

## Step 3: Create Bluesky Posts (5 total)

**Platform specs:**
- 300 character limit (tight - every word counts)
- 2-3 hashtags recommended
- Link cards don't count toward limit, but link text does
- Audience: Bluesky Jamie — openly ADHD, looking for community, validation, and "people like me"

**Hashtag strategy:**
- Standard rotation (pick 2-3): #ADHD, #AI, #Neurodivergent, #Writing, #Substack, #MentalHealth, #Neurospicy
- Add 1 custom per post as relevant (e.g., #Creativity, #ClaudeAI, #JustDoIt)

**Mix for the week:**
- 2-3 posts WITH link to the article
- 2-3 standalone posts (thought-provoking, no link)
- Keep flexible on which posts get links

**Process:**
1. Draft all 5 posts (ready to use, minimal tweaking expected)
2. Present to user for review
3. User tweaks as needed
4. **Proofread all posts** - check grammar, spelling, character count
5. Finalize
6. **Update Notion tasks** with Bluesky content for each day

**Jamie Check (before moving to next platform):**
Ask: "Would Bluesky Jamie relate to all 5 of these posts? Do they feel authentic, vulnerable, and like something they'd want to engage with?"

---

## Step 4: Create Substack Notes (5 total, one per day)

**Platform specs:**
- No strict character limit (can be longer, more reflective)
- Writers and neurodivergent audience
- Discovery happens through engagement more than posting
- Notes can bring subscribers 2-3 weeks after posting
- Audience: Substack Jamie — writer version, exploring creative side, looking for "people like me"

**Fixed Schedule:**
- **Day 1 (Publish day):** Standalone note (emotional fragment)
- **Day 2:** Standalone note (emotional fragment)
- **Day 3:** Restack (restack another creator's relevant content)
- **Day 4:** **Linked note (ALWAYS Day 4)**
- **Day 5:** Standalone note (AI/practical: prompt, tool tip, practical takeaway etc)

### Process (in this order):

**1. Linked Note (Day 4) - do this FIRST:**
1. Draft 2-3 complete options (summary style that preserves Olena's voice)
2. Present options to user
3. User picks/tweaks one
4. **Proofread** - check grammar and spelling
5. Finalize

**2. Standalone emotional Notes (Day 1 and Day 2):**
1. Identify 3-5 "most powerful/emotional/captivating fragments" from the original post
2. Explain briefly why each could work well as a standalone Note
3. User browses, pulls what resonates, shapes into 2 notes
4. **Proofread** - check grammar and spelling
5. Finalize

**3. Restack (Day 3):**
1. Ask user what they would like to restack on Day 3. Make suggestions on the possible themes and/or angles based on the content of the Substack post.
2. User identifies what they want to restack. Ask them if they are planning to add their own thoughts to this restack, proofread it if applicable.
3. Add reminder to Day 3 task - be sure to include the link to the content they are planning to restack (if provided) along with their notes if applicable.

**4. AI/Practical Note (Day 5):**
1. Identify a practical/actionable element from the post (e.g., a prompt, a tool tip, a technique)
2. Draft a note that shares this practical takeaway
3. User tweaks as needed
4. **Proofread** - check grammar and spelling
5. Finalize

**After all notes are finalized:**
- **Update Notion tasks** with Substack Note content for each day

**Jamie Check (before moving to next platform):**
Ask: "Would Substack Jamie relate to all 5 of these notes? Do they feel reflective, authentic, and like content from a fellow writer exploring similar struggles?"

---

## Step 5: Create LinkedIn Posts (3 total)

**Platform specs:**
- **Include link directly in post** — tested and confirmed this doesn't hurt engagement
- Longer posts (800-1000 words) get 26% better engagement
- Data visualizations get 36% better performance
- First 2 lines = everything (the hook determines engagement)
- First 60 minutes of engagement matter most
- Audience: LinkedIn Jamie — professional mode, hiding ADHD struggles, needs permission to engage

**KEY STRATEGY: Trojan Horse Approach**
LinkedIn Jamie is NOT ready to publicly engage with vulnerable content like "my legs walked me to the bedroom." Instead:
- Use **adjacent professional topics** that lead TO the Substack post
- Use **professional framing** they expect ("AI productivity system," "executive function support," "cognitive load")
- The Substack post delivers the vulnerable truth; LinkedIn gives **permission to click**
- ALL posts get **data/news hooks** — research relevant statistics

**Schedule & Post Types:**
- **Day 1 (publish day):** Post 1 — **Substack preview** (closest to post content, drives traffic while fresh)
- **Day 2:** Post 2 — **AI/Framework PDF** (adjacent topic with AI angle — at least one LinkedIn post per week should feature AI)
- **Day 5:** Post 3 — **Selfie** (personal story with professional framing)

**Hashtag strategy:**
- 3-5 hashtags per post
- Standard rotation (pick 2-3): #ADHD, #AI, #Leadership, #ExecutiveLife, #Neurodivergent, #FutureOfWork
- Add 1-2 custom per post based on topic (e.g., #MentalHealth, #Productivity, #Burnout, #HighPerformers)

**Visual options:**
- Post 1 (Day 1): Substack preview card
- Post 2 (Day 2): PDF carousel (create via Gamma or Canva)
- Post 3 (Day 5): Selfie

**Closing format (use on all posts):**
End with a signature block that includes:
1. A divider line
2. "Hi, I'm Olena 👋" + a VARIATION of what she does (don't use the exact same phrase every time)
3. A reaffirming sentence related to the post topic

```
—
Hi, I'm Olena 👋 I build (and write about) [VARIATION]...

[Reaffirming sentence related to the post topic]
```

**Intro variations (rotate through):**
- "...AI tools that work with creative brains rather than against them."
- "...helpful AI tools that solve real human problems."
- "...how non-technical creatives can build real things with AI."
- "...the messy, real process of building useful things with AI — no coding required."
- "...how AI can help curious creative people build things they didn't think they could build."

**Reaffirming sentence examples:**
- "If there's an important project you are afraid to take a break from because you worry you won't be able to get back to it, please know that what you need is not 100% consistency but something that will make it easy for you to start again."
- "Your creativity will thank you for the break."
- "You don't need more discipline. You need tools that work with how your brain actually works."

**Process:**

**Phase 1: Choose angles (do this BEFORE diving into individual posts)**
1. Brainstorm 4-5 distinct **adjacent professional topic angles** that could lead to the Substack post
2. Present all angles to user with brief descriptions
3. User picks 3 angles
4. Together, decide which angle maps to which format:
   - Which is closest to post content? → **Substack preview (Day 1)**
   - Which works as an AI-focused framework/guide? → **AI/Framework PDF (Day 2)** — ensure this has an AI angle
   - Which is most personal/story-driven? → **Selfie (Day 5)**

**Phase 2: Create posts one at a time**
For Day 1 and Day 2 posts:
1. Research relevant data/statistics for that angle (web search)
2. Present 3 hook options using the data
3. User selects hook
4. **Check for duplicate hooks** - ensure this hook is distinct from other LinkedIn posts this week
5. Draft full post with professional framing
6. User revises as needed
7. **Proofread thoroughly** - check grammar, spelling, flow
8. Finalize with hashtags, visual suggestion, and CTA variation
9. **For PDF posts:** Create FULL slide content (not just titles) — include all text, prompts, examples for each slide
10. **Update Notion task** with this post's content
11. **Then move to next post** - repeat from step 1

For Day 5 (Selfie post):
1. **NO data hook needed** — selfie posts are personal stories with professional framing
2. Ask user to share the personal story/experience they want to feature
3. Draft the post based on their story (keep their voice, add professional framing)
4. User revises as needed
5. **Proofread thoroughly** - check grammar, spelling, flow
6. Finalize with hashtags and selfie visual reminder
7. **Update Notion task** with this post's content

**Jamie Check (after all 3 posts are complete):**
Ask: "Would LinkedIn Jamie relate to all 3 of these posts? Do they feel professional enough to engage with publicly, while still leading to the deeper content?"

---

## Content Format in Tasks

Each task should have this structure:

```
📍 LINKEDIN (format type)

[Full post text including link and hashtags]

Visual: [suggestion]

[If PDF: Full slide-by-slide content here]

---

🦋 BLUESKY (with link / standalone)

[Full post text including link and hashtags - ready to copy-paste]

---

📝 SUBSTACK NOTE (type)

[Full note text including link if applicable - ready to copy-paste]
```

---

## Workflow Summary

1. **Identify the post** (Step 1) - Query Notion directly (don't ask user), read Jamie persona, read post content from Ulysses
2. **Confirm schedule and create task shells** (Step 2) - present table with actual dates → user confirms → create 5 empty Notion tasks with Plan Dates and Project links (use full URL for Project relation)
3. **Create Bluesky posts** (Step 3) - draft 5 → user tweaks → proofread → Jamie check → finalize → **update Notion tasks**
4. **Create Substack Notes** (Step 4) - linked note first → emotional notes → restack prompt → AI/practical note → proofread → Jamie check → finalize → **update Notion tasks**
5. **Create LinkedIn posts one at a time** (Step 5) - adjacent topic → data research → hooks → user picks → draft with professional framing → user revises → proofread → finalize → **update Notion task** → repeat for each post (note: selfie posts skip data research) → Jamie check
6. **Summarize** what was created

---

## Important Reminders

- **Use TodoWrite** to track progress through all steps
- **Create task shells FIRST** - ensures content is saved even if session is interrupted
- **Update tasks as you go** - add content to Notion immediately after each platform is finalized
- **One platform at a time** - don't overwhelm with all content at once
- **User drives voice** - provide drafts, let user tweak to sound authentic
- **ALWAYS proofread** - check grammar, spelling, and flow for ALL posts on ALL platforms before finalizing
- **Jamie sub-persona check** - after each platform, verify content resonates with that platform's Jamie
- **LinkedIn = Trojan horse** - adjacent professional topics + data hooks, NOT direct post summaries
- **LinkedIn AI post** - ensure at least one post (the PDF/Framework) has an AI angle
- **LinkedIn selfie posts** - NO data hooks needed; draft directly from user's personal story
- **LinkedIn link in post** - include link directly in post body (not first comment)
- **LinkedIn closing format** - use signature block with intro variation + reaffirming sentence
- **ADHD-friendly** - keep responses concise, use clear formatting
- **Conversational tone** - this is a collaborative process
- **Avoid formulaic language** - no templates, no "Hot take:", no "I used to... Then...", no rhetorical question hooks
- **Avoid AI clichés** - "Here's the truth," "Turns out," "Game-changer," etc. (see full list in Voice & Tone Guidelines)
- **Read from Ulysses directly** - NOT via WebFetch (which only returns summaries)
- **Weekend-free** - by default no social media tasks on Saturday/Sunday (unless specific circumstances impact the schedule)
- **Full PDF content** - include all slide text, prompts, and examples in tasks (not just titles)
- **Copy-paste ready** - all content (text + link + hashtags) together for easy copying
- **Use Plan Date** - when setting task dates in Notion, use Plan Date property (not Due Date)
- **Use full URLs for relations** - when creating tasks, Project relation requires full URL format (e.g., `https://www.notion.so/...`), not just page ID
