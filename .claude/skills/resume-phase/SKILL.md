---
name: resume-phase
description: Resume an interrupted Mini-ERP development task from GitHub checkpoints with minimal repeated context.
---

# Resume Phase Skill

## Purpose
Continue the existing D2C Mini-ERP task when another Claude session runs out of tokens.

## Required Reading
Read these files first:
1. `CLAUDE.md`
2. `CURRENT_TASK.md`
3. `HANDOFF.md`
4. `docs/PROJECT_CONTEXT.md`

Do not reread the entire repository by default.

## Workflow
1. Identify the current task from `CURRENT_TASK.md`.
2. Read `HANDOFF.md` for the last known progress and next action.
3. Inspect only files relevant to the current task.
4. Treat previous reports as historical evidence, not proof of current live state.
5. Verify current state before making changes.
6. Do not repeat completed work unless verification reveals a problem.
7. If essential information or access is missing, state the exact blocker and request the smallest necessary artifact.
8. Before making risky changes, explain the proposed approach and wait for approval when required.

## Safety Rules
- Never expose secrets, passwords, API keys, or access tokens.
- Never activate or publish n8n workflows without explicit approval.
- Never modify production data during tests without authorization.
- Preserve existing Supabase schema, RLS, RPCs, and business rules unless a change is explicitly approved.
- Keep changes minimal and scoped to the current task.

## End-of-Session Checkpoint
Before stopping:
1. Update `CURRENT_TASK.md` with the actual task status.
2. Update `HANDOFF.md` with:
   - Changes made
   - Tests actually run and their results
   - What remains incomplete
   - The next concrete action
   - Relevant files or workflow IDs
3. Distinguish verified facts from assumptions.
4. Do not claim a task is complete unless the required verification passed.
5. Commit the checkpoint changes to GitHub when repository write access is available.
