# resume-agent

A Claude skill for tailoring job applications to specific roles. Give Claude a job description and it will analyze how well your background fits, rewrite your resume to match, and write a targeted cover letter.

## What it does

**Workflow 1: Gap Analysis**
Paste a job description and get a structured breakdown of how your experience maps to the role, what gaps exist, and how to position yourself.

**Workflow 2: Tailored Resume + Cover Letter**
Claude rewrites your resume to match the specific role, flags every change it makes, and writes a targeted cover letter — all based on your actual experience.

---

## Setup

No manual file editing required. Claude handles setup for you the first time the skill is used.

When you open the skill for the first time, Claude will:

1. Ask you to paste or upload your existing resume (or build one from scratch if you don't have one)
2. Parse what you provide and ask follow-up questions only for what's missing or unclear
3. Ask a short series of questions about your industry, career goals, tone preferences, and what to highlight
4. Write your completed `resume.md` and `profile.md` files and confirm them with you before saving

The whole process takes 5–10 minutes and only happens once. After that, Claude reads both files silently at the start of every session.

To update your files later, just tell Claude: "Update my resume — I have a new role to add" or "My career goals have changed, let's update my profile."

---

## How to use

### On Claude.ai (zip upload)

1. Fill out `profile.md` and `resume.md` as described above
2. Zip the folder:
   ```
   zip -r resume-agent.zip resume-agent/
   ```
3. In Claude.ai, go to **Settings → Capabilities** and upload the zip
4. Start a new conversation, paste a job description, and ask Claude to analyze the fit or tailor your resume

### In Claude Code

1. Clone this repo into your Claude skills directory:
   ```
   git clone https://github.com/[your-username]/resume-agent ~/.claude/skills/resume-agent
   ```
2. Fill out `profile.md` and `resume.md`
3. Claude will pick up the skill automatically in new sessions

### Via the Claude API

Upload via the Skills API (`/v1/skills`) with the `skills-2025-10-02` beta header.

---

## Keeping your files updated

Edit `resume.md` and `profile.md` directly whenever your situation changes:
- New role or responsibilities
- New tools or skills
- Career goal shift
- New accomplishments worth highlighting

If you installed via zip on Claude.ai, re-zip and re-upload after changes. If you're using Claude Code via git clone, just save the files — Claude reads them fresh each session.

---

## Example prompts

Once the skill is installed and your files are filled out, try:

- "Here's a job description — how well do I fit?"
- "Tailor my resume for this role"
- "Write me a cover letter for this position"
- "Do a gap analysis on this job posting"

---

## File reference

| File | Purpose |
|------|---------|
| `SKILL.md` | Instructions Claude follows — do not edit unless you want to change the workflow |
| `profile.md` | Your industry, goals, tone, and positioning — fill this out |
| `resume.md` | Your full work history — fill this out |
| `README.md` | This file |
