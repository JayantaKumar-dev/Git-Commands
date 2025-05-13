# 🛠️ Source Code Management Tool (SCM)

## 📌 Key Features

- **Version Control**: It allows teams of developers to keep track of changes to their codebase.
- **Collaboration**: It enables multiple developers to work together on the same project.
- **Continuous Integration/Continuous Deployment (CI/CD)**:  
  It integrates with various CI/CD tools (like GitHub Actions, Jenkins, and Travis CI) to automate testing, building, and deploying your code.

## 💡 Examples

1. GitHub  
2. Bitbucket  
3. ClearCase  
4. SVN

---

## 🔁 GitHub and Git

### 🧰 Prerequisites

1. Create a GitHub account
2. Install Git on your local system
3. Configure name and email using the following commands (One-time configuration):

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

## 🔍 Git Architecture Explained
### 1️⃣ Working Tree
The Working Tree is where all the files for your project are stored on your local machine.

### 2️⃣ Staging Area (Index)
The Staging Area is a "pre-commit" area where changes are added before being committed using git add.

### 3️⃣ Local Repository
Your local .git folder that stores all the commits and project history.

### 4️⃣ Central Repository (Remote)
Hosted on platforms like GitHub, GitLab, or Bitbucket. Team members push and pull from this repository.

## 🔧 Git Commands

### 1. git init
Purpose: Initializes a new Git repository in the current directory.

Usage: You run this command in a project folder to convert it into a Git repository. It creates a .git directory where Git stores all its configuration files and version history.

```bash
git init
```

### 2. git status
Purpose: Shows the current status of the working directory and staging area.
Usage: This command is used to check whether there are any modified, added, or deleted files in the working directory that need to be staged or committed.

```bash
git status
```
It will show if files are untracked, modified, or staged.

### 3. git add
Purpose: Adds files or changes to the staging area (index) in preparation for a commit.
Usage: You specify the file(s) to add or use a wildcard (e.g., git add . to add all files).

```bash
git add test.txt
git add .       # To add all Changes
```

### 4. git commit
Purpose: Commits the staged files to the local repository, saving your changes along with a commit message.
Usage: This records your staged changes and adds them to the local repository’s history.

```bash
git commit -m "Commit message describing changes"
```

### 5. git push
Purpose: Pushes the committed changes from the local repository to the central repository (remote repo like GitHub).
Usage: After committing locally, use this to share your changes with others by sending them to the central repository.

```bash
git push origin main  # Push changes to the "main" branch
```

### 6. git restore
Purpose: Used to undo changes in the working directory and the staging area.
Usage:
If a file is unstaged, git restore will discard local changes made to that file.
If a file is staged, git restore --staged will unstage the file but keep the changes in the working directory.

```bash
git restore test.txt               # Discard changes
# Unstage a staged file (without discarding changes):
git restore --staged test.txt     # Unstage changes
```

### 7. git log
Purpose: Displays the commit history, including commit IDs, author information, dates, and commit messages.
Usage: This is useful to view the history of changes made to the project.


```bash
git log
# To view a simpler summary, you can add options:
git log --oneline   # Simple summary
```

### 8. git rm
Purpose: Removes a file from both the working directory and the staging area, and it schedules the deletion for the next commit.
Usage: If you want to delete a file, this command removes it and stages the change for the commit.

```bash
git rm file_name.txt
git commit -m "Remove test.txt"
git push origin main
```

### 9. git clone
Purpose: Downloads a copy of an existing Git repository (usually from a remote central repository) to your local system.
Usage: This command is typically used when you want to start working on an existing project and need a copy of the central repository on your machine.

```bash
git clone https://github.com/username/repository.git
```

#### 🔄 10. git pull

Purpose: Fetches and merges changes from the central repository to your local repository.
Usage: Use this to keep your local repository up to date with changes made by other collaborators. However, conflicts may arise if your local changes clash with those on the central repo.

```bash
git pull origin main
```
Note: Conflicts occur when there are changes in the same part of a file in both your local and the central repository. You’ll need to manually resolve these conflicts.

### 11. git gui
Purpose: Opens the Git GUI tool, which is a graphical user interface (GUI) for interacting with Git repositories.
Usage: Some users prefer to use a GUI rather than the command line to manage their repositories. The git gui tool provides a more visual interface for Git operations like commit, branch, and status management.

```bash
 git gui
```

This will open a graphical tool where you can perform many of the Git operations like staging, committing, and viewing the commit history without needing to use

#### git pull versus git fetch
___________________________
#### a. git pull

- Downloads changes from the remote repository (e.g., GitHub, GitLab) to the local repository.
- Automatically merges the fetched changes into your current working branch.
- May cause merge conflicts if there are conflicting change

EX:
```bash
git pull
```

#### b. git fetch
_______________
- Downloads the latest changes from the remote repository but does not merge them into your working branch.
- This is a safe operation because it allows you to review the changes before merging.
- The fetched changes are stored in origin/<branch>, and you can manually merge them when ready.

Ex:
```bash
git fetch
git merge
```
______________________________________________________________________________________________________________________
### 12. git stash:
_______________
- git stash is a command used in Git to temporarily save changes that are not yet committed to work on something else without losing your modifications.
- when you run git stash, all your modified but unstaged or staged changes are temporarily stored in a hidden area

```bash
git stash - to store changes in temp area
git stash apply - to get the changes from temp area back
```



### 13. git cherrypic:
__________________
- git cherry-pick is used to apply a specific commit from one branch to another without merging the entire branch.

**Interview Question?**

You have done today 5 commits, but you want to merge only 3rd commit to particular branch, how will you do?
Answer:
```Bash 
git cherrypic
```

Note: git merge will merge all the commit to a particular branch

_______________
