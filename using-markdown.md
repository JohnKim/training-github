# Markdown 사용하기

Markdown 은 일종의 마크업 언어로 텍스트에 태그를 이용해서 글자를 굵게하거나, 이미지를 삽입하거나 하는 일이 가능합니다. 또한 Markdown 파일안에 HTML 코드도 넣을 수 있습니다. 최근에는 다양한 블로그 시스템에서 Markdown 문법을 지원하고 있습니다.

Markdown 문법으로 문서를 작성하기 위해서는 웹서비스로 제공되는 온라인 Markdown 에디터나 Desktop 용 프로그램을 활용할 수도 있습니다.

* Desktop 용 프로그램 [https://typora.io](https://typora.io)
* 온라인 에디터 [https://stackedit.io](https://stackedit.io)

Github 의 README.md 파일은 Github 리파지토리를 열었을 때 가장 먼저 보이는 대표 문서 파일로, Markdown 문법으로 작성하도록 되어 있습니다. 주로 Github 리파지토리의 프로젝트 설명이나, 개발 및 실행 가이드가 작성됩니다. Github 에서 제공하고 있는 Markdown 문법 가이드를 통해 어렵지 않게 익힐 수 있습니다.

* [https://guides.github.com/features/mastering-markdown/](https://guides.github.com/features/mastering-markdown/)

본 실습 강의 자료 역시 Markdown 으로 작성되었고, GitBook \([https://www.gitbook.com\](https://www.gitbook.com\)\) 을 통해 온라인 및 다양한 포멧의 파일로 출판되도록 하였습니다.

* https://github.com/JohnKim/training-github



### 1. 새로운 프로젝트 repository 생성하기

Github 에서 새로운 Repository 를 생성합니다.

생성할 때 `Initialize this repository with a README` 를 선택하면 Repository 생성된과 동시에 README.md 파일이 생성됩니다.

프로젝트 명은 resume 로 합니다.

![](/images/create-resume-repo.png)

생성 한 후 Settings 메뉴를 클릭하여 Github Page 설정을 활성화 합니다.

![](/images/edit-github-page-setting.png)

master branch 를 선택한 후 저장한 후 아래와 같은 URL 로 접속하면 README.md 로 작성한 파일을 웹사이로 볼 수 있습니다.

[https://johnkim.github.io/resume/](https://johnkim.github.io/resume/)

### 2. resume 프로젝트 clone 하기

resume 프로젝트 Repository 를 clone 명령으로  PC 에 내려받아 Markdown 문법으로 간단한 자기소개서를 작성해 보도록 합니다.

```
$ git clone https://github.com/JohnKim/resume.git
$ cd resume
$ vi README.md
이것은 과제입니다.
```



