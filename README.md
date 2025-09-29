# gh-delete-repos

Clean up local Git repositories that no longer exist on GitHub.

## Motivation

When using tools like [gh-clone-org](https://github.com/matt-bartel/gh-clone-org), you might end up with many local repositories that have since been deleted from GitHub. This script helps identify and remove those orphaned local repos.

## Usage

```bash
# See what would be deleted (recommended first step)
gh delete-repos --dry-run

# Interactive cleanup
gh delete-repos

# Auto-delete without prompts
gh delete-repos --yes
```

## Requirements

- `gh` (GitHub CLI): `brew install gh`
- Authenticated: `gh auth login`

## ⚠️ USE WITH CAUTION

This script **permanently deletes** local directories. Always run with `--dry-run` first to see what would be removed.

---

*Scans subdirectories for Git repos, checks if they exist on GitHub, and optionally deletes local copies of repositories that are no longer available remotely.*