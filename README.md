# corso21
GIT repo for Versioning Control course of Steve Jobs Academy

# GIT Commands
git init
Initialize the current directory to be used with git.

git remote add origin
Connect the current working directory to a remote directory.

git add filename.ext
Add a specific file in the stage.

git add .
Add all modified and untrucked file in the stage.

git reset
Remove all files in the stage.

git commit -m "operation(section): message"
Add a commit to be pushed.

git commit -am "git add and commit"
Add all modified and untracked file in the stage and the commit to be pushed.

git push
Push in the branch the changes of the commit.

git pull
Pull form the original repository and update the working directory.

git stash
Save the changes in a stash and rollback to the file before the modifications.

git log [--oneline]
Show the commits log.

git reset [--soft] commitID
Rollback to a previous version of the code, with --safe bring all the modifications previously done.