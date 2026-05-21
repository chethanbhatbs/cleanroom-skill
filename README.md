# Organize — Claude Code Skill

Sort Downloads, organize screenshots by month, flag duplicates and large files. Your laptop organizer.

## Prerequisites

- [Claude Code](https://claude.ai/claude-code) CLI installed
- GitHub CLI (`gh`) for one-line install

## Installation

**One-line install:**

```bash
gh repo clone chethanbhatbs/cleanroom-skill ~/.claude/skills/cleanroom
```

**Manual install:**

```bash
git clone https://github.com/chethanbhatbs/cleanroom-skill.git
cp -r organize-skill/ ~/.claude/skills/cleanroom/
```

**Verify it's installed:**

```bash
ls ~/.claude/skills/cleanroom/
```

You should see `SKILL.md` (and any other skill files).

## Usage

```
/organize              # Quick scan: sort Downloads, flag issues
/organize full         # Full scan: all folders, duplicates, stale files
/organize downloads    # Only sort the Downloads folder
/organize screenshots  # Only organize screenshots by month
```

### What it does

- **Sorts Downloads** into the right folder by file type:
  - `.pdf` (Aadhar, PAN, certificates) → `~/personal/`
  - `.xlsx`, `.csv`, reports → `~/work/`
  - Screenshots → `~/screenshots/YYYY-MM/`
  - Installers (`.dmg`, `.zip`) → `~/Downloads/App Installers/`
- **Organizes screenshots** by modification date into `~/screenshots/YYYY-MM/` folders
- **Flags duplicates** (e.g., `file.pdf` and `file (1).pdf`)
- **Flags large files** >100MB that may no longer be needed
- **Flags stale files** in Downloads older than 30 days
- **Keeps Desktop empty**

### Rules
- **Never deletes files** — only moves and organizes
- **Shows plan before moving** — asks for confirmation on bulk moves
- If a file's destination is unclear, it asks you



## How Claude Code Skills Work

Skills are markdown files in `~/.claude/skills/` that give Claude Code specialized instructions for specific tasks. When you invoke a skill (e.g., `/Organize`), Claude reads the `SKILL.md` and follows its instructions.

## Uninstall

```bash
rm -rf ~/.claude/skills/cleanroom
```

---

<p align="center">
  <sub>Built with <a href="https://emergent.sh">Emergent</a> + <a href="https://claude.ai/code">Claude Code</a> · refined by hand</sub>
</p>
