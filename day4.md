
# Day 4 – Branching and Merging in Git (master  final version)

## What I Learned Today
- How to create and switch branches  
  - `git branch feature-idea`  
  - `git checkout feature-idea`
- How to add new files and commit them on a branch  
  - `git add <file>`  
  - `git commit -m "message"`
- How to merge a branch back into master  
  - Switch to master: `git checkout master`  
  - Merge: `git merge feature-idea`
- How to view commit history with a visual graph  
  - `git log --oneline --graph --all`

## Key Takeaways
- Branches let me experiment without breaking master.  
- Merging is how I bring those experiments back.  
- If there’s no conflict, Git merges automatically.  
- If there *is* a conflict, Git tells me exactly where, and I have to fix it manually.

## Commands Practiced
```bash
git checkout feature-idea
echo "Learning Git Day 4" > day4.md
git add day4.md
git commit -m "Day 4: Added learning log"
git checkout master
git merge feature-idea
git log --oneline --graph --all


## Day 4 Summary (2025-08-17)
- Created a feature branch, committed changes, merged to master.
- Practiced the stage → commit cycle and used \`git status\` to track states.
- Resolved an intentional merge conflict to understand conflict markers and fixes.
- Pushed repo to GitHub (origin/master set).

**Key commands I used**
\`\`\`bash
git checkout -b <branch>
git add <file> && git commit -m "msg"
git merge <branch>
git status
git log --oneline --graph --all
\`\`\`

**Notes**
Conflicts happen when the same lines differ across branches.
Edit between \`<<<<<<<\`, \`=======\`, \`>>>>>>>\`, then \`git add\` and \`git commit\`.
