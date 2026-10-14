# ShellSafe Agent & Skills Seminar Pack

This starter pack contains:
- `AGENTS.md` — repository-wide coding and safety instructions
- `CLAUDE.md` — Claude-specific project guidance
- `knowledge.md` — domain and workflow context
- `.agents/skills/shellsafe-sensor-data-validation/SKILL.md` — custom skill 1
- `.agents/skills/shellsafe-hab-risk-review/SKILL.md` — custom skill 2

## Before using
Review every file and adjust it to match the actual codebase. In particular, confirm the current sensors, framework, database, prediction method, notification recipients, and test commands. The pack intentionally avoids assuming these details.

## Suggested Git workflow (run in the cloned ShellSafe repository)
```bash
git status
git switch -c seminar/agent-skills-shellsafe
```

Copy the files from this pack into the repository, preserving the `.agents/skills/...` paths. Then inspect and commit:
```bash
git status
git diff --check
git diff
git add AGENTS.md CLAUDE.md knowledge.md README-SEMINAR.md .agents/skills/
git commit -m "Add ShellSafe agent instructions and custom skills"
git push -u origin seminar/agent-skills-shellsafe
```

If the branch already exists, choose another branch name or switch to the existing branch after checking its contents. Do not run `git init` in an existing cloned repository.

## Skills provider
The seminar asks for skills installed from a provider. That is a separate step from creating custom skills. Use the provider/tool approved by your instructor, verify its source and skill contents before installation, and capture a screenshot showing the provider and installed skill. Do not install an unknown script blindly.
