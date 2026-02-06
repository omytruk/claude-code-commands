# Wrap Up Session & Update Documentation

This command helps close out a Claude Code session by reviewing what was accomplished and ensuring CLAUDE.md stays current.

## Purpose

Creates a consistent, ADHD-friendly closing ritual that:
- Captures important decisions and changes
- Keeps CLAUDE.md documentation current
- Identifies loose ends or follow-up tasks
- Prevents "what did we even do today?" anxiety

**IMPORTANT:** Explicitly confirm each step as you complete it - even if there's nothing to do for that step. This creates a clear audit trail and prevents accidentally skipping steps. 

---

## Task Overview

You will help close the session through the following steps:
1. **Session Review** - Summarize what was accomplished
2. **What Did I Learn About Olena?** - Reflect on non-obvious insights about how she works, thinks, and wants to be supported
3. **Sweep for Factual Changes** - Scan for concrete updates (new projects, commands, files, etc.)
4. **Update Documentation** - Capture both learnings and factual changes in CLAUDE.md
5. **Sync Brain to GitHub** - Push CLAUDE.md changes to olena-brain repo
6. **Coral Brain Context Check** - Verify Coral still gets the right sections
7. **File Sync** - Copy updated skills/commands to active location
8. **AI Tools Resource Page Check** - Check if Hey Claude resource page needs updating
9. **Capture Loose Ends** - Note any follow-ups or unfinished items
10. **Final Check** - Offer to create brain dumps or reminders

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

## Step 2: What Did I Learn About Olena?

**The goal of this step is to grow as Olena's assistant.** Re-read the conversation and ask: *What do I understand about Olena now that I didn't before?*

Think beyond the tasks completed. The most valuable learnings are often the ones that weren't the main topic — they show up in how Olena reacted, what she avoided, what lit her up, what she said casually.

**What to reflect on:**

- **How her brain worked today** — Did she hit a wall? What got her unstuck? Did she need a push or space? What triggered overwhelm or avoidance? What kept her engaged?
- **How she wants to be supported** — Did she correct my approach? ("Don't give me options, just pick one.") Did she respond better to some interaction styles than others? Did she say "I prefer..." or "Please don't..." about anything?
- **What she revealed about herself** — New constraints (schedule, energy, capacity), fears or anxieties that surfaced, things she's excited about, shifts in how she sees her projects or goals.
- **Writing voice discoveries** — Tone shifts, word preferences, what felt right or wrong in drafts we worked on together.
- **Patterns worth naming** — Recurring behaviors that aren't yet captured in CLAUDE.md (e.g., "she always does X before starting Y" or "she shuts down when Z happens").

**Don't force it.** Some sessions are purely operational and there's nothing new to learn. That's fine — acknowledge it and move on.

### Decide what to capture:

For each insight, decide: is this worth remembering for future sessions? If yes:
- **What I learned:** [The insight]
- **Where it belongs in CLAUDE.md:** [Section — usually "ADHD Patterns to Support," "Working WITH Olena's Brain," or "Writing Voice"]
- **Why it matters:** [How this helps me support Olena better]

If nothing new — confirm: "No new relational insights this session."

---

## Step 3: Sweep for Factual Changes

Now scan for the concrete stuff that needs updating in CLAUDE.md:

- **Active Projects & Writing** — New posts published? Status changes? New writing completed?
- **Claude Code Slash Commands** — New commands created or updated? Status changes?
- **Notion Workspace Structure** — New databases, fields, projects, or IDs?
- **Local Folder Structure** — New folders, moved files, important new paths?
- **ADHD Patterns to Support** — New patterns identified or existing ones refined?
- **Writing Voice** — Guidelines refined or new notes discovered?
- **How to Help Most Effectively** — New workflows, knowledge bases, or instructions?

### Create update list:

For each factual change:
- **What changed:** [The concrete change]
- **Where it belongs in CLAUDE.md:** [Section name]
- **Current value:** [What it says now]
- **New value:** [What it should say]

If nothing changed — confirm: "No factual updates needed."

---

## Step 4: Update Documentation

**Apply updates from both Step 2 (learnings) and Step 3 (factual changes) to CLAUDE.md.**

### Approach: Two-tier

**TIER 1: Direct updates** (make these without asking)
- New file locations, database IDs, project status changes
- New command additions, date stamps
- Adding a bullet point to an existing list (e.g., new pattern under "Working WITH Olena's Brain")

**TIER 2: Present before/after for user approval first**
- Voice guideline refinements
- New sections to add
- Structural reorganization
- Significant content additions

### After all updates:
- Update the "Last Updated" timestamp at bottom
- Confirm all changes with brief summary

**If neither Step 2 nor Step 3 produced updates, skip this step and confirm:** "Nothing to update in CLAUDE.md this session."

---

## Step 5: Sync Brain to GitHub

**After updating CLAUDE.md, sync to GitHub so all tools have the latest version.**

### Commands to run:
```bash
cd ~/Documents/PROJECTS/olena-brain && git add CLAUDE.md && git commit -m "Update brain: [brief description of changes]" && git push
```

### Process:
1. Stage CLAUDE.md changes
2. Commit with descriptive message summarizing what was updated
3. Push to origin

### Confirm to user:
"✅ Brain synced to GitHub — all tools will see the latest version."

**If no changes were made to CLAUDE.md, skip this step AND Step 6, and confirm:** "No brain changes this session — skipping GitHub sync and Coral check."

---

## Step 6: Coral Brain Context Check

**Coral fetches CLAUDE.md from GitHub but skips certain sections that aren't relevant for a voice assistant. If the brain changed, verify Coral still gets the right context.**

### When this matters:
- Sections were **added, renamed, or restructured** in CLAUDE.md
- Content was **moved between sections** (e.g., from a skipped section to a non-skipped one, or vice versa)
- A new section was added that Coral **should NOT** receive (Claude Code-specific details, file paths, command docs)

### Current SKIP_SECTIONS list:
Coral skips these sections (defined in `voice-assistant/lib/brain.ts` line 14):
- `### Custom Claude Skills`
- `### Claude Code Slash Commands`
- `## Local Folder Structure`
- `## Obsidian Vault`
- `### Book Research Tagging Structure`
- `### Writing Folder`
- `### Writing Voice`
- `## How to Help Most Effectively`
- `#### Research Tools`
- `#### Key Figures of Fascination`

### What to check:
1. **New sections added?** → Should Coral see them, or should they be added to SKIP_SECTIONS?
2. **Sections renamed?** → The skip list uses `startsWith` matching — if a heading was renamed, the old entry won't match anymore. Update the skip list.
3. **Sections restructured?** → Heading level changes (e.g., `###` to `##`) affect which sub-sections get skipped. Verify the skip still works correctly.

### If changes needed:
Update `SKIP_SECTIONS` in `~/Documents/PROJECTS/voice-assistant/lib/brain.ts` and push to GitHub (Vercel auto-deploys).

### Confirm to user:
- If no impact: "✅ Coral's brain context is unaffected by today's changes."
- If update needed: "⚠️ Coral's SKIP_SECTIONS needs updating — [describe what changed]."

**If no changes were made to CLAUDE.md, this step was already skipped in Step 5.**

---

## Step 7: File Sync

If any Claude skills or slash commands were created or modified during the session, **copy them to the active location automatically**:

- **Commands:** Copy from `Documents/PROJECTS/claude-code-commands/` to `~/.claude/commands/`
  ```bash
  cp ~/Documents/PROJECTS/claude-code-commands/[command-name].md ~/.claude/commands/
  ```

- **Skills:** Copy from `Documents/PROJECTS/claude-skills/` to the active skills location (if applicable)

**After copying, confirm to user:** "✅ Copied [command-name].md to ~/.claude/commands/"

**Only do this step if changes were actually made to these files.** If no skills or commands were modified, skip to Step 8.

---

## Step 8: AI Tools Resource Page Check

**This step applies ANY time the session involved:**
- Updated or created Claude skills
- Updated or created Claude Code commands
- Built new AI tools or workflows

**If any of the above apply, ask:** "Since we updated [skills/commands/tools], do you want to check if the AI Tools Resource Page needs updating? (`https://olenamytruk.substack.com/p/adhd-ai-os`)"

**If none of the above apply, confirm:** "No AI tools, commands, or skills were modified this session — skipping resource page check."

---

## Step 9: Capture Loose Ends

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

## Step 10: Final Check

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