# resume-agent

A Claude skill for tailoring job applications to specific roles. Give Claude a job description and it will analyze how well your background fits, rewrite your resume to match, and write a targeted cover letter.

## What it does

**Gap Analysis**
Paste a job description and get a structured breakdown of how your experience maps to the role, what gaps exist, and how to position yourself.

**Tailored Resume + Cover Letter**
Claude rewrites your resume to match the specific role, produces a downloadable `.docx` file, and writes a targeted cover letter — all based on your actual experience.

---

## How to install

### On Claude.ai

1. Download the zip from this repo (click the green **Code** button, then **Download ZIP**)
2. Go to [claude.ai](https://claude.ai), open **Settings**, and go to **Capabilities**
3. Upload the zip
4. Start a new conversation — Claude will set everything up automatically

### In Claude Code

```bash
git clone https://github.com/[your-username]/resume-agent ~/.claude/skills/resume-agent
```

Open a new Claude Code session and the skill is live.

---

## First time setup

You don't need to edit any files. The first time you use the skill, Claude will:

1. Ask you to paste or upload your existing resume
2. Ask follow-up questions only for anything missing or unclear
3. Ask a few questions about your industry, goals, and how you want to be represented
4. Write and save your personal files automatically

The whole process takes about 5–10 minutes and only happens once.

---

## After setup

Paste any job description and tell Claude what you need:

- "How well do I fit this role?"
- "Tailor my resume and write me a cover letter"
- "Do a gap analysis on this job posting"

Claude will produce a downloadable `.docx` resume for each application so every version stays separate.

To update your resume or profile later just tell Claude — "I have a new role to add" or "my career goals have changed" — and it will update your files directly.

---

## File reference

| File | Purpose |
|------|---------|
| `SKILL.md` | Instructions Claude follows — no need to edit this |
| `profile.md` | Your personal profile — Claude fills this in during setup |
| `resume.md` | Your master resume — Claude fills this in during setup |
| `.gitignore` | Prevents your personal files from being committed if you fork this repo |
