> To initialise a git project right click on the directory and choose git bash, then verify the path is correct and apply command `git init`

If you are doing this first time then you will need to tell git who you are by below configuration command 

> create ssh key
- git config --global user.name 'rajnikant'
- git config --global user.email 'rajnikant.dankhara@gmail.com'

> to change defaut branch name e.g main or master 
`git config --global init.defaultbranch 'main'`  so next time repo created with name main 

### Remote commands
`git remote -v` command will show you your link to git remote (e.g. github.com)

> To Update url to origin
`git remote remove origin` will remove 
`git remote add origin url `

# commit and push
`git add .`
`git commit -m 'message'`
`git push origin name-of-branch`

# branching commands
`git branch` command will list all the branches in your current project

`git checkout -b name-of-branch` will create new branch with name name-of-branch

`git checkout name-of-branch` will switch to branch name-of-branch

`git branch -M main` to change git name of git branch

# delete branch commands

`git push --delete origin name-of-branch`

`git branch -D name-of-branch` will delete branch from your local machine

# synchronizing (update your local branch from remote)

`git fetch` (first to get changes from remote)

`git checkout main` if not on main or master already

`git pull origin main`

> before doing any of these check your commit is there in 
`git reflog --date=iso` if you see your change here you can always get it by command `git reset --hard "HEAD@{2022-10-30 10:19:07 +0000}"`

> reset 
`git reset --soft HEAD~3` this will keep change on your local branch
`git reset --hard HEAD~3` this will discard the changes of commit

> stash
`git stash` to park changes temporary 
`git stash apply` to get temporary changes from stash, but also keep it in stash list  
`git stash pop` to get temporary changes from stash, and delete it from the stash list 

> squash, amend 
`git rebase -i HEAD~4` will let you squash or amend changes in last 4 commits
in VI editor press `INSERT key to start editing` once edited press `ESCAPE` and at : enter wq to save or q to not save

