RISISTEMARE APPUNTI



# Corso21 - Versioning Control
GIT repo for Versioning Control course of Steve Jobs Academy

## Lexicum

**Repository** is the main online directory of the project, aliases *Origin*, *Main*.

**Working directory** is the local directory of the project, aliases *Local directory*.

## GIT Commands
**git init**

Initialize the current directory to be used with git.

**git clone**

Clone a remote repository into a local working directory.

**git remote add origin**

Connect the current working directory to a remote directory.

**git add** *filename*
**git add** *.*

Add a specific file in the stage.
Using dot *.* to add all modified and untrucked files.

**git reset**

Remove all files in the stage.

**git commit**
**git commit** -am *"operation(section): commit message"*

Add a commit to be pushed.
Using the flag *-a* add all modified and untracked files in the stage before committing.
Using the flag *-m* to add a commit message to the commit.

**git push**
**git push** -u *origin branchName*
**git push** -D *branchName*

Push in the branch the changes of the commit.
Using the flag *-u* to push a branch in the origin.
Using the flag *-D* to remove a branch from the origin.

**git pull**

Pull form the original repository and update the working directory.

**git stash**

Save the changes in a stash and rollback to the file before the modifications.

**git log**
**git log** --oneline

Show the commits log.
Using the flag *--oneline* to show a short version of the log.

**git reflog**

Show all operations performed in the working directory, useful to catch the rollback id.

**git reset [--soft | --hard]** *commitID*

Rollback to a previous version of the code, with --safe bring all the modifications previously done.
Losing all commit done after the rollback point.

**git checkout**
**git checkout [-b]** *commitID | branchName*

Move HEAD to the version where commitID was pushed, showing the project in a specific time.
If branchName is passed, move HEAD to branch.
Using flag *-b* create a new branch and move to it.
branchName tips: operation/specification (i.e. feature/header)

**git branch**
**git branch** -d

Create a new branch.
Using the flag *-d* to remove a branch. Remember to move away from a branch before delete one.

**git switch** *branchName*

Change branch.

**git merge** *branchName*

merge branch to origin.

**git blame** *filename*

Show who modified the file.

**git grep "string"**

Global search of the string.

**git revert commitID**

Rollback mantaining the commit done after the rollback point.

# Metodologie
**continuous development integration**

**trunk-based development**
Baso lo sviluppo su iterazioni veloci.
Each developer create a new branch from the main, then perform a merge or a replace.
Merge add two branches, pushing the commits of the derivated branch to the main branch.

**Enviroments**

**Stage** for developer to develop software and test new features

**Production** for hosting 

**branches**

- **Feature**: create something new
- **Bugfix**: fix bug for stage enviroments
- **Hotfix**: fix bug of production enviroments
- **Test**: test new features
- **Refactor**: rewrite feature or reorganize working directories (scuffholding)
- **Build**: new version added to production


**git flow**
quando creo nuove branch e faccio il merge/rebase lo faccio sulla branch develop, non sul main

# Work flows

- creo una branch ( git branch name , git checkout -b name )
- cambio branch ( git switch name )
- sincronizzo la branch con la origin ( git push -u origin name , solo la prima volta )
- effettuo i cambiamenti che voglio fare
- pusho i cambiamenti ( git -am "commit" && git push )
- faccio il merge con la origin ( git merge name )
- forzo il push ( git push -f )
- elimino la branch locale ( git branch -d name )
- elimino la branch da origin ( git push -D name )


rebase

- 
- git rebase name

Metodologie

con git flow committo su development e non sul main, succcessivamente il devops provvederà ad aggiornare la produzione da development.

con integrazioni veloci creo branch da committare al main.



Rebase aggiorno una branch figlia in corrispondenza alle modifiche del ramo principale.
Serve quando una modifica serve a tutte le branch figlie, lo addo al main e gli altri effettuano il rebase.