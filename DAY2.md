# TIL Day 2



## 'Status'의 의미 

* 'w.d & s.a , s.a&commits' 두개의 차이를 본다

   * 만약에 s.a에서 파일을 지운다면?

     * w.d - s.a / s.a - commits 의 차이를 보고 문장이 나온다.

     * 이후 'git add . '를 입력하면 'no commits yet'이라는 문장이 나온다.
       (다 똑같기 때문.)

     > s.a의 위치 : .git 폴더에 있다.(숨김폴더)
     >
     >> 'git ls-files --stage' : Vscode에서 s.a 볼 수 있는 문장



## 'Staging Area'의 의미  

​	기존버전은 그대로 두고 수정사항들만을 새로운 버전으로 생성할 수 있도록 하는 공간.



## Git 사용 시 주의사항

1. 중첩 'git init' 금지 : 서브파일 안에 또 '.git'가 있는 경우 / home에 init 금지
2. '.git' 이 있는 폴더는 이동할 수 있다.



## .gitignore 

* Git으로 프로젝트를 관리할 때 필수적으로 필요한 것.

  1. README.md

  2. .gitignore
* gitignore으로 설정한 파일은 무시할 수 있다. 
* 이미 버전관리가 된 파일은 무시할 수 없다.
* 민감한 정보를 가지고 있는 파일들을 숨길 때 사용
* 처음 로컬 저장소를 만들때 README.md , .gitignore 먼저 만들고 'git init'  한다.
  * 한번 관리대상이 되면 이후에 .gitignore에 작성하더라도 계속 관리의 대상으로 인식한다.

* 제외하고싶은 파일들은 git add 전 반드시 .gitignore에 작성한다.
* [.gitignore 만들어주는 링크](https://www.toptal.com/developers/gitignore)



## Clone 

> 원격저장소 자체를 로컬 저장소로 가져오는 것.

'git clone' 명령어를 사용하면 원격 저장소를 통째로 복제해서 내 컴퓨터에 옮길 수 있다.

`git clone <원격 저장소 주소>` 의 형태로 작성

`git init`과 `git remote add`는 이미 수행되어있다.



## Pull

> 원격 저장소의 변경 사항을 가져와서, 로컬 저장소를 업데이트하는 명령어.

* 로컬 저장소와 원격 저장소의 내용이 완전 일치하다면 git pull을 해도 변화가 일어나지 않는다.
* `git pull <저장소 이름><브랜치 이름>` 의 형태로 작성한다.
* 항상 변경 사항을 로컬 저장소로 업데이트할때 'pull - add - commit - push' 기억하기

