## GIT ##
[Worknig with Git](https://github.com/garagegames/torque2d/wiki/Cloning-the-repo-and-working-with-Git)
[High level commands](http://rogerdudler.github.io/git-guide/)
[Good article](https://blogs.msdn.microsoft.com/kaevans/2014/03/26/git-for-team-foundation-developers/)

**Concepts:**
- Repo: THe project source code that resides on GitHub.
- Fork: Create a copy of the else's original copy to ones own repo.
- Cloning: Clone/ copy an online repo to local machine.
- Branch: Different version of same project (within a repo).
- Remote: An alias pointing to an online repo.
- Staging Area: Staging/ updating files, ready to be checked in.

**Imp commands**
- Fetch: Downloads current state of a Repo, including branches, w/o modifying current report. (Places files under .git/Fetch-Ahead).
- Merge: Merge modifications of another branch into current directory.
- Pull: (combination of Fetch and Match commands), Fetches info from online repo and merges into local copy.
- Add: Adds a modified (or added) file to staging area, reparing files to be checked in.
- Commit: Records snapshot of staging area, and makes it ready to be pushed.
- Push: Upload local changes to remote repo.


### Config ###
- System
  - stored in /etc/gitconfig or C:\Program Files(x86)\Git\etc\gitconfig
  - applies to entire computer
  - access using command> git config --system
- User level (global)
  - stored in  ~/.gitconfig or c:\users\<username>\.gitconfig
  - applies to the user name
  - access using command> git config --global
- Repository level
  - stored in in repo under .git/config
  - applies to that repository only.
  - access using command> git config
- Configuring git.
  - its common to modify global or repo level config file
  - Exmpale commands below to set some common properties.
    - > git config --global user.name "yshah"
    - > git config --global user.email "yatin72@hotmail.com"
    - > git config --global --list
    - > cat ~/.gitconfig

INitialize  repo
- run command> git init
- run> git add <case sensitive file name> to 'stage' files to check into.
- 

#### Git commands ####
```batch
Git commands used:

git init
git log
git status
git add -u
git add -A
git add -am
git add <filename>
git commit -m "some comment here"
git reset --hard <sha1 OR Head~n>
git reset --soft <sha1 OR Head~n>
git clean
git clean -n
git clean -f
.gitignore
git log --oneline
git log --online --graph
git shortlog -sne
git show <head or sha1>
git remote
git remote -v
git branch
git branch -r
git tag

(for the command below, do create the repo online first.)
git remote add <basename> https://github.com/<username>/<reponame>
 
git branch -r
git pull ==> git fetch <reponame>; git merge BaseRepo/master
git branch --set-upstream master BaseRepo/master
git push BaseRepo  master
git remote rm BaseRepo
git tag <name>
git tag
git tag -a v1.0 -m " some message"
git tag -s v1.0_signed -m "signed tag"
git tag -v v1.0
git push --tag

git log --graph --oneline --all --decorate
git config --global alias.lga "log --graph --online --all --decorate"
git branch <name> [<sha1>]
git branch -m <currentname> <newname>
git branch -d <name>
git branch -D <name>
git checkout -b <newname>
git reflog ==> [git keeps the reflog worth of 30 days]
git branch <name> <sha1> ==> [restores a branch with that sha1]
git show HEAD
git stash
git stash list
git stash apply ==> [restores recursively]
git stash pop 
git stash drop
git stash branch <name>
git merge <branchname> ==> merges the branchname to the current branch.
git mergetool
git diff --cached
git rebase <branchname> ==> pruns the current branch and puts on top of the branchname.
git rebase --continue ==> resume further conflicts
git cherry-pick <sha1> 
git fetch <remote> <local branch>
git push
git push <remote> <local branch>
git branch -r
git push <remote> <local branch>:<new remote branchname>
git push <remote> :<new remote branchname> ==> this command deletes the named remote branch name

Notes: (IMP)
[branches are labels on sha1 of the individual commits]
[branches will follow commits and they will move along checkins whiile tags remains on the same commit, they are friendly names on sha1]

```
