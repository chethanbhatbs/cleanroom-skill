# Organize — Claude Code Skill

Clean and organize your laptop — sort Downloads, flag duplicates, organize screenshots by month, and report what was moved.

## Usage

```
/organize           # Quick scan: sort Downloads, flag issues
/organize full      # Full scan: all folders, duplicates, stale files
/organize downloads # Only sort the Downloads folder
/organize screenshots # Only organize screenshots by month
```

## Rules

- **Never deletes files** — only moves and organizes
- **Shows plan before moving** — confirms bulk moves with user
- Downloads sorted by file type into `~/personal/`, `~/work/`, `~/projects/`, `~/screenshots/`
- Screenshots organized into `~/screenshots/YYYY-MM/` by modification date
- Flags duplicates, large files (>100MB), and stale files (>30 days)
- Desktop must stay empty

## Installation

```bash
cp -r organize ~/.claude/skills/
```

## License

MIT
