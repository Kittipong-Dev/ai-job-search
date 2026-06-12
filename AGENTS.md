# AGENTS.md

## Project purpose

This repository is an AI job-search assistant. It helps the user build a professional profile, evaluate job postings, tailor CVs, draft cover letters, and prepare interview notes.

## Important files

- `CLAUDE.md`: original Claude Code project guidance. Use it as legacy project context.
- `.claude/commands/`: original workflow prompts. Treat these as reusable workflow specs, not Claude-only commands.
- `.claude/skills/job-application-assistant/`: candidate profile, writing style, CV templates, cover letter templates, evaluation criteria, and interview prep.
- `cv/`: generated CV LaTeX and PDFs.
- `cover_letters/`: generated cover letter LaTeX and PDFs.
- `documents/`: user source documents such as CV, LinkedIn export, diplomas, references, and previous applications.

## Codex workflow adaptation

When the user asks for setup, follow `.claude/commands/setup.md`.

When the user asks to apply to a job, follow `.claude/commands/apply.md`.

When the original instructions mention Claude-specific tools:
- `Read` means read the file.
- `Edit` means edit the file.
- `Glob` means list matching files.
- `WebFetch` means fetch the URL if network access is available.
- `WebSearch` means search the web if available.
- `Agent tool` means use a separate reviewer pass. If subagents are unavailable, perform the reviewer step yourself as a clearly separated second role.

## Safety and quality rules

- Do not fabricate skills, achievements, dates, education, or work experience.
- If a job requirement is a gap, say so honestly and frame adjacent experience.
- Before finalizing generated LaTeX, compile and inspect the PDFs when LaTeX is available.
- Keep generated CVs and cover letters version-controlled.
- Do not commit secrets, tokens, private credentials, or raw personal documents unless the user explicitly confirms. 
