# Learning_GitHub

```
git clone https://github.com/originalkyu/Learning_GitHub.git

git add .
git commit -m "fitst commit"
git push origin main
```

## 이용할 git, linux 명령어 모음
### 리눅스 명령어
```
apt remove git : 깃을 제거하는 명령어
apt install git : 깃을 설치

ls -a
touch a.txt
cat a.txt
```
#### 권한
```
chmod 777 파일
```


### git 명령어
#### help
```
git help
git help commit
```

#### version
```
git —-version
```

#### git config 설정
```
git config 설정값

git config --unset --global user.name
git config --unset --global user.email

git config --global user.name “사용자이름”
git config —-global user.email “이메일주소”
```
#### 현재유저 및 config 확인
```
git config --list 
or
git config -l

code .git/config
```

#### stage 및 add,commit 확인
```
git status
git ls-files --stage
git log
```

#### git clone
```
git clone 원격URL
git clone 원격URL 새폴더 이름 // 현재 파일 뿐 아니라 history를 모두 가져옴
```

## 협업하기 1 : 기본 방법
* local의 main branch는 push와 pull 용도로만 사용한다
* service1, service2 branch가 있음을 가정함
```
A 작업자
git branch service1
git checkout service1

작업, add, commit, push 가 이뤄짐
git push origin service1

git checkout main
git merge service1
git push origin main

B 작업자가 최신 버전을 자신의 branch에 반영함
git pull origin main
git checkout service2
git merge main
```

## 협업하기 2 : Pull Request 이용하기
* local의 main branch는 push와 pull 용도로만 사용한다
* service1, service2 branch가 있음을 가정함
```
A 작업자
git branch service1
git checkout service1

작업, add, commit, push 가 이뤄짐
git push origin service1

git checkout main
git merge service1
git push origin main

B 작업자가 최신 버전을 자신의 branch에 반영함
git pull origin main
git checkout service2
git merge main
```

## 협업하기 3 : 여러 개의 push가 이뤄졌을 때 이전 버전으로 돌아가는 법

## 협업하기 4 : 두 명이 하나의 파일을 동시에 수정하여 충동이 발생했을 때


#### reset과 revert

## git ignore 작성법
```
# a.txt 제외
a.txt

# .obj 파일 제외
*.obj

# b.txt는 제외하지 않음
b.txt

# 현재 디렉터리의 c.txt 무시
/c.txt

# /pub/ 디렉터리 안 모두 무시
/pub/

# doc 디렉터리 아래의 모든 .txt 무시
```

3.14 화
### 나의 리포지토리에 다른 사람이 push 할 수 있을까?

3.15 수
### 충돌이 일어났을 때 어떻게 대처할 수 있을까?
- git pull 하기 전에 최신버전에서 수정된 파일을 수정한 경우

git reset
git stash
