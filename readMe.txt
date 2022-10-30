To initialise a git project right click on the directory and choose git bash, then verify the path is correct and apply command `git init`

If you are doing this first time then you will need to tell git who you are by below configuration command 

git config --global user.name 'rajnikant'
git config --global user.email 'rajnikant.dankhara@gmail.com'

# remote commands
`git remote -v` command will show you your link to git remote (e.g. github.com)

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

