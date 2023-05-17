git 

git init : create the empty repository

git status : check the step that we take until now

git add <filename> : add file to stage

git add . : add all files to stage

git commit -m "message" : after add files to stage we should send them to repository and we do it by this command -> this command send add added files in stage to repository

git commit -a -m "message" : after make change in file that we commit in repository it change to <modified> that means it's contact changed and for commit this change we can first add this file to stage by <git add .> command and then commit it OR just do this two step by one step by this command



***git restore will restore the file to the last committed version***

git checkout -- . : discard change in files before stage them
git restore . :  to discard changes in working directory

git reset HEAD . : unstage files
git restore --staged . : unstage files

**after <git reset> should run <git checkout -- .> so change will apply.**


git reset <id commit> : back to specifice commit change
    discribe : after run above command we return to the commit that point it with it's id and it's file return to Unstaged (unstaged after reset) and for make the change apply we should run <git checkout -- . > comand.

git reset --hard <id commit> : back to specifice commit change
    discribe : without need to checkout it return completley and delete the file that then weren't or add file the at that commit were there.


------------------------------------BRANCH
git branch <branch name> : make a branch 
git chechout -b <branch name> : another way for build branch

git branch -a : show all branches
git checkout <branch name> : switch to branch <branch name>
git branch -d <branch name> : delete branch <branch name>


*** before change the branch make sure thet all changes are commited ***

merge branches => 
                first : we should switch to main branch that we wand to add another brach to it.
                last : run this command -> git merge <branch name>

git log --graph : by this command we can see the log better that means we can see witch log balong to witch branch.


*** if we change same file in two branch and merch the branch make conflict and the showing branch name change to <branch name>|MERGING 
in this case we have two options : 
            1 -> git status -> git merge --abort : this will abort the merge
            2 -> git status -> go to the file that have comflect and choose the change that you want by your hand.

            after any of this option make sure to commit all the changes.

git stash : this command help us when we have uncommited file and we don't want commit theme now but if we switch to another branch this change comes with us and we don't want it soooo with this command we save this change in stash and when we need theme we can find them in stash

another command for save stash => git stach save "message" 

git stash list : show list of stash

git stash drop <name of stash> : remove the stash (<name of stash>) 

git stash show <stash name> / git stash show -p <stash name> : show the changes

git stash pop <stash name> / git stash apply <stash name> : apply stash that not commited with <pop> it will be deleted from stash list but with <apply> it just will be apply and don't deleted from the list and we should delete it by our hand.


------------------------------------------- GITIGNOR

touch .gitignor : create .gitignor file

*** add files name to gitignore file that we want git ignore them ***

*** if we wand ignore some files that we was track theme we can use this command for clear catch :
    git rm --cached -r . -> git status -> git add . -> git commit "message"
    discription :-> first clear cache -> then check staus -> then add files that git don't ignore them to git -> and last commit this files to git.
 
 