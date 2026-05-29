# claude-skills

A portable `.claude/` folder dropped into any project to extend Claude Code with custom skills and scripts.

## Usage

Copy the `.claude/` directory into the root of any project:

```bash
cp -r /path/to/this-repo/.claude /path/to/your-project/
```

Claude Code will automatically pick up the skills and make them available as slash commands.

## Skills

| Skill | Trigger | Description |
|-------|---------|-------------|
| `grill-me` | `/grill-me` | Relentlessly interviews you about a plan or design until reaching shared understanding |
| `handoff` | `/handoff` | Compacts the current conversation into a document another agent can pick up |
| `improve-codebase-architecture` | `/improve-codebase-architecture` | Finds refactoring and deepening opportunities in a codebase |
| `ralph` | `/ralph` | Converts a PRD into `prd.json` format for the Ralph autonomous agent system |
| `tdd` | `/tdd` | Red-green-refactor loop for building features or fixing bugs test-first |
| `to-issues` | `/to-issues` | Breaks a plan or PRD into independently-grabbable GitHub issues |
| `to-prd` | `/to-prd` | Turns the current conversation into a PRD and posts it to the issue tracker |
| `write-a-skill` | `/write-a-skill` | Scaffolds a new skill with proper structure and bundled resources |

## Scripts

| Script | Description |
|--------|-------------|
| `scripts/ralph.sh` | Shell helper used by the `ralph` skill |

## Structure

```
.claude/
├── scripts/          # Shell helpers used by skills
└── skills/           # One directory per skill
    └── <skill-name>/
        └── SKILL.md  # Skill definition and instructions
```
