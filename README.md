# Git workflow & basics 
> Wunderkraut BE - 14/05/2013

## commands

listing of commonly used commands

### git clone

#### » git clone repo
> clone a repo from the server to local machine

`git clone git@github.com:Krimson/git-workflow.git`

#### » git clone branch
> clone a specific branch from the server to a local machine

`git clone --branch <branch> git@github.com:Krimson/git-workflow.git`

### git branches
> mind the caps, BRANCH ≠ branch

#### » checkout an existing branch to work on
`git checkout <branch>`

#### » list git branches

##### » list local branches

`git branch` _or_ `git show-branch`

##### » list remote branches

`git branch -a` _or_ `git show-branch -a`

##### » Show branch info in the CLI

- Simple
  `git log --all --graph --decorate --oneline --simplify-by-decoration`
- Eleborate
  `git show-branch --all`

#### » create a branch to work on

`git branch <branchname>`

#### » git branch from commit

`git branch <branch> <commit>`

#### » remove local branch

`git branch -d <branch>`

#### » cleanup obsolete remote branches

`git push origin --delete <branch>`

### merge

#### merge <branch B> into <branch A>

`git checkout <branch A>`
`git merge <branch B>`

#### merge <branch B> into <branch A> without fast-forward and without commit (safe option)

`git checkout <branch A>`
`git merge --no-commit --no-ff <branch B>`

### git status

#### get status of repo

`git status`

#### status of repo with hint to unstage files

`git status -s`

### add changes
> unlike SVN, you need to push changes to the remote server after adding & commiting them. Commit a lot, push a less.

#### » add file

`git add /foo/bar`

#### » add folder

`git add foo`

### commit changes

`git commit -m "my commit message"`

#### » commit all tracked files
> automatically stage all tracked, modified files before the commit

`git commit -a -m "my commit message"`

### reset changes

`git reset`

#### » reset soft
> undo the last commit and put the files back onto the stage

`git reset --soft HEAD~`

#### » reset hard
> undo the last commit, unstage files AND undo any changes in the working directory

`git reset --hard HEAD`

### revert changes

#### » revert changes to file

`git checkout /foo/bar`

#### » revert commit

`git revert <commit>`

#### » git revert all changes

`git checkout .`

### file actions, git style

#### » rename file or folder with git

`git mv foo bar`

#### » remove file with git

`git rm foo`

#### » remove folder with git

`git rm -r foo`

### git stash
> save changes made in the current index and working directory for later

#### » save changes and return to last commit

`git stash`

#### » list stashed stuff

`git stash list`

#### » get your stashed changes back

`git stash apply`

#### » remove stashed stuff

`git stash drop`

### git push

#### » git push all branches
> push all branches to the origin server
`git push --all origin`

#### » git push <branch>
> push a specific branch to the origin server

`git push origin <branch>`

## misc stuff

conflict & script-y stuff

### handling conflicts

just do it!


#### remove deleted tracked files

`git rm $(git ls-files --deleted)`

## bonus

Some additional information on config, best practices, resources etc.

### config

manage sensible defaults & tweaks in `~/.gitconfig`

#### » color example

`diff = auto`
`status = auto`
`branch = auto`
`interactive = auto`
`ui = auto`

#### » color "diff" example

`meta = yellow bold`
`frag = magenta`
`plain = white bold`
`old = red bold`
`new = green bold`
`commit = yellow bold`
`func = green dim`

#### » color "status" example

`added = yellow`
`changed = green`
`untracked = cyan`

#### » core example

`excludesfile = /Users/sjugge/.gitignore`

#### » push example

`default = current`

### gitignore

manage global and user specific .gitignore rules on your machine in `~/.gitignore`

#### » example

`# OS specific files`
`*.DS_Store`
`*.Spotlight-V100`
`*.Trashes`
`# app specific files`
`*bbprojectd`
`*nbproject`
`*.sublime*`

### resources

- official homepage: [http://git-scm.com/]
- official documentation: [http://git-scm.com/documentation]
- git pro book online: [http://git-scm.com]
- git reference site: [http://gitref.org]
- learn git online with GitHub Code School: [http://try.github.io]
