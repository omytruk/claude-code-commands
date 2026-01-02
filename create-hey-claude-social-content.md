# Create Hey Claude Social Media Content

This command creates a week's worth of social media content to promote a Hey Claude Substack post across LinkedIn, Substack Notes, and Bluesky.

---

## Strategy & Context

### Platform Sub-Personas

Before creating content, understand who we're speaking to on each platform:

**Bluesky Jamie** — The younger/more online version. More openly ADHD, uses it as identity. Tech-curious but not technical. Looking for community and validation. Ready to engage with vulnerable content directly.

**Substack Jamie** — The writer version. Already exploring their creative side, reading other writers. More open about neurodivergence. Looking for "people like me." Appreciates longer, more reflective content.

**LinkedIn Jamie** — The professional version. In a corporate or freelance role, managing work while hiding ADHD struggles. Scrolling during a break between meetings. Needs permission to admit the struggle exists. NOT ready to publicly engage with vulnerable content — needs professional framing first.

### Why This Approach

**LinkedIn** (3 posts/week: Day 1, Day 2, Day 5)
- Goal: Drive traffic to Substack (NOT grow LinkedIn following - Olena already has a solid network)
- Audience: Professional/AI/leadership network (ex-colleagues from EPAM, coaches, tech/transformation folks)
- Challenge: LinkedIn deprioritizes external links - workaround is link in first comment
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

**EMBRACE:**
- Mid-thought observations
- Incomplete sentences if that's how the thought lands
- Specific details from her actual experience
- Questions that invite real conversation
- Her actual vocabulary and rhythm

---

## Task Overview

You will create promotional content for a published post through the following steps:
1. **Identify the post** - Query Notion for most recent post, read Jamie persona, read full content
2. **Confirm schedule and create task shells** - Confirm dates with user, create empty Notion tasks upfront
3. **Create Bluesky posts** (5 posts for the week) + Jamie check → update Notion tasks
4. **Create Substack Notes** (5 notes for the week) + Jamie check → update Notion tasks
5. **Create LinkedIn posts** (3 posts) + Jamie check → update Notion tasks
6. **Add daily engagement section** to all tasks

**IMPORTANT:**
- Work through ONE platform at a time. Don't present all content at once - it's overwhelming.
- Create task shells FIRST, then update them as each platform's content is finalized. This ensures content is saved even if the session is interrupted.

---

## Step 1: Identify the Post

**Do NOT ask the user** for post details. Query Notion directly:

1. **Query Notion** (`2a908620-e1b0-80ad-8d78-000bc8f9d2cd`) sorted by Published Date descending, limit 1 to get the most recent post:
   - Post title
   - Post URL (Link field)
   - Draft Link (for reading content before publication)
   - Published date
   - Premise
   - Audience

2. **Read the Jamie persona** from `~/Documents/WRITING/Hey Claude/hey-claude-strategy.md` to have the full persona fresh in mind.

3. **Read the post content** via WebFetch using the **Draft Link** (not the published URL). The draft link works before the post is published, allowing social content creation ahead of time.

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
| Dec 18 | Day 2 | LinkedIn Post 2 (PDF) + Bluesky standalone + Substack Note (standalone - emotional) |
| Dec 19 | Day 3 | Bluesky link post + Substack Note (restack) |
| Dec 22 | Day 4 | Bluesky standalone + Substack Note (with link) |
| Dec 23 | Day 5 | LinkedIn Post 3 (Selfie) + Bluesky link post + Substack Note (standalone - AI/practical) |

Does this look correct? Any dates need adjustment?
```

**Only proceed after user confirms.**

### Create task shells in Notion

After schedule is confirmed, create 5 empty task shells:

**Database:** Tasks (`2a708620-e1b0-807e-b3eb-000b698751cc`)

**For each task:**
- **Task title:** `Hey Claude Social Media: [Mon DD]` (e.g., "Hey Claude Social Media: Dec 17")
- **Plan Date:** The corresponding date (use Plan Date, NOT Due Date)
- **Project:** Hey Claude (`2a708620-e1b0-81df-ba5c-da0514b7f74b`)

**Note:** If page creation via API fails, ask user to create the 5 task shells manually (just titles), then find and update them with Plan Date and Project links.

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
- Link in FIRST COMMENT (not in post body) - LinkedIn deprioritizes external links
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

**Schedule:**
- **Day 1 (publish day):** Post 1 — Substack preview format (closest to post content, drives traffic while fresh)
- **Day 2:** Post 2 — PDF carousel format (adjacent topic with framework/guide)
- **Day 5:** Post 3 — Selfie format (personal story with professional framing)

**Hashtag strategy:**
- 3-5 hashtags per post
- Standard rotation (pick 2-3): #ADHD, #AI, #Leadership, #ExecutiveLife, #Neurodivergent, #FutureOfWork
- Add 1-2 custom per post based on topic (e.g., #MentalHealth, #Productivity, #Burnout, #HighPerformers)

**Visual options:**
- Post 1 (Day 1): Substack preview card
- Post 2 (Day 2): PDF carousel (create via Gamma or Canva)
- Post 3 (Day 5): Selfie

**Closing format (use on all posts):**
End with a combined intro + segue that introduces Olena AND leads to the post:
```
I'm Olena, and I build AI tools that help neurodivergent professionals and creatives work with their brains, not against them. [Segue to post content] — link in the first comment.
```

**Link-to-comment CTA variations (rotate through):**
- "Link in the first comment."
- "You'll find the link in the first comment."
- "Wrote more about what that looks like in practice — link in the first comment."

**Process:**

**Phase 1: Choose angles (do this BEFORE diving into individual posts)**
1. Brainstorm 4-5 distinct **adjacent professional topic angles** that could lead to the Substack post
2. Present all angles to user with brief descriptions
3. User picks 3 angles
4. Together, decide which angle maps to which format:
   - Which is closest to post content? → **Substack preview (Day 1)**
   - Which works as a framework/guide? → **PDF carousel (Day 2)**
   - Which is most personal/story-driven? → **Selfie (Day 5)**

**Phase 2: Create posts one at a time**
For each post (in order: Day 1, Day 2, Day 5):
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

**Jamie Check (after all 3 posts are complete):**
Ask: "Would LinkedIn Jamie relate to all 3 of these posts? Do they feel professional enough to engage with publicly, while still leading to the deeper content?"

---

## Step 6: Add Daily Engagement Section

After all content is created, add the daily engagement section to ALL 5 Notion tasks:

```
---
✨ DAILY ENGAGEMENT (20-30 min total)

📝 SUBSTACK NOTES
Find 3-5 notes from writers in ADHD/writing/creativity space and leave thoughtful comments:
• Add your perspective (not just "Great post!")
• Share a related experience
• Ask a thoughtful follow-up question
• Aim for 2-3 sentences minimum
• Quality > quantity - one great comment beats five generic ones

🦋 BLUESKY
Browse #ADHD #AI #Neurodivergent #Writing feeds and reply to 3-5 posts:
• Share your experience or perspective
• Ask a genuine follow-up question
• Avoid generic comments like "Love this!"
• Aim for comments that continue the conversation
```

---

## Content Format in Tasks

Each task should have this structure:

```
📍 LINKEDIN (format type)

[Full post text including hashtags]

FIRST COMMENT: [URL]

Visual: [suggestion]

[If PDF: Full slide-by-slide content here]

---

🦋 BLUESKY (with link / standalone)

[Full post text including link and hashtags - ready to copy-paste]

---

📝 SUBSTACK NOTE (type)

[Full note text including link if applicable - ready to copy-paste]

---

✨ DAILY ENGAGEMENT (20-30 min total)
[engagement section]
```

---

## Workflow Summary

1. **Identify the post** (Step 1) - Query Notion directly (don't ask user), read Jamie persona, read post content
2. **Confirm schedule and create task shells** (Step 2) - present table with actual dates → user confirms → create 5 empty Notion tasks with Plan Dates and Project links
3. **Create Bluesky posts** (Step 3) - draft 5 → user tweaks → proofread → Jamie check → finalize → **update Notion tasks**
4. **Create Substack Notes** (Step 4) - linked note first → emotional notes → restack prompt → AI/practical note → proofread → Jamie check → finalize → **update Notion tasks**
5. **Create LinkedIn posts one at a time** (Step 5) - adjacent topic → data research → hooks → user picks → draft with professional framing → user revises → proofread → finalize → **update Notion task** → repeat for each post → Jamie check
6. **Add daily engagement section** (Step 6) - add to all 5 tasks
7. **Summarize** what was created

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
- **ADHD-friendly** - keep responses concise, use clear formatting
- **Conversational tone** - this is a collaborative process
- **Avoid formulaic language** - no templates, no "Hot take:", no "I used to... Then...", no rhetorical question hooks
- **LinkedIn link reminder** - always remind to put link in first comment
- **Full PDF content** - include all slide text, prompts, and examples in tasks (not just titles)
- **Copy-paste ready** - all content (text + link + hashtags) together for easy copying
- **Use Plan Date** - when setting task dates in Notion, use Plan Date property (not Due Date)
