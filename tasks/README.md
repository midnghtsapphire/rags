# Tasks

**Purpose:** Organized, prioritized, actionable to-do list processed from brain dumps and daily work.

## Files

### `todo.md`
Your master to-do list with priority levels. All tasks end up here after processing.

### `completed.md`
Archive of completed tasks (moved from todo.md when done).

### `someday-maybe.md`
Ideas that aren't actionable right now but you don't want to forget.

## Daily Processing Workflow

### Step 1: Review Brain Dump
Open today's file in `/projects/braindump/`

### Step 2: Categorize Items
For each item in your brain dump, decide:

**Is it actionable?**
- ✅ YES → Add to `todo.md` with priority
- ❌ NO → Move to `someday-maybe.md` or delete

**Is it urgent?**
- 🔥 Priority 1 (P1) - Do today
- ⚡ Priority 2 (P2) - Do this week
- 📌 Priority 3 (P3) - Do this month
- 💭 Priority 4 (P4) - Someday/maybe

**Is it part of an existing project?**
- Add `[Project Name]` tag
- This prevents creating duplicate projects

### Step 3: Process to Google Calendar (Optional)
Use Google Calendar integration to:
- Set reminders for P1 tasks
- Block time for P2 tasks
- Schedule review sessions for P3 tasks

### Step 4: Archive Brain Dump
Move today's brain dump to `/projects/braindump/archive/` folder

## Task Format

```markdown
- [ ] Task description [Project Name] (P1) @context #tag
```

**Example:**
```markdown
- [ ] Build landing page for Alt Text app [The Alt Text] (P1) @coding #mvp
- [ ] Research Cohere API pricing [OZ Marketing] (P2) @research #llm
- [ ] Write blog post about ADHD workflows [Content] (P3) @writing #blog
```

## Priority Definitions

**P1 - Critical (Do Today)**
- Blocking other work
- Time-sensitive deadline
- High-impact, quick win
- Client/customer facing

**P2 - Important (This Week)**
- Moves projects forward
- Scheduled meetings/calls
- Dependencies for other tasks

**P3 - Planned (This Month)**
- Strategic work
- Learning/research
- Nice-to-have features

**P4 - Someday/Maybe**
- Ideas to explore later
- Low priority improvements
- Experimental projects

## Preventing Project Sprawl

### Before Creating a New Project:
1. Check if it fits into an existing project
2. Ask: "Is this a feature or a product?"
3. Use tags to group related tasks without creating new folders

### Project Consolidation Rules:
- If two projects share 50%+ of the same goals → merge them
- If a "project" has fewer than 3 tasks → it's probably a feature
- Use the brain dump to capture ideas, not create structure

## ADHD-Friendly Tips

**Don't process while capturing.** Brain dump first, organize later.

**Set a daily processing time.** End of day works best for most people.

**Use timers.** Give yourself 15 minutes to process the brain dump.

**Batch similar tasks.** Group all coding tasks, all research tasks, etc.

**Celebrate completions.** Move finished tasks to `completed.md` and review weekly.

**Review weekly.** Every Sunday, review all P2 and P3 tasks and reprioritize.
