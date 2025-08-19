# 📝 Git Cheat Sheet  

## 🔰 Basic GitHub Flow  

```bash
git init                                # Initialize a new Git repository
git remote add origin <url>             # Add remote repository (GitHub/GitLab etc.)
git pull origin main --allow-unrelated-histories   # Pull latest code (even if unrelated histories)
git checkout -b feature-branch          # Create & switch to a new branch
git add .                               # Stage all changes
git commit -m "Your commit message"     # Commit staged changes with a message
git push -u origin feature-branch       # Push branch to remote & set upstream
```

---

## 🔧 Remote Management  

```bash
git remote -v                           # List all remotes with their URLs
git remote set-url origin <url>         # Change remote URL for 'origin'
git remote rename origin upstream       # Rename remote from origin → upstream
git remote remove origin                # Remove the remote named origin
git remote add origin <url>             # Add a new remote called origin
git fetch --prune                       # Remove local references to deleted remote branches
git remote get-url origin               # Show the URL of the remote origin
```

---

## 🛠️ Branching & Merging  

```bash
git branch -d branch_name               # Delete a branch safely (won't delete if unmerged)
git branch -D branch_name               # Force delete branch even if unmerged
git push origin --delete branch_name    # Delete branch from remote
git checkout -b new_branch              # Create a new branch and switch to it
git merge branch_name                   # Merge specified branch into current branch
git pull origin main --allow-unrelated-histories   # Merge histories that are unrelated
```

---

## ✨ Commit Management  

```bash
git commit --amend -m "New message"     # Edit last commit (message or content)
git rebase -i HEAD~3                    # Interactive rebase (squash, reorder last 3 commits)
git cherry-pick <commit_hash>           # Apply specific commit from another branch
git reset --soft HEAD~1                 # Undo last commit but keep changes staged
git reset --hard HEAD~1                 # Undo last commit and discard changes
git revert <commit_hash>                # Create a new commit that undoes changes from given commit
```

---

## 🎯 Debugging & Recovery  

```bash
git reflog                              # Show history of all branch HEAD changes (recover lost commits)
git bisect start                        # Start binary search debugging to find buggy commit
git bisect good <commit>                # Mark a commit as good (no bug)
git bisect bad                          # Mark current commit as bad (contains bug)
```

---

## 📦 Stash & Cleanup  

```bash
git stash                               # Save uncommitted changes for later use
git stash list                          # Show list of saved stashes
git stash pop                           # Apply last stash and remove it from stash list
git clean -f                            # Delete untracked files
git clean -fd                           # Delete untracked files and directories
git clean -fx                           # Delete ignored + untracked files
```

---

## 🧑‍💻 Worktrees & Sparse Checkout  

```bash
git worktree add ../dir branch_name     # Create an additional working directory for a branch
git sparse-checkout init --cone         # Initialize sparse checkout mode
git sparse-checkout set path/to/folder  # Checkout only specific folder(s)
```

---

## 🏷️ Tagging & Releases  

```bash
git tag -a v1.0 -m "Release 1.0"        # Create annotated tag named v1.0
git push origin v1.0                    # Push tag v1.0 to remote
```

---

✅ Keep this file handy whenever you’re stuck!  
