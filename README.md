# gitstuffs

`git branch`     -> shows all local branches   
`git branch -r`  -> shows all remote branches  
`git branch -a`  -> shows all branches local and remote

`git add -A`  -> adds all
`git add -u`   -> adds modified only
`git add . `  -> adds all files in sub directories as well 

> origin = remote
pull = fetch + merge  -> bringing remote changes into my local repo
`git reset`   -> pulls branch from last commit
`git reset --hard head`     -> puts you back to where you were before changes
`git reset --hard commitId`   -> puts you back to that commit

am - fetch on dev/fetch on feature branch/if there are changes on dev switch and pull 
pm - commit/push to remote

merge conflicts - start at bottom and work up
pull request - push branch/pull from origin develop
merge to dev or master - got to branch/click merge / delete branch

> workflow: 
> - `git checkout develop` 
> - `git pull`
> - `git checkout featureBranch`
> - `git merge develop` (maybe with "--no-ff --no-commit" options)

**basic workflow: add/commit/pull/push**

** Start a new feature workflow **
git checkout -b new-feature master
** Edit some files **
```git add <file>
git commit -m "Start a feature"
# Edit some files
git add <file>
git commit -m "Finish a feature"
# Merge in the new-feature branch
git checkout master
git merge new-feature
git branch -d new-feature ```

`git reset fileName`  -> removes that file from staging
on branch: `git pull origin master(or other remote branch)`  -> pulls that remote into current branch
`git branch -m <oldname> <newname>`  -> renames (moves) a branch
`git branch -m <newname>`  -> renames (moves) current branch
`git branch -d <branchname>`   -> deletes branch branchname 
`git branch newBranchName`   -> creates a new branch named newBranchName
  
`git stash` --> **use with extreme caution**
`git stash apply`
`git stash list`
> git checkout failed due to untracked files - find out what is going on with those files and probably delete them this is a merge conflict

`git remote -v`   -> shows which remote you are tied to 

`git config --global core.editor "notepad++.exe --muliInst -nosession"`  -> set notepad++ to be default editor (instead of EMACS)
`git config --global -e` 

`git init projectName`  -> do this in the folder that you want to project to go into. This will create a folder named projectName in current folder

`git add filename` -> adds to stage and starts tracking
`git commit -am "message"`  -> adds/commits with message

`git checkout -- fileName`   -> gets a file back to the state of the last commit

`git log --abrev-commit`  -> shows log with abbreviated commit id (7 chars)
`git log --oneline --graph --decorate`  -> similar to gitk
`git log --since="3 days ago"`   or "today" or "yesterday"
`git log -- fileName`   -> just shows that filename



