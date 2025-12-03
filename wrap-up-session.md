# Wrap Up Session & Update Documentation

This command helps close out a Claude Code session by reviewing what was accomplished and ensuring CLAUDE.md stays current.

## Purpose

Creates a consistent, ADHD-friendly closing ritual that:
- Captures important decisions and changes
- Keeps CLAUDE.md documentation current
- Identifies loose ends or follow-up tasks
- Prevents "what did we even do today?" anxiety

---

## Task Overview

You will help close the session through the following steps:
1. **Session Review** - Summarize what was accomplished
2. **CLAUDE.md Check** - Identify needed updates
3. **Update Documentation** - Make changes to CLAUDE.md
4. **Capture Loose Ends** - Note any follow-ups or unfinished items
5. **Final Check** - Offer to create brain dumps or reminders

---

## Step 1: Session Review

**Review the entire conversation** and create a concise summary:

### What to identify:
- **Key decisions made** - Important choices or directions chosen
- **Files created or modified** - New commands, skills, documentation
- **New information discovered** - Folder locations, database IDs, workflows
- **Workflows established** - New processes or procedures documented
- **Problems solved** - Issues resolved or blockers removed
- **Next steps identified** - Plans for future work

### Output format:
```markdown
## Session Summary

**Date:** [Current date]

**Main accomplishments:**
1. [First major accomplishment]
2. [Second major accomplishment]
...

**Files created/modified:**
- [File path] - [What changed]

**Key decisions:**
- [Decision made and why]

**New information:**
- [Important discovery or learning]
```

---

## Step 2: CLAUDE.md Check

**Read CLAUDE.md** and compare against the session review.

### Look for updates needed in these sections:

#### Active Projects & Writing
- New posts created or published?
- Status changes (draft → scheduled → published)?
- New writing completed (book chapters, content)?

#### Claude Code Slash Commands
- New commands created?
- Existing commands updated or refined?
- Status changes (framework → ready to use)?

#### Notion Workspace Structure
- New databases or fields added?
- Database IDs discovered or changed?
- New projects added to Active Projects list?

#### Local Folder Structure
- New folders created?
- Files moved or reorganized?
- Important new file locations?

#### ADHD Patterns to Support
- New patterns identified?
- Insights from coaching sessions?
- Updated understanding of what works?

#### Writing Voice
- Voice guidelines refined?
- New tone or style notes discovered?
- Examples to add?

#### How to Help Most Effectively
- New workflows to reference?
- Additional knowledge bases to access?
- Updated instructions?

### Create update list:
For each section needing updates:
- **Section:** [Section name]
- **Current:** [What it says now]
- **Needs:** [What should be updated]
- **Reason:** [Why this update is needed]

---

## Step 3: Update Documentation

### Approach: Two-tier (like post proofreading)

**TIER 1: Simple factual updates**
- New file locations
- Database IDs
- Project status changes
- New command additions
- Date stamps

**Action:** Make these updates directly to CLAUDE.md

**TIER 2: Substantial changes**
- Voice guideline refinements
- New sections to add
- Structural reorganization
- Significant content additions

**Action:** Present before/after for user approval, then update

### After all updates:
- Update the "Last Updated" timestamp at bottom
- Confirm all changes with brief summary

---

## Step 3.5: File Sync Reminders

### Skills/Commands Copy Reminder
If any Claude skills or slash commands were created or modified during the session:
- **Skills:** Remind user to copy from `Documents/PROJECTS/claude-skills/` to the active skills location
- **Commands:** Remind user to copy from `Documents/PROJECTS/claude-code-commands/` to `~/.claude/commands/`

Only mention this if changes were actually made to these files.

### Paywalled Page Update Check
If the session involved Hey Claude Substack AND any of the following:
- Updated or created Claude skills
- Updated or created Claude Code commands
- Built new AI tools or workflows
- Made changes that paid subscribers should know about

**Then ask:** "Since we updated [skills/commands/tools], do you want to check if the paywalled resource page needs updating? (`https://olenamytruk.substack.com/p/adhd-ai-os`)"

---

## Step 4: Capture Loose Ends

Identify and document:

### Unfinished Tasks
- Things started but not completed this session
- Blockers encountered
- Items waiting on user decision

### Follow-Up Items
- "Next time we should..."
- "Remember to..."
- "Don't forget to..."

### Questions to Resolve
- Open questions that arose
- Decisions that need more thought
- Things to research or explore

### Output format:
```markdown
## Loose Ends

**Unfinished:**
- [ ] [Item description]

**Follow-Up:**
- [ ] [Next step to take]

**Questions:**
- [ ] [Question to resolve]
```

**Ask user:** "Would you like me to add any of these to your Notion Tasks or Brain Dump?"

---

## Step 5: Final Check

### Offer capture options:

**Ask:**
"Before we wrap up, would you like to:
- 💭 Add any thoughts to Brain Dump?
- ✅ Create any tasks or reminders?
- 📝 Capture any other notes?
- 🎉 Just finish up and exit?"

### If user wants to capture:
- Use appropriate skills (brain-dump-skill, action-keeper-skill)
- Keep it quick and low-friction
- Don't turn this into a whole new task

### Closing message:
```markdown
✅ Session wrapped up!

**Updated:** CLAUDE.md with [brief list of changes]
**Captured:** [Any tasks/notes added]
**Ready for next time!**

Have a great rest of your day! 👋
```