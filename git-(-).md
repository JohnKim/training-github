# Git 사용하기 \(Remote\)

이제까지는 PC 의 Local Repository 에 커밋까지 한 상태 입니다. 이제 Remote Repository 인 Github 에 소스를 올리는 실습을 진행 합니다.

### 1. Github 에서 Repository 생성

![](/images/create-new-repository-1.png)

생성하는 repository명\(프로젝트 명\)은 `training-github` 으로 합니다.

![](/images/create-new-repository-2.png)

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
$ cd ..
```

### 4. 다른 개발자의 프로젝트 Fork 해서 내려받고 수정하기

옆사람의 Github 프로젝트에서 Fork 버튼을 눌러 자신의 Gitub 원격저장소로 복사합니다.

그리고 clone 명령으로 PC 에 내려받습니다.

```
$ git clone https://github.com/생성한계정/training-github-1.git
$ cd training-github-1
```

이제 파일 내용을 수정하여 커밋하고 push 하여 업로드 합니다.

```
$ vi hello-world.txt
내가 수정했다!

$ git commit -am 'update hello-world.txt'
$ git push
```

### 5. Pull Request 요청하기

Pull Request 란 다른 개발자의 프로젝트를 수정한 것을 반영하도록 요청하는 것입니다.

New pull request 버튼을 눌러 내용을 확인하고 Create pull request 버튼을 눌러 PR 을 요청합니다.

다른 개발자가 자신의 프로젝트의 파일을 수정한것을 pull request 내용을 보고 확인한 후 수락할 수 있습니다.

### 6. 변경된 소스 파일 다시 내려받기 \(pull\)

Github 원격 저장소에 있는 자신의 프로젝트가 Pull Request 를 수락하면서 변경되었을 것입니다.

이제 이 변경된 프로젝트를 자신의 PC 에 업데이트합니다.

```
$ cd training-github
$ git pull
$ cat hello-world
```

### 7. Desktop Github 프로그램 사용하기

[https://desktop.github.com/](https://desktop.github.com/) 에서 프로그램을 다운로드 받아 설치 합니다.

Github Desktop 은 지금까지의 실습 내용을 GUI 환경에서 할 수 있는 프로그램입니다.

기존의 clone 해서 내려받은 프로젝트 폴더를 Drag&Drop 하여 볼 수 있습니다.

또는 직접 Github Desktop 으로 clone 할 수 있습니다.

이런 좋은 프로그램이 있었는데 왜 고생을 한 것일까요? 억울해 하지 않습니다. 반드시 커멘트창에서 사용했던 명령어에 익숙해지고, 이 프로그램을 사용하도록 합니다.

> Github Desktop 뿐 아니라 SourceTree 라는 GUI 프로그램도 많이 사용합니다. \([https://www.sourcetreeapp.com](https://www.sourcetreeapp.com/\)\)\)

_이제 git 다 배운 건가요? 아닙니다. 다음주 그리고 그다음주 계속 실습하면서 계속 배울 예정입니다._

