GIT TIPS AND TRICKS
===================

- Great explanation of what [git add remote](https://help.github.com/articles/fork-a-repo) upstream is for

- If you add a new file and then add more changes, it will appear as modified in git status.  You can run into conflicts missing that.  To prevent, git add new file again

````
set editor
    - git config --global core.editor vi
    - export EDITOR=vi

````

````
Get repo info:
git config --list
````

````
Show diff of staged files only
git diff --staged
````

````
See patch diffs in log
git log -p 
git log -p 2
````

````
Change -m to most recent commmit
git commit --amend
````

````
After a commit, add another file then amend to replace previous commit
git add <forgottenfile>
git commit --amend
````

````
Adding a remote
git remote add <remote name> <git url>
````

````
Info on remote
git remote -v
````

- Fixing conflict
When you get the crappy conflict tags, vi the file, fix it, then add, commit, and push again.

- git push -u
"Upstream" would refer to the main repo that other people will be pulling from, e.g. your GitHub repo. The -u option automatically sets that upstream for you, linking your repo to a central one. That way, in the future, Git "knows" where you want to push to and where you want to pull from, so you can use git pull or git push without arguments. 
git can set a particular branch in a remote repository to be the default "upstream" branch for that particular branch. For example, if you clone an existing repository, git will, by default, associate your master branch with the master branch in the origin repository, i.e. the one you're cloning from. This means that git can provide helpful defaults, such as being able to just use git pull while on master rather than having to specify a repository and a branch to fetch and merge from. It's also this association that lets git produce its helpful "Your branch is ahead of origin/master by 10 commits" messages...

Finding Things
=============
- language:java
- sort by forks and stars
