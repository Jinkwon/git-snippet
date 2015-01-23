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
```

### REBASE 로 여럿이서 작업하기
```
$ git branch
* master
Already up-to-date.
$ git checkout -b feature
$ vim feature.js
$ git add .
$ git commit -am "[Feature] developed new feature1"
$ git commit -am "[Feature] developed new feature2"
$ git checkout master
$ git pull // sync latest code with master branch
$ git checkout feature
$ git rebase master
Applying .. 
$ git checkout master
$ git merge --no-ff -m "[Feature] developed feature"
$ git push
```
