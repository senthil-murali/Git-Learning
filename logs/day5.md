# Day 5 – Repo Cleanup and Standardization

## Goals for the Day
- Clean the repo and remove unwanted build artifacts.
- Standardize note format and storage going forward.
- Add a proper README for clarity and polish.
- Mark a milestone with a new tag.

---

## What I Learned
- **HEAD vs origin/master**:  
  - `HEAD -> master` = my local branch pointer.  
  - `origin/master` = the remote branch on GitHub.  
- **Interactive rebase (`git rebase -i`)**: how to squash/reword commits to make history cleaner.
- **.gitignore behavior**: it only stops *new* files from being tracked; already tracked files must be removed with `git rm --cached`.
- **Force pushing safely**: `git push --force-with-lease` is the safer way to update remote after rewriting history.
- **Milestone tags**: creating annotated tags (`git tag -a v0.2 -m "message"`) to freeze repo progress at clean checkpoints.

---

## Actions Taken
- Removed the unwanted `log/` folder from tracking.  
- Updated `.gitignore` to exclude build artifacts, OS junk, and editor settings.  
- Added a new `README.md` with repo purpose, links to daily logs, and a summary of skills learned.  
- Decided to leave old `.txt` files as-is but **standardize on `.md` for all new logs** from now on.  
- Created milestone tag **v0.2** after cleanup and documentation.

---

## Commands Practiced
```bash
git rebase -i HEAD~2
git commit --amend
git rm -r --cached log/
git mv
git push --force-with-lease origin master
git remote show origin
git tag -a v0.2 -m "Repo cleaned and standardized"
git push origin v0.2
