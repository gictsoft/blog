---
title:  "Git Study"
published: true
permalink: git.html
summary: "git study material"
tags: [news, getting_started]
---

## Git 이란?

Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency. (출처 : https://git-scm.com/)
* 버전관리 시스템 - 효율적인 협업과 버전관리

### 1. 버전관리 <= 형상관리

* 소스코드 관리 + 개발 환경, 빌드, 기타...


### 3. 버전관리툴

* CVS : check out / in 을 이용한 버전관리
* SVN : CVS와 높은 호환성, 대체 시스템
* GIT : 우리가 배울 툴

##Git Basic

### 1. 위치에 따른 기본 개념

 * Remote repository : server
 * Local repository : local
	

### 2. 상태에 따른 기본 개념

 * untracked
 * working directoy : modified
 * steaging area : staged
 * git directory : commited
	
### 3. Basic Process

 * Clone
 * Pull
 * Add
 * Commit
 * Push
 * Checkout

```
 위치와 상태에 따른 기본개념을 확실이 하는것이 중요
```
	
### 4. 기초 연습(command prompt & github)
   
 * git을 사용하는 다양한 방법
   - command prompt
   - GUI tool : tortoisegit, gerrit, msysgit, sourceTree, gitX....
   - 각 프레임워크 개발 도구를 이용 : eclipse......
   - remote repository 연동 software : github, gitlab.....

```
기본인 command prompt 에서 명령어로 실행시킬 수 있으면 어디서든 가능하단 말이오~~~~!!
```

 * git init
 * git status / git log
 * git clone
 * git add
   - git add <file name>
   - git add . {or (*.txt) , (*.*)} 
 * git commit
   - git commit -m <commit message>
   - git commit -v
   - git commit --amend
 * git rm
   - 파일삭제, local modify단에서 삭제하고 staged 시키는 명령어
   - git rm --cached <file name> : modify 삭제, local에 남김(.gitignore) 
 * git checkout
   - 파일 이전 상태로 돌림, modified → untracked
   - git checkout -- <file name> 
 * git reset
   - staged or commited → modified
   - git reset HEAD <file name> (HEAD^ or HEAD~2)

### 5. remote repository
 
 * git clone <url>
 * git remote
   - 원격 저장소 연동 : git remote add <remote repository name> <url>
   - git remote -v // show <remote repository name>
   - git remote rename <before name> < after name>
   - git remote rm <remote repository name>
 * git push // fetch
   - git push <remote repository name> <branch name>
   - git fetch <branch name>

## Git Branch

### 1. git branch

 * 가지치기(냇물파기) : 독립된 저장 공간을 생성한다. 
 * git branch <branch name>
 * git branch -d <branch name>

### 2. git checkout <branch name> : branch 이동

### 3. git merge <branch name>

### 4. git reset --hard <remote name>/<branch name>

## Git flow 전략

### 1. branch 관리 전략중 하나.

 * master : 최종 릴리즈한 안정화 버전
 * develop : 개발 버전
 * feature : 기능 개발 버전
 * release : release 점검을 위한 branch
 * hotfix : 버그 수정 branch
 * support : 호환성 문제 처리를 위한 branch

## 참고 사이트

 * 깃 홈페이지 (https://git-scm.com)
 * 깃 명령어 배워보기 (http://webclub.tisoty.com/317)
 * TMON의 개발이야기 (http://blog.naver.com/PostView.nhn?blogId=tmondev&logNo=220759303637)

{% include links.html %}