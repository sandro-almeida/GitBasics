### Installing git (Windows machine) ###
# Step 1: Go to the web site below and download the installation file (Git-2.15.1.2-64-bit.exe)
http://msysgit.github.io

# Step 2: Run the installation file and set the appropriate options


### Git training docs ###
https://guides.github.com/introduction/git-handbook/ 
https://git-scm.com/docs 
https://www.git-tower.com/learn/git/videos/
https://www.git-tower.com/learn/git/ebook/en/command-line/tools-services/diff-merge-tools


### Git concepts ###
.gitignore
  > Located at the root of your project, ignores files listed inside it (accept wildcards)

> At any time only one branch is active = checkout branch = HEAD

> Git is an example of a distributed version control system (DVCS). Unlike once popular centralized version control systems, DVCSs like Git don’t need a constant connection to a central repository. Developers can work anywhere and collaborate asynchronously from any time zone.

> A repository, or Git project, encompasses the entire collection of files and folders associated with a project, along with each file’s revision history. The file history appears as snapshots in time called commits, and the commits exist as a linked-list relationship, and can be organized into multiple lines of development called branches. Because Git is a DVCS, repositories are self-contained units and anyone who owns a copy of the repository can access the entire codebase and its history.

> Branching is a core concept in Git, and the entire GitHub Flow is based upon it. There's only one rule: anything in the master branch is always deployable.

> With GitHub, you can deploy from a branch for final testing in production before merging to master.


### Git commands ###
git <command> --help
  > Shows a help page for each <command>

git init
  > Create a local repository

git clone <URL>
  > Clone an existing repository

git remote add origin <URL of the repository>
  > Link the new created local repository to the <URL of the repository>; the <URL of the repository> is created in github
  > Ex: git remote add origin https://github.com/sandro-almeida/Bash-Scripts.git

git push -u origin master
  > Push the committed changes from the local project to the remote repository

git push --set-upstream origin <currentBranch>
  > Push the current branch (<currentBranch>) and set the remote as upstream
  > Ex: git push --set-upstream origin RemoveDominiosHardcoded

git pull
  > Updates local repository with updates from remote repository

git status
  > Shows an overview of your changes

git diff <fileName>
  > Shows a diff from the current version of a file and its last version

git diff --staged <fileName>
  > Shows a diff from the current staged version of a file and its last version

git difftool <fileName>
  > Open a GUI diff tool (PENDING: understand how to set up the difftool)

git add <fileName>
  > Add <fileName> to the staged area
  Ex: git add .

git rm <fileName>
  > Set the removed file to the staged area

git rm -r <dirName>
  > Recursively removes a directory and its files and includes this deletion in the staging area

git commit -m "<commit message>"
  > Commit the files located at the staged area, which creates a new node at the history tree

git log [-stat -p]
  > Shows a list of historical commits
  Ex: git log --oneline

git show --name-only
  > Lists files committed but not yet pushed

git checkout <branch>
  > Moves to a different branch

git checkout -
  > Moves to the branch earlier accessed before moving to the actual branch

git checkout <file>
  > Discard <file> changes in working directory

git branch <new branch name>
  > Creates a new branch

git branch -a
  > Shows a list of current branches

git reset
  > Unstage changes (move from the staging area to the working directory)

git reset --hard
  > Undo all changes in the working directory and staging area

git reset --hard HEAD~1
  > Removes last commit, returning to the commit before head

git reset HEAD <file>
  > Unstages <file> (<file> already added to the staging area returns to the working directory)

git reset HEAD~2
  > Undo the last 2 commits; the files created/updated on these 2 commits return to the working directory

git clean -fd
  > Remove untracked files and directories (e.g. new files and directories in the working directory)

git clean -n
  > Indicates the files to be removed but do not remove them

git merge <branch>
  > Incorporate changes from the <branch> into the current branch. Ex: assuming the current branch is master, then git command 'git merge topic' will replay the changes made on the topic branch since it diverged from master until its current commit on top of master, and record the result in a new commit

git config --list
  > List all variables (global and local) set in config file, along with their values

git config --global -l
  > List all global variables set in config file, along with their values
  
git config --global pull.rebase true
  > Adds a new configuration (pull.rebase=true) in the global config file; it indicates that the pull command will now perform a rebase operation rather than a merge

git config --global merge.ff false
  > Adds a new configuration (merge.ff=false) in the global config file; it indicates that new merge commands will no longer be fast-forward, always forcing a new commit after a merge

git config --system --edit
  > Edit the system configuration file

git fetch
  > Fetch remote tracking branches (useful when you create a branch in gitHub and this branch has not yet showed up in your local repository)

GIT_SSL_NO_VERIFY=true <git command>
  > When having problems like "fatal: unable to access '<URL>': SSL certificate problem: self signed certificate in certificate chain"
  Ex: GIT_SSL_NO_VERIFY=true git push -u origin master




