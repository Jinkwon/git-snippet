# git-snippet
git snippet for general works

### fork 된 저장소에서 upstream 설정
```
$ git remote add --track master upstream git://github.com/upstreamname/projectname.git 
$ git fetch upstream
$ git merge upstream/master
```

### .gitignore 초기화
```
$ git rm -r --cached .
$ git add .
```

### Remote Branch 삭제
```
$ git branch -rd origin/REMOTE_BRANCH
OR
$ git push origin --delete REMOTE_BRANCH