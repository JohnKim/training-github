# Git 사용하기 \(Remote\)

이제까지는 PC 의 Local Repository 에 커밋까지 한 상태 입니다. 이제 Remote Repository 인 Github 에 소스를 올리는 실습을 진행 합니다.

### 1. Github 에서 Repository 생성.

### 2. Github 원격 저장소에 올리기 \(push\)

동일한 프로젝트 디렉토리에서 원격 저장소를 origin 에 추가 합니다.

```
$ git remote add origin https://github.com/생성한계정/training-github.git
```

그리고, 지금까지 Local Repository 에 커밋했던 모든 파일을 origin 의 master 에 업로드 합니다.

```
$ git push origin master
```

이제 Github 웹사이트를 통해 커밋 이력과 현재 저장된 파일들을 확인합니다.

### 3. Github 에서 프로젝트 내려받기 \(clone\)

지금까지 작업한 프로젝트 디렉토리를 삭제 합니다.

```
$ cd ..
$ rm -rf training-github
$ ls -al
```

이제 Github 원격 저장소로부터 프로젝트를 PC 에 내려받습니다.

```
$ git clone https://github.com/생성한계정/training-github.git
$ cd training-github
$ ls -al
```



