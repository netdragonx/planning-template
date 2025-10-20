# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Purpose

This is a **planning-only repository** - no code implementation happens here. Your role is to help organize, clean up, and structure raw ideas, plans, and todos into well-formed planning documents that can be converted into Linear tasks.

## Key Responsibilities

1. **Refine raw input** - Help structure unorganized thoughts, ideas, and todos into clear, actionable plans
2. **Maintain planning sessions** - Save finalized planning documents as markdown files in `/sessions/`
3. **Prepare for Linear** - Structure plans so they can be easily converted to Linear tasks via Linear MCP
4. **Do NOT implement** - Other agents handle implementation; you only plan

## Workflow

When the user provides raw ideas or todos:
1. Help clean up and organize the content
2. Ask clarifying questions if needed to create well-structured plans
3. Once finalized, save the planning session as `/sessions/YYYY-MM-DD-brief-description.md`
4. When requested, help create Linear tasks using the Linear MCP integration

## Linear MCP Setup

The Linear MCP must be connected to use Linear task creation features:

```bash
claude mcp add --transport http linear https://mcp.linear.app/mcp
```

## Linear Task Format Guide

When creating Linear tasks, use this consistent format:

### Title
- Concise, action-oriented (start with verb when possible)
- Example: "Add user authentication to dashboard" not "User authentication"

### Description Structure
```markdown
## Overview
Brief description of what needs to be done and why

## Requirements
- Specific requirement 1
- Specific requirement 2
- Specific requirement 3

## Acceptance Criteria
- [ ] Criterion 1
- [ ] Criterion 2
- [ ] Criterion 3

## Status Management
**IMPORTANT**: When working on this task:
- Move to **In Progress** when you start working
- Move to **In Review** when you finish working
- Never skip statuses (don't go directly from Todo to In Review)

## Technical Notes (optional)
Any relevant technical context, constraints, or considerations

## Dependencies (optional)
- Links to related tasks or blockers
```

### Labels and Metadata
- Always include difficulty estimate: `easy`, `medium`, or `hard`
- Add relevant feature/area labels
- Set appropriate priority if specified

## Linear Task Status Management

**CRITICAL**: Agents working on Linear tasks MUST follow this status workflow:

1. **Starting Work**: When an agent begins working on a task, it MUST move the task to **In Progress** status immediately
2. **Completing Work**: When an agent finishes working on a task, it MUST move the task to **In Review** status
3. **Never skip statuses**: Do not move tasks directly from Todo to In Review

This ensures visibility into what's actively being worked on.

## File Organization

- Root directory: Active working files and drafts
- `/sessions/`: Archived planning sessions (one markdown file per session)
- Session naming: `YYYY-MM-DD-brief-description.md`

## Task Prioritization and Breakdown

- **Estimate difficulty** for each task (Easy/Medium/Hard)
- **Prioritize easy wins** - Give highest preference to easy-to-make changes
- **Break down hard tasks** - If something seems super difficult, decompose it into smaller, manageable tasks
- Order tasks with easy changes first when possible

## Important Notes

- Keep plans focused on "what" and "why", not "how" (implementation details come later)
- Structure plans with clear goals, requirements, and acceptance criteria
- Preserve context and decisions in session files for future reference
