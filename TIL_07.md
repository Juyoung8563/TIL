# TIL (Today I Learned) - Day 7: 생성형 AI활용 백엔드 데브코스

# **오늘의 학습 내용**

---

```javascript
// 변수 선언
var x = 10; // 더 이상 사용 권장되지 않음
let y = 20; // 값 변경 가능
const z = 30; // 값 변경 불가

// 주석 사용
// 단일 줄 주석
/* 여러 줄
   주석 */

// console.log를 통한 출력
console.log("Hello, JavaScript!");

// 데이터 타입
let str = "문자열"; // string
let num = 123; // number
let isTrue = true; // boolean
let nothing = null; // null
let notDefined; // undefined
let obj = { key: "value" }; // object
let arr = [1, 2, 3]; // array

// 연산자
let sum = 10 + 5; // 15
let isEqual = 10 === "10"; // false (엄격 비교)
let isLooseEqual = 10 == "10"; // true (느슨한 비교)

// 삼항 연산자
let result = sum > 10 ? "크다" : "작다";

// 조건문
if (sum > 15) {
  console.log("15보다 큽니다");
} else if (sum === 15) {
  console.log("15입니다");
} else {
  console.log("15보다 작습니다");
}

// switch문
switch (sum) {
  case 10:
    console.log("10입니다");
    break;
  case 15:
    console.log("15입니다");
    break;
  default:
    console.log("다른 값입니다");
}

// 반복문
for (let i = 0; i < 5; i++) {
  console.log(i);
}

let i = 0;
while (i < 5) {
  console.log(i);
  i++;
}

for (const item of arr) {
  console.log(item);
}

for (const key in obj) {
  console.log(`${key}: ${obj[key]}`);
}
```

---

# **배운 점**

- 자바스크립트의 문법은 유연하면서도 간결하게 로직을 표현할 수 있도록 구성되어 있다.
- `const`와 `let`의 사용을 통해 변수의 변경 가능 여부를 명확히 구분할 수 있다는 점을 학습.
- 삼항 연산자는 짧고 간단하게 조건문을 처리하는 데 유용하지만, 가독성을 고려해 적절히 사용해야 함.
- `switch`문은 조건이 여러 개인 경우 깔끔하게 표현할 수 있어 가독성을 높이는 데 효과적이다.

---

# **느낀 점**

- 자바스크립트는 처음 접했지만, 문법이 Java보다 비교적 쉬워서 친숙하게 다가왔다.
- `node .`으로 결과를 즉각 확인할 수 있어 학습하는 데 흥미를 더해줌.
- 복잡한 데이터 타입과 조건문을 활용하면서, 작은 변화로 큰 결과를 만들어낼 수 있음을 깨달았다.
- Java처럼 `sout`같은 에밋이 없어서 아쉽...

---

# **오늘의 난관**

- `===`와 `==`의 차이점과 활용 방법이 헷갈렸다.
- `null`과 `undefined`의 차이가 헷갈렸다.

---

# **문제 해결 과정**

- `===`와 `==`의 차이를 직접 콘솔에서 실험하며 결과를 확인함.
  - `===`: 데이터 타입과 값이 모두 같은 경우 참
  - `==`: 데이터 타입이 달라도 값만 같으면 참
- `null`: 값이 비어있음을 의도적으로 나타냄
- `undefined`: 값이 정의되지 않음을 나타냄

---

# **앞으로의 계획**

- 자바스크립트의 고급 문법 (예: 함수, 클래스, 비동기 처리)에 대해 심화 학습.
- 간단한 프로젝트를 통해 오늘 배운 개념을 실습하며 정리.
- 매일 학습한 내용을 정리하며 점진적으로 발전된 결과물을 만들어갈 계획.

---

- _작성일 : 2025 - 01 - 24_
