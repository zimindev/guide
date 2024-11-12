
# Mini Guide to Git

Git is a distributed version control system that helps developers track changes in their code and collaborate effectively. Below is a quick guide to help you get started with Git.

## 1. Install Git

Before you begin, make sure Git is installed on your system. You can check if Git is installed by running:

```bash
git --version
```

If Git is not installed, you can download and install it from [git-scm.com](https://git-scm.com/).

## 2. Configure Git

Set your username and email to associate with your commits:

```bash
git config --global user.name "Your Name"
git config --global user.email "youremail@example.com"
```

## 3. Create a Repository

To start a new Git project, navigate to your project folder and run:

```bash
git init
```

This initializes a new Git repository.

## 4. Cloning a Repository

To clone an existing repository from GitHub or another Git host:

```bash
git clone https://github.com/username/repository.git
```

## 5. Check the Status

To see the current status of your files (modified, added, or removed), use:

```bash
git status
```

## 6. Staging Changes

Before committing changes, you need to stage them:

```bash
git add <filename>        # Stages a specific file
git add .                 # Stages all changes
```

## 7. Committing Changes

Once changes are staged, commit them:

```bash
git commit -m "Your commit message"
```

Use descriptive commit messages to explain the changes you've made.

## 8. Viewing the Commit History

To view your commit history:

```bash
git log
```

## 9. Pushing Changes

To push your local changes to a remote repository (e.g., GitHub):

```bash
git push origin main      # Push changes to the 'main' branch
```

## 10. Pulling Changes

To pull the latest changes from the remote repository:

```bash
git pull origin main      # Pull changes from the 'main' branch
```

## 11. Creating and Switching Branches

To create a new branch:

```bash
git checkout -b new-branch
```

To switch to an existing branch:

```bash
git checkout existing-branch
```

## 12. Merging Branches

Once you've finished working on a branch, you can merge it into another:

```bash
git checkout main         # Switch to the branch you want to merge into
git merge new-branch      # Merge 'new-branch' into 'main'
```

## 13. Resolving Merge Conflicts

If Git cannot automatically merge changes, you will need to resolve the conflicts manually. After resolving, stage the resolved files:

```bash
git add <filename>
```

Then commit the merge:

```bash
git commit -m "Resolved merge conflict"
```

## 14. Deleting a Branch

To delete a branch after merging:

```bash
git branch -d branch-name
```

For remote branches:

```bash
git push origin --delete branch-name
```

## 15. Reverting Changes

If you need to revert to a previous commit:

```bash
git checkout <commit-id>  # Checkout a specific commit
```

If you want to undo your last commit:

```bash
git reset --soft HEAD~1   # Undo last commit but keep changes
git reset --hard HEAD~1   # Undo last commit and discard changes
```
