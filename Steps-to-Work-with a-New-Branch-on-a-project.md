# Steps to Work with a New Branch on a project
----------------------------------------------

### Steps:
* First ensure you are added as collaborator and have write permission to collaborate on project repo
* If you have not "write" permission, then you need to "fork" the repository.
* It will create a copy of repo in your github.
 then 
* You need to clone the repository.

If you have "write" permission, you can directly clone the repo.

then,

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
* git fetch origin
* git checkout main
* git pull
* git checkout newBranchName
* git merge main

Or, rebase instead of merging
using: 
* git fetch origin
*git checkout main
* git pull
* git checkout newBranchName
* git rebase main

### Resolve Merge Conflicts (If Any)
If there are conflicts, Git will notify you. Resolve them in your editor, stage the changes, and continue
using:
first, 
* git add your files and directory path seprated with space

now, 
in case of rebasing,
* git rebase --continue

in case of merging,
* git merge --continue

When you are merging branches and Git encounters conflicts, it stops and prompts you to
resolve the conflicts manually. After resolving the conflicts in the files, Git needs to know
that you've fixed the conflicts and are ready to continue the merge process.
so, again you need to add your changed files/directories using : git add

### Confirming merge
After merging your branch to main/anyBranch, to confirm your merge, we can do:
* git log --oneline
This will show you the commit history with a merge commit

### After merge your branch on local main, Ensure Your Local main is Up-to-Date

 Now,
 To reflect the changes on GitHub (remote repository), you need to push the merged main branch, using:
 * git push origin main
   
Now,
Check the remote repository
* Go to your repository on GitHub and check the main branch to see if the changes from yourNewBranch have been integrated.

### Best Practices
* Use meaningful branch names (e.g., feature/login-functionality, bugfix/issue-123).
* Keep your branch up-to-date with the main branch to minimize merge conflicts.
* Write clear and concise commit messages.
* Push your branch frequently to avoid losing work.
* Use merge when collaborating with a team, as it preserves the context of branches.
* Use rebase for private or local branches to clean up the history before sharing it with others.

### Key Summarized points:
* All the branches you work on locally on your system are local branches in Git.These branches are not visible to others or in the remote repository until you push them.
* First you create your local branches then after all works, you push your local branches to remote to make them visible to others.
* After finishing work on local branches, you switch to local main, you merge your local branches with local main, then push the updated local main to remote main on github to reflect change remotely on github.


## Note: For collaborater without having 'write' permission, they cannot merge their local main to remote main directly, they need to follow below steps:
* Fork the repository to create a copy of it under their GitHub account.
* Clone their forked repository to their local machine.
* Make changes and push them to their fork.
* Create a pull request from their fork to the original repository to propose the changes.

For creating a pull request:
they can go to the GitHub page of their forked repository (not the original repository).
From there, they can create a pull request to propose merging their changes from their fork into the original repository's main branch (or any other branch they're working with).
After that the repo owner will review and merge their changes.

