# Git 사용하기 \(Local\)

Github 은 원격 소스 저장소 중에 하나 입니다. 본인이 작업한 소스 파일을 Github 에 업로드하기 전에, PC 에서 프로젝트 폴더를 만들고, 파일을 생성해 커밋하는 부분 까지 실습 합니다.

### 1. Git 개발자 설정하기

개발자 이메일을 설정합니다. 나중에 원격 저장소인 Github 에 업로드 하기 위하여  Github 가입했던 이메일 주소로 설정합니다.

```bash
$ git config user.email “yohany@gmail.com”
```

개발자 이름을 설정합니다. Github 의 ID 이어도 되고, 실제 이름을 작성하여도 됩니다. 나중에 다른 개발자가 소스 수정된 이력을 볼때 노출되는 이름입니다.

```bash
$ git config user.name “John Kim”
```

> 만약 이미 Git 이 설정되어 있는 PC 라면 기존의 설정 정보를 삭제하도록 아래와 같은 명령어를 실행합니다.
>
> `git config --global --unset credential.helper`
>
> `git config --global --unset credential.helper`

> 만약 `git config` 명령 실행시 `fatal: not in a git directory` 에러가 나는 경우라면, 아래 2.프로젝트초기화 부터 하고, `git config` 를 실행합니다.

### 2. 프로젝트 초기화

프로젝트를 시작하기 위하여 프로젝트 디렉토리를 생성하고, git 명령어로 초기화 합니다. 초기화라고 하는 것은 초기화한 디렉코리가 git 으로 관리되도록 하기 위함입니다.

training-github 이라는 이름으로 폴더를 만듭니다. \(이 프로젝트 명은 training-github 입니다.\)

```
$ mkdir training-github
$ cd training-github
$ pwd
```

프로젝트 디렉토리에서 git 초기화를 실행합니다.

```
$ git init
$ ls -al
```

### 3. 첫번째 Commit !

파일을 하나 생성하고 작성한 후 add 한 후 commit 하는 과정을 진행합니다.

처음 생성할 파일명은 README.md 입니다\(대문자 파일명에 확장자는 .md\). 파일을 생성하고 아무 문장이나 작성하여 저장합니다.

```
$ vi README.md
안녕~ 오늘은 GITHUB을 배워보는거다!
```

vi 편집기를 사용하여 만들어도 되고, 이전에 설치한 Atom 에디터를 사용해서 생성해도 됩니다. vi 를 사용할 수 있다면, 가급적 vi 를 사용하는 것이 좋겠습니다.

파일을 생성한 후 add 명령으로 Staging Area 단계로 추가합니다.

```
$ git add README.md
```

이제 commit 명령으로 Local Repository 에 커밋합니다.

```
$ git commit -m "first commit!"
```

### 4. 상태를 확인하면서 두번째 Commit !

이번에는 새로운 파일을 생성하고 add 후 commit 하면서, 중간 중간에 현재 상태를 확인해 봅니다.

먼저 현재 상태를 확인합니다.

```
$ git status
```

파일을 하나 더 생성하고 add 합니다. \(역시 Atom 에디터를 사용해도 됩니다.\)

```
$ vi hello-world.txt
세상아 안녕!
$ git add hello-world.txt
```

그리고 다시 확인해서 add 명령으로 Staging Area 단계로 추가된 것을 확인할 수 있습니다.

```
$ git status
```

이제 commit 명령으로 Local Repository 에 커밋하고, 커밋된 상태를 확인합니다.

```
$ git commit -m "second commit!"
```

### 5. 기존 파일 수정하여 세번째 Commit !

먼저 현재 상태를 확인합니다.

```
$ git status
```

기존의 README.md 파일을 수정하도록 합니다.

```
$ vi README.md
난 개발이 정말 재미 있다!!
```

수정된 파일\(들\)을 이전 상태와 비교 할 수 있습니다.

```
$ git diff
```

수정된 파일\(들\)을 commit 합니다.

```
$ git add README.md
$ git commit -m 'update README.md'
```

지금까지 커밋된 내용을 확인해 봅니다.

```
$ git log
```

### 6. 간편하게 네번째 Commit !

새로 파일을 만들어서 실습해 봅니다.

```
$ vi test.txt
테스트!!

$ git commit -am 'create test.txt file'
$ git shortlog
```

-am 은 알아서 add 하고 메시지를 입력한다는 의미 입니다.

shortlog 는 커밋된 파일이 많은 경우 간단하게 확인하려고 할때 자주 사용합니다.

