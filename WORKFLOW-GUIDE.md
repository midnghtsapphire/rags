# Complete Workflow System Guide

Your ADHD-friendly system for capturing ideas, organizing tasks, and managing prompts.

## The Three-Part System

### 1. Brain Dump (`/projects/braindump/`)
**Purpose:** Capture everything without judgment or organization.

**When to use:** Throughout the day, whenever an idea hits.

**How it works:**
- Open today's brain dump file
- Add your idea under any category (or create new ones)
- Don't worry about quality, completeness, or organization
- Just capture and move on

### 2. Tasks (`/projects/tasks/`)
**Purpose:** Organized, prioritized action items.

**When to use:** End of day processing, or when you need to see what's next.

**How it works:**
- Review brain dump daily
- Extract actionable items
- Assign priorities (P1-P4)
- Tag with projects
- Move completed tasks to archive

### 3. Prompt Library (`/home/ubuntu/prompt-library/`)
**Purpose:** Centralized collection of reusable prompts.

**When to use:** When you create a great prompt or need to find one.

**How it works:**
- Store prompts in organized folders
- Use template for consistency
- Version control via GitHub
- Search and reuse across projects

## Daily Workflow

### Morning (5 minutes)
1. Open `/projects/tasks/todo.md`
2. Review P1 (Critical) tasks
3. Block time in Google Calendar for top 3 tasks
4. Open today's brain dump file for quick capture

### Throughout the Day
- Capture ideas in brain dump as they come
- Check off completed tasks in `todo.md`
- Don't process or organize yet—just capture

### End of Day (15 minutes)
1. **Review brain dump:**
   - Read through today's captures
   - Identify actionable items

2. **Process to tasks:**
   - Add actionable items to `todo.md` with priorities
   - Move non-actionable ideas to `someday-maybe.md`
   - Delete obvious non-starters

3. **Archive brain dump:**
   - Move to `/projects/braindump/archive/`
   - Create tomorrow's brain dump file

4. **Update Google Calendar:**
   - Add P1 tasks as calendar events for tomorrow
   - Block time for P2 tasks this week

5. **Celebrate wins:**
   - Move completed tasks to `completed.md`
   - Review what you accomplished

### Weekly Review (30 minutes - Sunday)
1. Review all P2 and P3 tasks
2. Reprioritize based on current goals
3. Check `someday-maybe.md` for items that became priorities
4. Review `completed.md` to celebrate progress
5. Plan next week's focus areas

## Preventing Project Sprawl

### Before Creating a New Project:
✅ **DO:**
- Check if it fits into an existing project
- Ask: "Is this a feature or a product?"
- Use tags to group related tasks
- Add to brain dump first

❌ **DON'T:**
- Create new folders immediately
- Start coding before planning
- Duplicate similar projects
- Create "projects within projects"

### Consolidation Rules:
- If two projects share 50%+ goals → merge them
- If a "project" has fewer than 3 tasks → it's a feature
- Use brain dump to capture, not to create structure

## Google Calendar Integration

### Setting Up Daily Processing
You can use Google Calendar to:
1. Set a daily reminder for "End of Day Processing" at your preferred time
2. Block time for P1 tasks
3. Schedule weekly review sessions

### Using MCP Tools
The system can automatically:
- Add P1 tasks to your calendar
- Create time blocks for focused work
- Set reminders for task reviews

## Prompt Library Workflow

### When You Create a Great Prompt:
1. Save it to appropriate folder in `/home/ubuntu/prompt-library/`
2. Use the template format (`TEMPLATE.md`)
3. Commit to GitHub with descriptive message
4. Update the folder's README if needed

### When You Need a Prompt:
1. Browse the prompt library folders
2. Copy the prompt
3. Customize variables for your use case
4. Document which prompt you used in project notes

### Organizing Scattered Prompts:
1. Add to brain dump: "Organize [prompt name] into library"
2. During processing, add to tasks with P2 or P3 priority
3. When you have time, format and add to library
4. Commit to GitHub

## File Locations Quick Reference

```
/home/ubuntu/
├── projects/
│   ├── braindump/
│   │   ├── README.md
│   │   ├── 2026-01-30-braindump.md (today's file)
│   │   └── archive/ (old brain dumps)
│   ├── tasks/
│   │   ├── README.md
│   │   ├── todo.md (master task list)
│   │   ├── completed.md (finished tasks)
│   │   └── someday-maybe.md (future ideas)
│   ├── oz/ (LLM configurations)
│   ├── chatgpt_oz.md (final LLM stack)
│   └── WORKFLOW-GUIDE.md (this file)
└── prompt-library/ (GitHub: oz-prompt-library)
    ├── README.md
    ├── TEMPLATE.md
    ├── prompt-engineering/
    ├── app-development/
    ├── marketing/
    ├── automation/
    ├── data-analysis/
    ├── research/
    ├── accessibility/
    └── business-strategy/
```

## Tips for ADHD Success

### Capture Without Judgment
Your brain dump is a safe space. Write everything down, even if it seems silly later.

### Separate Capture from Processing
Don't organize while capturing. That's two different brain modes.

### Use Timers
Set a 15-minute timer for daily processing. It's enough time to be effective but not overwhelming.

### Batch Similar Tasks
Group all coding tasks, all research tasks, etc. Context switching is expensive for ADHD brains.

### Celebrate Small Wins
Moving tasks to `completed.md` is a celebration. Review it weekly to see your progress.

### Don't Over-Organize
The system is meant to reduce cognitive load, not create more work. If something feels too complex, simplify it.

### Review and Adjust
This system should evolve with you. If something isn't working, change it.

## Troubleshooting

### "I have ideas scattered everywhere!"
- Add to brain dump: "Consolidate ideas from [location]"
- Process during end of day or weekly review
- Don't try to do it all at once

### "I'm creating projects within projects again!"
- Stop and review existing projects first
- Ask: "Is this really a new product or just a feature?"
- Use tags instead of folders
- Consult with OZ AI before creating new structure

### "My todo list is overwhelming!"
- Focus only on P1 tasks today
- Move P3 and P4 to `someday-maybe.md`
- Break large tasks into smaller ones
- Remember: You can only do one thing at a time

### "I forgot to do daily processing!"
- That's okay! Do it when you remember
- Even 5 minutes is better than nothing
- Don't let perfect be the enemy of good

## Next Steps

1. ✅ System is set up and ready to use
2. 📝 Start using today's brain dump file
3. ⏰ Set up daily processing reminder in Google Calendar
4. 🎯 Add your first tasks to `todo.md`
5. 📚 Add your scattered prompts to the library (gradually)

---

**Remember:** This system exists to serve you, not the other way around. Adjust as needed!
