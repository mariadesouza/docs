#GIT 

## Cheat Sheet
### 

* Verify user settings
> git config user.name
> git config user.email
> git config --list

* Set a new username
> git config user.name "me myself"

* Get repo 
> git clone https://github.com/user/repo.git

* Renaming a branch
> git branch -m <oldname> <newname>

* lists the branches that have been merged into the current branch
> git branch --merged 

* lists the branches that have not been merged
> git branch --no-merged 

* Delete a branch
> git branch -d the_local_branch
> git push origin --delete <branch>

* Changing a commit message
> git commit --amend

## Known Errors and Solutions

* error: src refspec [branch] does not match any.

Created a new branch. Committed files. 
Tried git push origin [branch]. Got above error.
Resolved by:
> git push origin HEAD:[branch] 

> git show-ref to see what refs do you have. 

