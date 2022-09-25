# 오픈소스소프트웨어
## Week 1-1, 강의개요
* 강의계획서  
[강의계획서 바로가기!!](http://www.naver.com)
* 수업주의사항
    > 1. 강의 시작 전, 동영상 시청해오기  
    > 2. 출석은 간단한 퀴즈를 통해 진행할 예정  
    > 3. 수업은 질문, 요약정리, 실습으로 이루어짐  
***
## Week 1-2 , 오픈소스소프트웨어 개요
1. **오픈소스소프트웨어란?**
    * 소프트웨어 저작권 소유자가 모든 사람에게 소스코드를 게시, 사용, 복사, 수정 및 배포할 _권리_를 부여한 소프트웨어
2. **OSS 특징(_상용화 관점_)**
    - 일괄 사전 이용 허락 -> 직접 연락해 허락을 구하지 않아도 된다.
    - 로열티 없음
    - 소스 코드 제공
    - 복제, 배포, 수정 허용
    - 기간과 목적에 있어 제한이 없음
    - 지적 재산권의 보호를 받음 **상업용 OSS와의 공통점**
3. **OSS 특징 (_철학적 관점_)**
    - Free Software, _Richard Stallman_ **지금의 OSS**
        > copyleft (No SW Patent, NO DRM)  
            * 프로그램을 실행 할수있는 자유  
            * 프로그램의 작동원리를 연구하고 이를 자신의 필요에 맞게 변경시킬수 있는 자유  
            * 이웃을 돕기 위해서 프로그램을 복제하고 배포할수있는 자유  
            * 프로그램을 향상시키고 이를 공동체 전체의 이익을 위해서 다시 환원시킬수있는 자유  
    - Open Source Software
        > 상용 SW 까지 인정해주자! 코드를 공개하지만 독점하는 방식  
4. **OSS License**
    * 오픈소스 소프트웨어의 사용, 복제, 수정, 배포 권한의 범위를 지정  
5. **OSS License의 종류**
    * GPL
    * LGPL
    * MIT License
    * BSD License
    * Apache License
    * MPL
    * 라이센스종류이미지
    ![라이센스종류](https://www.e4ds.com/news_photo/FKZLRCJFW5OIDNJ9L1H9.JPG)
***
## Week 2-1 , 버전 관리 개요
1. **Version Control System (VCS)**
    - 이전의 작업 버전으로 쉽게 돌아가기 위해서 파일을 추적하는 시스템
2. **VCS의 종류**
    - CVS (Concurrent Version System)
    - SVN (Subversion)
    - Mercurial
    - Darcs
    - Git
3. **VCS의 유형**
    - **Centralized VCS, 중앙집중형**
        > 하나의 레포에 많은 사용자가 붙어서 개발
    - **Decentralized (Distributed) VCS, 분산형**
        > 로컬이 따로 있고, 원격레포가 존재하는 방식
4. **VCS의 기능**
    - **Check in/Commit**
        > 파일을 확인하고 수정하는 것 즉, 작업하던 것을 저장소에 넣는 것  
    - **Checkout and Edit / Fetch**
        > 저장소에서 파일을 수정하고 꺼내오는것   
    - **Diffs**
        > 버전간의 차이를 살피는 것  
    - **Branching**
        > 한 파일에서 여러가지 기능을 나눠서 개발하는 것  
    - **Merging**
        > 나눠서 개발 하던걸 합치는 행위 / 개발자의 개입이 가장 많이 들어가는 부분
    - **Conflicts**
        > merge 할때, 생기는 충돌들이 어디서 일어났는지까지 알려준다.
    - **Tagging**
        > 각 버전에 이름을 붙이는 것
***
## Week 2-2 , Git
1. **GIT의 관리영역 (4가지)**
    - **Workspace**
        > 작업하고 있는 파일들이 있는 곳
    - **Index(stage)**
        > 다음 커밋으로 고려되는 파일들이 있는 곳
    - **Local Repository**
        > 로컬 저장소로 커밋되어진 파일들이 있는 곳
    - **Remote Repositoy**
        > 원격 저장소로 푸시된 파일들이 있는 곳
    - **Summary Image**
    ![4가지 관리영역](https://blog.kakaocdn.net/dn/NENjI/btqwdBBI1Pb/KK3vzraKzl1WVg7JqSe8CK/img.png)
2. **GIT Workflow**
    - _git add (파일이름)_
    - _git commit -m "커밋메시지"_
    - _git push origin master_
        > master branch에 origin을 밀어넣는다는 코드
    - _git commit --amend_
        > 가장 마지막 커밋을 수정하는 코드
    - _git reset HEAD~1_
        > 가장 최근 커밋을 지우는 코드  
3. **GIT 상태확인 방법**
    - _git show_
    - _git log_
    - _git shortlog_
    - _git diff_
    - _git status_
***
## Week 2-3, Github/Fork/PullRequest
1. **Github**
    - 분산형 관리시스템인 git에서 원격저장소를 이르는 말
2. **Fork**
    - 타인의 원격저장소에서 코드를 가져오는 행위
3. **PullRequest**
    - 타인의 원격저장소에 내가 만든 commit을 제출한다는 의미
4. **Overall Workflow**
    - _git clone <<url>url>_
    - _git commit -m "커밋메시지"_
    - _git push origin master_
5. **Fork이후에도 버전 업데이트 하는 방법**
    - _git fetch (원격저장소이름)_
    - _git diff pb/master_
    - _git merge pb/master_
    - _git commit -a -m "커밋메시지"_
    - _git push origin master_
***
## Week 3, Markdown
1. **Markdown Language?**
    - 간단한 텍스트 편집기를 사용하여 포맷된 텍스트를 작성할때 쓰는 가벼운 마크업언어
2. **Markdown Language Grammer**
    - 기울임꼴
        > 기울임체로 쓰고싶은 단어를 _로 감싸준다.
    - 볼드체
        > 볼드체로 쓰고싶은 단어를 **로 감싸준다.
    - 헤더
        > #의 개수로 크기를 다르게 만들수있다.
    - 링크
        > 링크 텍스트는 [ ]으로 감싸주고, 이어 링크는 ( )로 감싸준다.
    - 이미지
        > !로 시작하고 대체텍스트는 [ ]로 감싸준후, 링크는 ( )로 감싸준다.
    - 인용구
        > 꺽쇠괄호로 시작하면 된다.
    - 글머리 기호
        > *로 시작하면 된다.
    - 문단구분
        > 문장뒤에 띄어쓰기를 두칸 넣어준다.
***
#### Edited by _전남대학교 215430 오다영_