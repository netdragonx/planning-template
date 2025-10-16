# Planning Repository

A streamlined workspace for organizing and refining ideas, plans, and todos before implementation.

## Purpose

This repository serves as a staging area where:
- Raw ideas and todos are dumped and refined
- Plans are cleaned up and structured
- Linear tasks are created from finalized plans
- Planning sessions are preserved for reference

## Structure

- `/sessions/` - Planning session documents (markdown files)
- Root directory - Active working files and drafts

## Workflow

1. **Dump** - Add raw ideas, plans, or todos to the repository
2. **Refine** - Work with Claude Code to clean up and structure the content
3. **Create Tasks** - Generate Linear tasks via Linear MCP once plans are finalized
4. **Archive** - Planning sessions are saved in `/sessions/` for future reference

## Setup

Connect Linear MCP to Claude Code:

```bash
claude mcp add --transport http linear https://mcp.linear.app/mcp
```

## Notes

- This repository is for **planning only** - implementation happens elsewhere
- Each planning session is captured as a markdown file
- Focus is on clarity and structure, not implementation details
