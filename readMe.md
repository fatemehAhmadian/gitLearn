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