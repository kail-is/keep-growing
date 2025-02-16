# 발표 대상

* mz 추구미
* 단축키를 능숙하게 활용 ㅋㅋ하고 싶은 사람

# Gilded Rose 미션 

* 황금장미여관 - 와우
* 의식적으로 연습하고 리팩터링 기술을 향상하는 미션
* [Github Repo](https://github.com/emilybache/GildedRose-Refactoring-Kata)
* 1만시간의 재발견 -> 목표 의식을 가지고 연습을 해야 늘어난다
  * 명확한 목적 / 컴포트존에서 벗어남 / 목표의식 

# 리팩터링 

* IO를 고정시킨 상태에서 내부 구현을 개선하는 것

# 라이브 코딩 .... ㅋㅋㅋ 

* [린트 라이브러리](https://github.com/JLLeitschuh/ktlint-gradle)


* [린트 라이브러리] -> Ktlint 라이브러리 (https://github.com/JLLeitschuh/ktlint-gradle)

* 컨트롤 시프트 아이 -> Command + Shift + I: 정의 빠르게 보기

* 컨트롤2번 -> Command + Command: Run Anything

* 오 ㅋ 컨트롤 G -> Command + G: 특정 라인으로 이동

* 다 닫고 하나씩 열 수 있다 -> Command + Shift + F12: 에디터 창 관리

* 오 대박 긁어서 새로운 펑션으로 전환 가능 -> Command + Option + M: 메소드 추출

* (item.name -> 확장함수로 바꿈) -> Option + Enter로 확장 함수로 변환

* f2를 누르면 고쳤으면 하는 곳으로 이동됨 -> F2: 다음 에러/경고로 이동

* 옵션 엔터를 통해 제안하는 대로 바꿈 -> Option + Enter: 코드 수정 제안

* 커맨드 f 1 -> 어차피 제로야 => 그냥 둠 -> Command + F1: 에러 설명 보기

* if문 1줄 사용 가능 -> 단일 라인 if문 작성 가능

* Ktlint로 수정할 때 돌려 보면 됨 -> Ktlint 실행으로 스타일 체크

* 옵션 엔터 알트 인서트 -> Option + Enter / Command + N

* 비슷한 모양으로 바꿔주면 일을 하기 시작햠 (when절 -> 예뻐짐) -> Option + Enter로 when 변환

* 인버트를 하면 원하는 코드가 나왔다? -> Command + Option + N: 인라인/조건 반전

* 스플릿 -> 인버트 -> -> 메소드 추출 후 조건 반전 (Command + Option + M 사용)

* false로 바꿈 -> 지워 -> Option + Enter로 불필요한 조건 제거

* 유사한 코드가 오른쪽에서 보인다 (노란색?) -> Option + Enter로 함수 추출 제안

* 함수 내에서 분기
  * 리프트: when-> if -> function -> when으로 바꾸기 -> Option + Enter로 순차 변환
  * 로직을 이해한 다음에 그에 따라 if문 만들고 -> 똑같이 바로위 반복

* 바깥의 if를 안으로 옮겨줄 수 있다 -> Option + Enter로 if 구문 최적화

---- 

## 자주 쓰는 단축키 모음

* Ctrl + Shift + I: Quick Definition 보기
* Ctrl + G: 특정 라인으로 이동
* F2: 다음 에러/경고로 이동
* Alt + Enter (Option + Enter): 코드 수정 제안
* Ctrl + F1 (Command + F1): 에러 설명 보기
* Alt + Insert: 새로운 코드 생성 메뉴


## 리팩토링 단축키

* 코드 선택 후 Ctrl + Alt + M: 새로운 메서드로 추출
* 코드 선택 후 Ctrl + Alt + V: 변수로 추출
* 코드 선택 후 Ctrl + Alt + F: 필드로 추출
---
* Shift + F6: 이름 한 번에 바꾸기
* Ctrl + Alt + L: 코드 포매팅
* Ctrl + Alt + O: 안 쓰는 import 정리


## 편집 단축키

* Ctrl + W: 코드 블록 선택 확장
* Ctrl + D: 라인 복제
* Ctrl + Y: 라인 삭제
* Ctrl + /: 라인 주석
* Ctrl + Shift + /: 블록 주석
