aaa
bbb
# git --mixed default, keep the file in stage arear contemperary
# with commit before; work arear unchanged.

# we submit file to stage area but not commit to repository, then 
# use git reset --mixed HEAD to see what will happen.
#1. this content discarded
#2. this content now stored in work arear and stage arear,
#	after this order, work arear not changed that we can use vim to check, but stage arear changed, we need using git add . to readd file to stage arear.

# git --soft, does not touch the index file or the working tree at all (but resets the head to <commit>	, just like all modes do). this leaves all your changed files "changes to be commit", as git status would put it.
# use git reset --soft HEAD to see what will happen.
#1.the work arear and stage arear not changed. we can use commit to submit file without readding the file to stage.
#2.work arear not changed. the stage arear will backward and we need to readd the file.

