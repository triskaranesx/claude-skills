# Sync Branch

Keep your current branch up to date with the main branch.

## Usage

```
/git/sync
```

## What this does

1. Fetches latest changes from origin
2. Checks out the main branch (main or master)
3. Pulls latest changes
4. Checks back out your working branch
5. Rebases your branch on top of main

## Steps

```bash
# Save current branch name
CURRENT_BRANCH=$(git rev-parse --abbrev-ref HEAD)

# Fetch all remotes
git fetch origin

# Determine default branch
DEFAULT_BRANCH=$(git remote show origin | grep 'HEAD branch' | awk '{print $NF}')

# Pull latest on default branch
git checkout $DEFAULT_BRANCH
git pull origin $DEFAULT_BRANCH

# Return to working branch and rebase
git checkout $CURRENT_BRANCH
git rebase $DEFAULT_BRANCH
```

## Notes

- If rebase conflicts occur, resolve them manually then run `git rebase --continue`
- To abort a conflicted rebase: `git rebase --abort`
- Prefer rebase over merge to keep a clean linear history
