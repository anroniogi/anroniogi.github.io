---
layout: article
title: Visual Studio로 Linux 코딩하기
categories: 개발환경
comments: true
image:
  teaser: 2018-03-12/visual_linux.png
---
> Visual Studio로 리눅스 프로그래밍을 해보자. 개쉬움

## Visual Studio 2017을 사용하는 리눅스 프로그래밍
#### 1. 준비사항
  - 리눅스 깔린 컴퓨터
  - Visual Studio 2017

#### VS2017 실행
  1. 리눅스 개발환경 설치 확인


![](/images/2018-03-12/ide_check1.png)

VS 2017에서 새 프로젝트 생성시 위의 사진과 같이 플랫폼 간-Linux 탭이 보이지 않는다면 아래의 ‘Visual Studio 설치 관리자 열기’를 클릭하여 필요한 개발도구들을 설치하도록 한다.
![](/images/2018-03-12/ide_check2.png)

워크로드 - C++을 사용한 Linux 개발 클릭

![](/images/2018-03-12/ide_check3.png)

개별 구성 요소를 클릭후 다음과 같이 설정하도록 한다.

---

#### 프로젝트 생성
설치가 완료되면, VS 우측 상단에 위치한 빠른실행 칸에 다음과 같이 ‘연결 관리자’를 입력 후 ‘플랫폼 간->연결 관리자’를 클릭한다.


![](/images/2018-03-12/setting1.png)



![](/images/2018-03-12/setting2.png)

다음과 같은 창이 뜨면, 추가를 누른 후, 연결하고자 하는 원격 시스템의 정보를 입력한다.

![](/images/2018-03-12/setting3.png)

VS2017에서 좌측 상단 탭 ‘파일-새로만들기-프로젝트‘를 클릭

Visual C++ - 플랫폼 간 – Linux를 클릭 후 빈 프로젝트를 선택, 프로젝트 이름을 입력한다.


연결이 되지 않는 경우에는 리눅스 PC 터미널에서 아래 명령어를 실행 후 다시 연결버튼을 누른다.
```sh
$ sudo apt-get install openssh-server g++ gdb gdbserver
```

---

#### 리눅스 프로젝트 생성
![](/images/2018-03-12/make_project1.png)

1. VS2017에서 좌측 상단 탭 ‘파일-새로만들기-프로젝트‘를 클릭
2. Visual C++ - 플랫폼 간 – Linux를 클릭 후 빈 프로젝트를 선택, 프로젝트 이름을 입력한다.


![](/images/2018-03-12/make_project2.png)

소스파일을 추가한 후 코드를 입력한다.

---

#### 실행, 리눅스에서 확인
![](/images/2018-03-12/make_project3.png)

빌드가 성공한다면, 상단의 탭중 ‘디버그-Linux콘솔’을 클릭한다.
![](/images/2018-03-12/make_project4.png)


![](/images/2018-03-12/make_project5.png)

빨간색 실행버튼을 누르면 실행이 된다.


![](/images/2018-03-12/check_on_linux1.png)

또한, VS에서 생성한 프로젝트가 Linux에도 생성되어 있는 것을 확인 할 수 있다.

![](/images/2018-03-12/check_on_linux2.png)
![](/images/2018-03-12/check_on_linux3.png)

생성된 파일의 경로는 VS2017의 ‘프로젝트-속성’에서 확인할 수 있다.

![](/images/2018-03-12/check_on_linux4.png)

리눅스에서도 동일하게 실행되는걸 확인할 수 있다.


>참조1 : https://docs.microsoft.com/ko-kr/cpp/linux/create-a-new-linux-project
>참조2 : http://blog.naver.com/PostView.nhn?blogId=tipsware&logNo=220991849234&categoryNo=52&parentCategoryNo=0&viewDate=&currentPage=1&postListTopCurrentPage=1&from=postView
