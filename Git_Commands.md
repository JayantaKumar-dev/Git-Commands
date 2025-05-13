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
🔍 Git Architecture Explained
1️⃣ Working Tree
The Working Tree is where all the files for your project are stored on your local machine.

2️⃣ Staging Area (Index)
The Staging Area is a "pre-commit" area where changes are added before being committed using git add.

3️⃣ Local Repository
Your local .git folder that stores all the commits and project history.

4️⃣ Central Repository (Remote)
Hosted on platforms like GitHub, GitLab, or Bitbucket. Team members push and pull from this repository.

🔧 Git Commands
1. git init
Initializes a new Git repository in the current directory.

bash
Copy
Edit
git init
2. git status
Shows the status of changes as untracked, modified, or staged.

bash
Copy
Edit
git status
3. git add
Adds changes to the staging area.

bash
Copy
Edit
git add test.txt
git add .       # Adds all files
4. git commit
Commits staged files to the local repository.

bash
Copy
Edit
git commit -m "Commit message describing changes"
5. git push
Pushes committed changes to the remote repository.

bash
Copy
Edit
git push origin main
6. git restore
Used to discard changes in the working directory or unstage files.

bash
Copy
Edit
git restore test.txt               # Discard changes
git restore --staged test.txt     # Unstage changes
7. git log
Displays commit history.

bash
Copy
Edit
git log
git log --oneline   # Simple summary
8. git rm
Removes a file from the working directory and stages the deletion.

bash
Copy
Edit
git rm file_name.txt
git commit -m "Remove file"
git push origin main
9. git clone
Creates a copy of an existing Git repository.

bash
Copy
Edit
git clone https://github.com/username/repository.git
🔄 10. git pull
Fetches and merges changes from the remote repository.

bash
Copy
Edit
git pull origin main
🆚 git pull vs git fetch
a. git pull
Downloads and merges remote changes into your branch.

bash
Copy
Edit
git pull
b. git fetch
Downloads changes but does not merge them automatically.

bash
Copy
Edit
git fetch
git merge
11. git gui
Opens the Git GUI interface for performing Git operations visually.

bash
Copy
Edit
git gui
12. git stash
Temporarily saves uncommitted changes for later.

bash
Copy
Edit
git stash          # Stashes changes
git stash apply    # Applies stashed changes
13. git cherry-pick
Applies a specific commit from another branch.

bash
Copy
Edit
git cherry-pick <commit-id>
📌 Interview Question:
You have done 5 commits today but want to merge only the 3rd commit into a branch. What will you do?
✅ Answer: Use git cherry-pick.

Note: git merge merges all commits, while git cherry-pick merges specific ones.
