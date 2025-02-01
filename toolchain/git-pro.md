### config
`git config --global user.name "Spectrumzero"`
`git config --global user.email lmhspecter@gmail.com`
`git config --global core.editor nvim`
`git config --global alias.co checkout`
`git config --global alias.br branch`
`git config --global alias.ci commit`
`git config --global alias.st status`
`git config --list`

### status
`git status`
`git status -s`

### diff
`git diff`
`git diff --staged`
`git commit -a -m "skip git add"`

### commit
`git commit`
`git commit -m "this is the commit information`
`git commit --amend`
`git commit -a -m "skip git add"`


### clone
`git clone https://github.com/spectrumzero/webdevDemos.git -b quiz-app`
### rm
`rm PROJECTS.md`
`git rm PROJECTS.md`
`git rm --cached README.md`

### mv
`git mv file_from file_to`



### undo
`git commit --amend`
`git restore --staged test.md `
`git restore rakefile`

### ignore
```gitignore
# no .a files
*.a

# but do track lib.a, even though you're ignoring .a files above
!lib.a

# only ignore the TODO file in the current directory, not subdir/TODO
/TODO

# ignore all files in the build/ directory
build/

# ignore doc/notes.txt, but not doc/server/arch.txt
doc/*.txt

# ignore all .pdf files in the doc/ directory
doc/**/*.pdf
```


### branch
`git branch testing`
`git checkout testing`
`git checkout -b testing`
`git merge hotfix`
`git branch -d hotfix`

`git branch`
`git branch -v`
`git branch -vv`
`git branch --no-merged`
`git branch --merged`
`git branch -D nomerged`

`git checkout --track neworigin/master`
`git checkout -b tic neworigin/master`
`git branch -u origin/master`


### remote
`git remote`
`git remote -v`
`git remote add newremote https://github.com/paulboone/ticgit.git`
`git remote show`
`git remote show newremote`
`git remote rename newremote neworigin`

#### fetch
`git fetch newremote`
`git fetch --all`

#### merge
`git merge hotfix`
`git merge origin/master`
`git checkout -b tic neworigin/master`

#### push
`git push origin serverfix:awesomebranch`
`git push origin --delete awesomebranch`
`git push origin main --set-upsteam`
`git push origin HEAD~1:main --force`

### rebase
`gir rebase -i HEAD~3`
`git rebase --continue`
`git rebase --abort`

### reset
`git reset --soft HEAD~`
`git reset --mixed HEAD~`
`git reset --hard HEAD~`


### log
`git log`
`git log -p -2`
`git log -stat`
`git log --graph`
`git log --pretty=oneline`

### reflog
`git reflog`

### show
`git show 97be5d2`
`git show master`
`git show HEAD@{1}`
`git show HEAD@{yesterday}`
`git show HEAD^`
`git show HEAD^0`
`git show HEAD~0`

### tag
`git tag`
`git tag -l 'v1.8.5*'`
`git tag -a v1.0 -m "version 1.0"`
`git tag v1.0-lw`
`git tag -a v1.1 9fceb02`
`git push origin v0.1`
`git push origin --tags`

### [source download](https://github.com/spectrumzero/markedBooks/blob/main/gitpro.pdf)




