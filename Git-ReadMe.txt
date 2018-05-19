### Installing git (Windows machine) ###
# Step 1: Go to the web site below and download the installation file (Git-2.15.1.2-64-bit.exe)
http://msysgit.github.io

# Step 2: Run the installation file and set the appropriate options


### Git training videos ###
https://www.git-tower.com/learn/git/videos/
https://www.git-tower.com/learn/git/ebook/en/command-line/tools-services/diff-merge-tools


### Git concepts ###
.gitignore
  > Located at the root of your project, ignores files listed inside it (accept wildcards)

> At any time only one branch is active = checkout branch = HEAD


### Git commands (all start with git) ###
<command> --help
  > Shows a help page for each <command>

init
  > Create a local repository

clone <URL>
  > Clone an existing repository

status
  > Shows an overview of your changes

diff <fileName>
  > Shows a diff from the current version of a file and its last version

difftool <fileName>
  > Open a GUI diff tool (PENDING: understand how to set up the difftool)

add <fileName>
  > Add <fileName> to the staged area
  Ex: git add .

rm <fileName>
  > Set the removed file to the staged area

commit -m "<commit message>"
  > Commit the files located at the staged area, which creates a new node at the history tree

log [-stat -p]
  > Shows a list of historical commits

checkout <branch>
  > Moves to a different branch

branch <new branch name>
  > Creates a new branch

branch -v
  > Shows a list of current branches

remote add origin <URL of the repository>
  > Link the new created local repository to the <URL of the repository>; the <URL of the repository> is created in github
  > Ex: git remote add origin https://github.com/sandro-almeida/Bash-Scripts.git

push -u origin master
  > Push the committed changes from the local project to the remote repository













