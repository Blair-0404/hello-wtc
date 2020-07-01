# hello-wtc

## 수업정리
* git init 하면 .git 이 생긴다. 하지만 .git은 local에 생기는 것 이다. 

### stage (로컬저장소와 원격저장소의 징검다리같은 공간이다.)
* git add : loacal의 변경사항을 stage에 올리는 행위
* git commit : commit 객체를 만들어낸다.(커밋은 내부적으로 트리가 있고 그 안에 오브젝트로 있다. = 트리객체이다)
    * commit 은 어떻게 하면 날라가나? git reset 만으로는 날아가지 않는다. commit은 작업에 대한 스냅샷과도 같아서 언제든 돌아갈 수도 있다.
        * 커밋하면 일단 로컬에는 무조건 남아있다. (=> git reflog로 작업했던 모든 커밋로그 볼 수 있다.)
    * commit 한 후에도 사실 stage에 그대로 있다. (하지만 이전 커밋객체?와는 다르다
    * 커밋생성->커밋객체 만들어짐(트리객체에 객체달려짐)
    * 커밋은 항상 부모 커밋이 있다.
    * 
* git은 항상 dif를 저장하지 않고 blob통체를 저장한다. 때문에 오히려 더 효율적 왜?
* echo ~ : 

### push vs pull(fetch + merge)
* push : 로컬 -> 원격
* fetch : 원격 -> 로걸
* pull : 원격 -> 로걸로  fetch + merge

### 공부할것 
* cat hello.txt (생성)
* git ls-files --stage 
* git log -n2 --online
* git log -n1 --graph (헤드 알려줌?)
* git cat-file -t 커밋번호
* git cat-file commit 커밋번호 (내용보여줌)
* 브랜치는 어떤 커밋의 참조일 뿐이다.( 어려움 )
* git hasn-object (파일명hello.txt?)
* git cat-file blob
* git add --all
* git log
* git reflog (작업했던 모든 커밋로그)
* git rebase master (마스터 위에 커밋이 생긴다?;)



* 깃에는 사실 커밋밖에 없고 나머지는 다 참조변수일뿐이다. 커밋은 내 컴퓨터에 항상 남아있다.


### rebase, cat, reset 추가공부해보기