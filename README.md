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



#### git ignore 작성법
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