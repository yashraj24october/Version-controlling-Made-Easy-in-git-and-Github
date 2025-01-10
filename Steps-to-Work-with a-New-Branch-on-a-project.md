# Steps to Work with a New Branch on a project
----------------------------------------------

### Steps:
* First need to clone the repository.

then 

* Go to main branch if not in main branch, using: git checkout main,
* You can check your current branch using: git branch

then 

* Take pull from main, using: git pull origin main

then

* Create a new branch, using: git checkout -b newBranchName

Now, 
you can start your work,

then 
After work,

* Using git add, Add your files and directories
* Using git commit -m "Add your commit message"

then 

* Push your new created branch on github, using: git push -u origin newBranchName

then
You need to create a Pull Request:

* Go to the project repository on github
* You’ll see a notification about your recently pushed branch. Click on "Compare & pull request."
* Add a title and description for your pull request.
* Assign reviewers if required, and submit the PR.

Now,
If there are updates on the base branch (e.g., main), you can incorporate them into your branch.
using:
git fetch origin
git checkout main
git pull
git checkout newBranchName
git merge main

Or, rebase instead of merging
using: 
git fetch origin
git checkout main
git pull
git checkout newBranchName
git rebase main

### Resolve Merge Conflicts (If Any)
If there are conflicts, Git will notify you. Resolve them in your editor, stage the changes, and continue
using:
git add <your files and directory path seprated with space>
git rebase --continue  # If rebasing
git merge --continue   # If merging

When you are merging branches and Git encounters conflicts, it stops and prompts you to
resolve the conflicts manually. After resolving the conflicts in the files, Git needs to know
that you've fixed the conflicts and are ready to continue the merge process.
so, again you need to add your changed files/directories using : git add

### Best Practices
* Use meaningful branch names (e.g., feature/login-functionality, bugfix/issue-123).
* Keep your branch up-to-date with the main branch to minimize merge conflicts.
* Write clear and concise commit messages.
* Push your branch frequently to avoid losing work.
* Use merge when collaborating with a team, as it preserves the context of branches.
* Use rebase for private or local branches to clean up the history before sharing it with others.
