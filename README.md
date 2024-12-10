1. 엔티티 사용 ex. &lt; // 오류 발생 여지를 최소화 한다.

2. HTML, CSS 코드 정리 // 가독성 = 개발 생산성 향상이다.

3. Logic과 출력을 각각의 JS 파일로 분리 // 로직과 출력은 파일 단위로 분리하는 것이 좋다.

4. 버튼과 키보드 입력 기능을 JS에 구현 // 여러 이벤트를 하나의 동작으로 연결한다.

5. 로직 및 출력 구현
	- eval()라는 JS 내장 함수 사용할 경우
	 -> 직접 함수를 구현하는 것보다 매우 간편하지만, 보안 및 성능 이슈가 있다.
	 -> 정규표현식 /^[0-9+\-*/.]$/ 으로 문자열 입력값을 제한해줘야 보안 이슈가 없다.
	 -> "최신 JS 엔진에서 여러 코드 구조를 최적화하는 것과 달리 eval()은 JS 인터프리터를 사용해야 하기 때문에 다른 대안들보다 느립니다." 하지만, 매우 간단하다.
	 -> eval() JS 내장 함수에 대한 설명
        https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global_Objects/eval
	 -> 예외처리 = 정규 표현식으로 입력값을 제한한다, 연산자&소수점 중복 입력을 막는다, =을 눌렀을 때 입력값이 false인지 확인한다, 연산자&소수점으로 끝날 때 = 입력을 막는다, 소수점은 하나만 허용한다.

6. 예외 처리

7. - 테스트 케이스 딱 하나 작성하기.
    - 사칙연산 우선순위가 잘 나오는지 확인하기.
    - 2 + 3 x 4 / 2 = 8 이거 딱 하나만 테스트 코드에 넣어주세요.

8. 리팩토링

cf. import/export를 사용할 때 package.json에 "type": "module",을 버전 밑에 추가해줬다.
Node.js 환경에서는 이렇게 설정 해줘야한다.
원래 브라우저 환경에서는 없어도 실행되는게 정상이지만
go live를 쓸 때는 필요하더라
cf. formula.textContent = "2" // 포뮬러 HTML에 2값을 반영한다.
cf. const value = button.dataset.value; // data-value 값을 가져온다.
cf. data-value 값은 DOM 표준 속성으로 dataset 객체에 저장됨
cf. if-else를 사용하기 보다는, if와 얼리 리턴을 사용하는 것이 가독성 좋다.