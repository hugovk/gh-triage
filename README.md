# gh-spam

A GitHub CLI extension to quickly close issues and PRs as spam.

## Installation

```sh
gh extension install hugovk/gh-spam
```

## Usage

```sh
gh spam <issue-or-pr-number-or-url>
```

This will:
- Apply the "invalid" label if it exists in the repo (case insensitive)
- Apply the "spam" label if it exists in the repo (case insensitive)
- Change the title to "spam"
- Close the issue as "not planned", or close the PR

### Options

- `-n, --dry-run`: Show what would be done without making changes

## Examples

```sh
# Close issue #123 as spam
gh spam 123

# Close a PR by URL
gh spam https://github.com/owner/repo/pull/456

# Dry run to see what would happen
gh spam -n 123
```
