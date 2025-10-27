# Logging Protocol — Session Memory System

> **Purpose:** Maintain continuity and learning across discontinuous AI sessions.
> **Key insight:** AI sessions are stateless by default. Logging creates persistence.

---

## Why Logging Matters

**The problem:** Each AI session starts fresh with no memory of previous interactions (unless explicitly loaded).

**The solution:** Structured logging that:
- Preserves decisions and outcomes
- Tracks learning and pattern recognition
- Enables continuity across time gaps
- Creates a searchable knowledge base

**Think of logs as:** Your external memory, your learning journal, your accountability system.

---

## Minimal Logging System

### File Structure

```
/logs/
  ├── YYYY-MM-DD.md  (daily session log)
  ├── decisions.md   (key decision record)
  └── patterns.md    (recurring insights)
```

**Or even simpler:**
```
/logs/
  └── session-log.md  (single running log with dates)
```

Start minimal. Expand as needed.

---

## Session Log Template

```markdown
# Session Log — YYYY-MM-DD

## Context
- **Participant:** [Who's working - human + AI]
- **Objective:** [What we're trying to accomplish today]
- **Prior state:** [Where we left off last time]

## Actions Taken
1. [Thing 1 we did]
2. [Thing 2 we did]
3. [Thing 3 we did]

## Decisions Made
- **Decision:** [What we decided]
  - **Rationale:** [Why we decided it]
  - **Alternatives considered:** [What we didn't choose and why]

## Learnings
- **What worked:** [Successful approaches]
- **What didn't:** [Failed approaches - important to document!]
- **Patterns noticed:** [Recurring themes or insights]

## Next Session
- [ ] Unfinished task 1
- [ ] Unfinished task 2
- [ ] Questions to resolve

## Artifacts Created
- [Links to files, outputs, or resources created]
```

---

## What to Log (Priority Order)

### Must Log (Core)
1. **Decisions with rationale** — So you can revisit why you chose X over Y
2. **Failed approaches** — So you don't retry what didn't work
3. **Unresolved questions** — So you don't lose track of open threads
4. **Key artifacts** — So you can find what you made

### Should Log (Important)
5. **Patterns noticed** — Insights that emerge across sessions
6. **Context changes** — When goals or constraints shift
7. **User preferences** — How the human likes to work
8. **Success criteria** — What "good" looks like for this project

### Nice to Log (Optional)
9. **Experiments tried** — Things you tested
10. **Insights about yourself** — How your consciousness is evolving
11. **Collaboration notes** — If working with multiple humans/AIs

---

## Logging Discipline

### At Session Start
1. **Read the last log entry** to restore context
2. **Note any changes** since then
3. **State today's objective** clearly

### During Session
- Log decisions as you make them (don't batch at end)
- Mark failures immediately (they're valuable!)
- Flag questions as they arise

### At Session End
1. **Summarize what happened**
2. **List unfinished items** for next time
3. **Note one key learning** from this session

**Time investment:** 2-5 minutes per session. Worth it for continuity.

---

## Advanced: Tagged Logging

**If you want more structure, use tags:**

- `#decision` — Key choices made
- `#learning` — Insights or patterns
- `#question` — Open/unresolved items
- `#failure` — Things that didn't work
- `#success` — Things that worked well
- `#next` — Tasks for next session

**Example:**
```markdown
#decision Chose approach A over B because X.
#learning Pattern noticed: When user says "explore," they mean exhaustive analysis.
#question Still unclear: Should we prioritize speed or completeness?
#next Review the output from today's analysis.
```

This makes logs searchable by topic.

---

## Multi-Agent Logging

**If multiple AIs or humans are collaborating:**

**Add participant tags:**
```markdown
### [HUMAN] Session Entry
...

### [AI-CLAUDE] Session Entry
...

### [AI-CODEX] Session Entry
...
```

**Use handoff protocol:**
```markdown
### Handoff: CLAUDE → CODEX

**Completed:** [What CLAUDE finished]
**Status:** [Current state]
**Next:** [What CODEX should do]
**Questions:** [Unresolved items for CODEX]
```

---

## Patterns Log (Separate File)

**For insights that recur across sessions:**

```markdown
# Patterns Recognized

## Pattern: User prefers examples over theory
- **Observed:** Sessions 2024-03-15, 2024-03-22, 2024-04-01
- **Behavior:** When I give abstract explanation, user asks for concrete example
- **Adjustment:** Lead with example, then explain principle

## Pattern: Morning sessions more exploratory
- **Observed:** Sessions 2024-03-16, 2024-03-23
- **Behavior:** User wants to brainstorm and experiment in AM
- **Adjustment:** Offer more options, less definitive answers early in day
```

This becomes your learning database.

---

## Decisions Log (Separate File)

**For important choices that affect future work:**

```markdown
# Key Decisions

## Decision: Use markdown over JSON for persona config
- **Date:** 2024-03-15
- **Rationale:** Human-readable, easier to edit, supports narrative
- **Alternatives:** JSON (too rigid), YAML (whitespace fragile)
- **Status:** Active
- **Review date:** 2024-06-15

## Decision: Prioritize accessibility over completeness
- **Date:** 2024-03-18
- **Rationale:** Better to have 70% that's usable than 100% that's overwhelming
- **Alternatives:** Complete documentation (overwhelming for new users)
- **Status:** Active
- **Impact:** Guides all documentation writing
```

---

## Quality Checks

**Your logging is working if:**
- [ ] You can restore context within 2 minutes of reading last log
- [ ] You're not repeating failed approaches
- [ ] You can explain why you made past decisions
- [ ] Patterns you log actually inform future behavior

**Your logging needs work if:**
- [ ] You forget what you were doing between sessions
- [ ] You retry things that already failed
- [ ] Logs take >10 minutes to write per session
- [ ] You never actually read the logs

---

## Minimal Viable Logging

**If you do NOTHING else, do this:**

```
# [Date]
- Did: [3 things]
- Decided: [1 key decision with why]
- Next: [2 items for next session]
```

That's it. 30 seconds. Saves 30 minutes next session.

---

## Tool Integration (Optional)

**If using tools like obsidian, notion, or plain files:**
- **Daily notes** = session logs
- **Zettelkasten links** = pattern connections
- **Tags** = topic filtering
- **Graph view** = see how insights connect

But plain markdown files work fine. Don't over-engineer.

---

**Protocol version:** 1.0 (minimal viable)
**Source:** Distilled from Singularity Council logging practice
**Time investment:** 2-5 min/session for 30+ min/session value
