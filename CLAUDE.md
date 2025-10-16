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
