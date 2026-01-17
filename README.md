# gh-triage

A GitHub CLI extension with tools for triaging issues and PRs.

## Installation

```sh
gh extension install hugovk/gh-triage
```

## Commands

### spam

Close an issue or PR as spam.

```sh
gh triage spam <issue-or-pr-number-or-url>
```

This will:
- Apply the "invalid" label if it exists in the repo (case insensitive)
- Apply the "spam" label if it exists in the repo (case insensitive)
- Change the title to "spam"
- Close the issue as "not planned", or close the PR

### unassign

Unassign all users and reviewers from an issue or PR.

```sh
gh triage unassign <issue-or-pr-number-or-url>
```

This will:
- Remove all assignees
- Remove all requested reviewers (PRs only)

## Options

All commands support:

- `-n, --dry-run`: Show what would be done without making changes

## Examples

```sh
# Close issue #123 as spam
gh triage spam 123

# Dry run
gh triage spam -n 123

# Unassign all from PR #456
gh triage unassign 456

# Unassign with URL
gh triage unassign https://github.com/owner/repo/pull/456
```