# 코루틴 컴파일 과정 파헤치기

* [발표 자료](https://drive.google.com/file/d/1oYBGmua0jHNXZKOK402MuJvuWlgHISxg/view?usp=drive_link)
---
* suspend라는 비동기: Main 함수에서는 실행이 불가 (block되어야 하니까)
* 함수 만들기
suspend를 매개변수로 받아서 해당 함수를 실행시킴 -> 일반 함수에서도 호출 가ㅡ능! 
* resume -> 일시정지된 로직 재개

---

# State Machine 

* label -> 함수를 얼마나 호출하는지 확인하는 것 
* 0으로 초기화되어 있고 -> 돌 때마다 +1 
* SUSPENDED -> marker 
  * 본래 리턴 타입이 아니라 이 함수가 중단되었다는 걸 알림
* 람다가 반환해야 하는 Unit을 리턴하고 끝남 
---
* SUSPENDED가 중단된다면? -> `suspendedIt(this)`으로 중단
  * 최상위의 suspendded를 호출하면서 끝남
  * 라벨은 업데이트되어 있었음 바로 1로 가서 실행
* 예외는?
  * resume 한도를 넘겼을 때
* suspendedIt
  * return은 무조건 SUSPENDED나 returnType 중 하나를 반환해야 한다?
  * 코틀린은 UNION 타입을 지원하지 않음 
  * zzzzzz any  (ㅋ)

# Contious Passing Type

* resume() -> 코틀린에서 사용하는 반환 함수
  * invokeSuspended -> 상태 변환을 수행함 
* memberService는 어떻게 실행할까?
  * memberRepo가 링크를 지니고 있어야 함
  * -> memberSErvie를 memberRepo에 전달해야 함 
  * => invoke 한수 시그니처에 Contioun을 추가! (컨플리션) -> Any로 변했죠 
    * Contious Passing Style
* `suspendedIt(this)` -> 부모를 자식에게 주입하는 거 

# Local Var 

* 로컬 변수를 제어하는 법 
* 코루틴이 일시중단되면 해당 지역변수를 저장해야함 -> 그러지 않으면 변수가유실됨
* 중단이 발생하기 전에 벼수를 저장한 뒤 코루틴 재개 시 복원해야 함 
* 컴파일 함수
  * `this.L$0` -> 재개했을 때 다시 불러오기 위해 변수에 저장
  * null 할당을 통해 클리어 
---
* 로컬 변수가 여러 개라면 임시 저장 공간이 여러 개 생기나요?
  * `L$0` -> `L$1` -> `L$2` ... 겹치지 않도록 저장소를 늘림

# Suspend Function

* suspend가 붙은 람다로 이야기한 이유
  * 정적함수일 수도 있음
  * 클래스 내 함수가 여러 개 있을 수 있음
* THEN?
  * 모든 함수를 suspend 람다로 변환하여 사용하면 됨
* JVM은 왜 사용하지 않는가?
  * 스택 트레이스의 가독성 
  * `invokesuspende`가 반복되어 출력되는 게 아니라 함수 이름이 출력되도록
  * 함수 이름을 함수 내부에 상태 기계를 구현하는 반식으로 해결 

