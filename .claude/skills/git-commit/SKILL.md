---
name: git-commit
description: |
  Stage source code and create commits with validated commit messages. Use when users ask to commit changes, create commits, stage and commit files, or save changes to git. Enforces commit message format with lowercase prefix (build, chore, ci, docs, feat, fix, perf, refactor, revert, style, test) and lowercase message start.
---

# Git Commit

Stage source code changes and create commits following strict commit message format rules.

## Commit Message Format

**Required format:** `<prefix>: <message>`

**Rules:**
- Prefix must be lowercase
- Message must start with lowercase letter
- Prefix and message separated by colon and space

**Valid prefixes:**
- `build`
- `chore`
- `ci`
- `docs`
- `feat`
- `fix`
- `perf`
- `refactor`
- `revert`
- `style`
- `test`

## Examples

**Valid:**
```bash
fix: some message
feat: add new feature
docs: update readme
```

**Invalid:**
```bash
Fix: some message       # prefix not lowercase
fix: SomeMessage        # message not lowercase
foo: some message       # invalid prefix
fix:some message        # missing space after colon
: some message          # prefix empty
fix:                    # message empty
```

## Workflow

### 1. Check current status
```bash
git status
```

### 2. Stage files
```bash
# Stage specific files
git add <file1> <file2>

# Stage all changes
git add .
```

### 3. Create commit
```bash
git commit -m "<prefix>: <message>"
```

## Tips

- **Small commits:** Stage related files in small chunks after completing a task
- **Clear messages:** Be specific about what changed and why
- **Choose correct prefix:** Match the prefix to the type of change
- **Validate first:** Always validate commit message format before committing
