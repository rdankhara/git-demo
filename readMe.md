> To initialise a git project right click on the directory and choose git bash, then verify the path is correct and apply command `git init`

If you are doing this first time then you will need to tell git who you are by below configuration command 

- git config --global user.name 'rajnikant'
- git config --global user.email 'rajnikant.dankhara@gmail.com'

> To change default branch name e.g. main or master 
`git config --global init.defaultbranch 'main'`  so next time repo created with name main 

> to verify all your configuration use command `git config --global/--local -g`

### SSH Key configuration
> To generate ssh key 
1. open git bash
2. open this link [generate ssh key](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
3. enter command on git-bash `ssh-keygen -t ed25519 -C "your_email@example.com"` then enter, don't enter any password, just hit enter, enter again 
4. enter command on git-bash `eval "$(ssh-agent -s)"`
5. enter command on git-bash `ssh-add ~/.ssh/id_ed25519`
6. open this link [add key to your git hub account](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account)
7. enter command on git-bash `clip < ~/.ssh/id_ed25519.pub` this command will copy your public key into your clipboard
8. now you need to paste it into your github account, so got to settings, ssh - gpg key section, new key, give any name and paste in big box below as in second link 
### Remote commands
> To add use command `git remote add origin link-to-your-git-repo`

`git remote -v` command will show you your link to git remote (e.g. github.com), if you want to update it

> To Update url to origin
````
`git remote set-url origin new-url` will update url 
````
### commit and push
`git add .`

`git commit -m 'message'`

`git push origin name-of-branch`

### Branching commands

`git branch` command will list all the branches in your current project

`git checkout -b name-of-branch` will create new branch with name name-of-branch

`git checkout name-of-branch` will switch to branch name-of-branch

`git branch -M main` to change git name of git branch

### Delete branch commands

`git push --delete origin name-of-branch` this will delete branch from remote

`git branch -D name-of-branch` will delete branch from your local machine

### Synchronizing (update your local branch from remote)

`git fetch` (first to get changes from remote)

`git checkout main` if not on main or master already

`git pull origin main`

> before doing any of these check your commit is there in 
`git reflog --date=iso` if you see your change here you can always get it by command `git reset --hard "HEAD@{2022-10-30 10:19:07 +0000}"`

### reset 
`git reset --soft HEAD~3` this will keep change on your local branch

`git reset --hard HEAD~3` this will discard the changes of commit

### stash
`git stash` to park changes temporary 

`git stash apply` to get temporary changes from stash, but also keep it in stash list  

`git stash pop` to get temporary changes from stash, and delete it from the stash list 

### squash, amend 
`git rebase -i HEAD~4` will let you squash or amend changes in last 4 commits

In VI editor press `INSERT key to start editing` once edited press `ESCAPE` and at : enter wq to save or q to not save

