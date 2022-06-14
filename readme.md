# LocalStorage 를 이용한 메모기능 구현
- JS localStorage 를 이용한 메모기능 구현 과제 입니다
- 윈도우 스티커메모 기능을 참고했습니다
 
## 목표

- 각 기능을 구현 후 모듈형으로 바꿔보기
- 이벤트캡처링, 버블링에 익숙해지기
- 추가기능 구현하면서 git branch 익숙해지기, commit 메세지 명확하게 작성
- prettier 셋팅하고 사용해보기

## 사용

- Html + CSS + VanillaJS


## 메인기능
윈도우의 스티커메모의 기능과 동일하도록 구현
1. 추가, 삭제
2. 크기조절
3. bold, u, del, i 
4. Drag & Drop 위치조절
5. 각 메모끼리 곂칠 수 있도록 구현

## 추가기능

## 구현
### 1. 추가, 삭제 (06/09)
 - 첫 메모를 기준으로 작성해서 추가하는 메모마다 무작위의 ID를 부여해서 생성해주고
   그 아이디를 기준으로 로컬스토리지에 key 값으로 저장해서 갱신, 삭제를 쉽게 컨트롤 할 수 있게 구현

### 레이아웃

### 파일별 역활

## 개발 중 에러와 해결방법
- cloneNode 를 사용해 복사하면 이벤트리스너가 사라지는 문제점
- 각 메모에 개별 ID를 부여해 생성하면 어떨지 + class문법으로 구현가능할지
- **삭제할 때 처음 ID없는 메모가 삭제됨**
   -> editorSection 을 cloneNode를 이용해 복사해 memoSection 을 삽입하는 방식으로 구현 했는데 무작위로 생성된 ID를 setAttribute를 이용해 추가하는 과정에서 첫 메모에도 ID가 추가되는 현상때문에 ID가 있으면 삭제되도록 구현해놔서 첫 메모가 삭제처리 되고 첫메모와 마지막 생성된 메모의 ID가 같아지는 현상이 일어났습니다. cloneNode을 먼저 한 후에 childNode 를 이용해 복사한 노드의 .div-memo 태그에 ID를 추가해주게 고쳐서 해결
## 개발하면서 느낀점
- 필요한 기능과 흐름을 정확히 정하고 그리는 단계가 필요하다
    - 미리 그려놓지 않고 구현하면서 문제를 해결하니까 구현해갈수록 복잡해지고 삽질하는 시간만 늘어난다.


