# Basics of Git

### Git Top 10 Commands :)

- Initialize a repository: `git init`
- Add all changes to staging: `git add .`
- View the status of the repo (optional): `git status`
- Commit changes with a message: `git commit -m "msg"`
- Add a remote repository: `git remote add origin [link]`
- Push changes to the main branch: `git push origin main`
- Pull latest changes from the main branch: `git pull origin main`
- Create a new branch: `git branch [name]`
- View commit history: `git log`
- Switch to a specific branch: `git checkout [branch name]`


### Fetch and Merge
- Fetch the latest changes from the remote main branch: `git fetch origin main`
- Merge changes from remote main into local: `git merge origin main`
- Fetch and merge in one command: `git pull origin main`

### Branch
- Create a new branch and switch to it: `git checkout -b [branch name]`
- Delete a branch: `git branch -d [branch name]`
- List all branches: `git branch`


### Rebase
- Rebase your current branch with changes from main: `git rebase main`
- Interactive rebase to combine multiple commits into one: `git rebase -i [hash]`
- Apply a specific commit from another branch: `git cherry-pick [hash]`


### Revert and Reset
- Revert a specific commit (undo changes): `git revert [hash]`
- Soft reset to previous commit (keep changes): `git reset --soft HEAD~1`
- Hard reset to previous commit (discard changes): `git reset --hard HEAD~1`


### Stash
- Save changes temporarily without committing: `git stash`
- Restore stashed changes: `git stash pop`
- Show list of stashes: `git stash list`
- Show contents of a specific stash: `git stash show stash@{1}`
- Apply a specific stash: `git stash pop stash@{1}`
- Clear all stashes: `git stash clear`


### Undo, Reflog and Restore
- Undo recent changes or commits: `git reflog`
- Hard reset to a specific commit hash: `git reset --hard [hash_no]`
- Remove changes from the staging area (before committing): `git restore --staged [file name]`

