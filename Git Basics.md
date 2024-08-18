# Basics Codes

- ***git commit***
- ***git branch (your branch name)*** : To split a branch
- ***git checkout (your branch name)*** : If you want to check out a branch
- ***git checkout -b (your branch name)*** : If you want to create a new branch AND check it out at the same time, you can simply type git checkout -b [yourbranchname]
- ***git merge(your branch name)*** : To merge the branch
- ***git rebase(your branch name)*** : Select on the other branch other than main branch i.e the new branch created from main. Now run the rebase command to coppy whatever was available into 


## Moving around Git

Head is where you can move in between the commits we use head.

- git checkout HEAD~3 : HEAD is default always in the current checkout branch , It will go to
- git checkout c3 : To move the head to a position . (In LearnGitBranching)
- git branch -f main HEAD : This is used to move the branch main from one place to the head places.
- git checkout (yourbranchname)^
- git checkout c2
- git checkout main^^
- git checkout main^^^
- git branch -f main HEAD~4

Git Reverse

- git reset HEAD~1 : Will remove the current commit location to previous version removing the current version.
git reset reverses changes by moving a branch reference backwards in time to an older commit. In this sense you can think of it as "rewriting history;" git reset will move a branch backwards as if the commit had never been made in the first place.

Git Revert
While resetting works great for local branches on your own machine, its method of "rewriting history" doesn't work for remote branches that others are using.
In order to reverse changes and share those reversed changes with others, we need to use git revert. 

- git revert HEAD
