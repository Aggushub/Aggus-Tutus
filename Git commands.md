## Git Commands with Use and Test Cases

### Repository Management

1. **git init** - Initialize a new git repository

   * `git init` – Creates a new .git folder in the current directory

2. **git clone** - Clone a repository

   * `git clone https://github.com/user/repo.git` – Copies remote repo locally

3. **git config** - Set configuration options

   * `git config --global user.name "John Doe"`
   * `git config --global user.email "john@example.com"`

---

### Staging and Committing

4. **git add** - Add files to staging area

   * `git add file.txt`

5. **git commit** - Commit staged changes

   * `git commit -m "Initial commit"`

6. **git status** - Show working directory status

   * `git status`

7. **git diff** - Show differences between changes

   * `git diff`

---

### Branching and Merging

8. **git branch** - List, create, or delete branches

   * `git branch` – Lists branches
   * `git branch new-feature` – Creates new branch

9. **git checkout** - Switch branches or restore files

   * `git checkout new-feature`

10. **git switch** - Alternative to checkout for branches

    * `git switch main`

11. **git merge** - Merge branches

    * `git merge new-feature`

12. **git rebase** - Reapply commits on top of another base

    * `git rebase main`

---

### Remote Repositories

13. **git remote** - Manage remotes

    * `git remote add origin https://github.com/user/repo.git`

14. **git push** - Push changes to remote repo

    * `git push origin main`

15. **git pull** - Fetch and merge from remote

    * `git pull origin main`

16. **git fetch** - Download objects from remote

    * `git fetch origin`

---

### History and Logs

17. **git log** - Show commit logs

    * `git log`

18. **git show** - Show a specific commit

    * `git show abc1234`

19. **git blame** - Show who modified each line of file

    * `git blame file.txt`

20. **git reflog** - Show reference logs

    * `git reflog`

---

### Undoing Changes

21. **git reset** - Unstage files or reset commits

    * `git reset HEAD file.txt`
    * `git reset --hard abc1234`

22. **git revert** - Create a new commit that undoes changes

    * `git revert abc1234`

23. **git clean** - Remove untracked files

    * `git clean -f`

---

### Stashing and Tags

24. **git stash** - Temporarily save changes

    * `git stash`
    * `git stash pop`

25. **git tag** - Tag specific points in history

    * `git tag v1.0`
    * `git push origin v1.0`

---

### Example Workflow

```bash
git init
touch README.md
git add README.md
git commit -m "Add README"
git remote add origin https://github.com/user/repo.git
git push -u origin main
```

Run these commands in a project directory to initialize and push to a remote GitHub repo.
