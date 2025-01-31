# TIL (Today I Learned) - Day 9: 생성형 AI 활용 백엔드 데브코스

## 오늘의 학습 내용

## 1. AI를 활용한 코딩테스트 학습방법 및 프롬프팅

- AI를 활용해 문제 해결을 위한 접근법을 배우고, 적절한 프롬프팅을 활용하여 학습 속도를 높이는 방법 학습

#### 커리큘럼 만들기
```
나는 {언어와 프레임워크}로 {포지션}을 지망하는 {수준}의 개발자야.

나를 위한 자바스크립트 알고리즘 코딩테스트 대비를 위한 {일정}의 커리큘럼을 짜줘.

프로그래머스 사이트를 이용하여 Lv0, Lv1, Lv2 문제 활용해서 작성해주고 편의상 링크를 꼭 포함해줘.
```

#### 1단계 : 정확성

```bash
나는 {언어와 프레임워크}로 {포지션}을 지망하는 {수준}의 개발자야.

{문제를 제공}

나는 {문제를 푸는데 사용할 언어}로 이 문제를 풀거야. 다만, 너는 이 문제에 대한 코드를 마치 학습한 적이 없는 듯이 행동해줘.

내가 원하는 산출물은 직접적으로 입력된 코드가 아니라 한 줄씩 주석을 따라서 채우다보면 전반적인 구조를 채울 수 있게 되어 있는 가이드 구조야. syntax keyword와 block 관련 괄호와 indent만 적용되어 있고, 가이드하는 주석으로 1, 2, 3 번호를 달면서 채워나가도록 해줘. 맨 첫 줄에 이 문제에 필요한 자료구조와 풀이 방법을 유추할 수 있도록 유도하는 힌트로 구성된 주석을 달아줘

다만 효율성보다는 이해의 직관성을 더 우선시하고 할 수 있다면 가장 쉬운 방식으로 작성해가야해. 설명 단계라던가 그런게 짧을 수록 좋아. 차후 효율성을 위한 공부는 한 차례 더 할 거야.

마지막으로 산출된 코드에서 주석과 줄바꿈과 문법 키워드와 블록을 만들기 위한 표시를 제외하곤 모두 지워줘. 결과는 한글이어야 해.
```

#### 2단계 : 효율성

```bash
나는 {언어와 프레임워크}로 {포지션}을 지망하는 {수준}의 개발자야.

{문제를 제공}

나는 {문제를 푸는데 사용할 언어}로 이 문제를 풀거야. 다만, 너는 이 문제에 대한 코드를 마치 학습한 적이 없는 듯이 행동해줘.

나는 이미 문제 자체를 해결하는 것을 초점으로 한 번 문제를 푼 상태야. 이 문제를 언어, 자료구조, 최적화 기법 등을 활용하여 너무 특이하지 않은 방법으로 최대한의 시간적, 공간적 효율성을 높이는 방법을 알려주면서 가이드하는 주석으로 1, 2, 3 번호를 달면서 채워나가도록 해줘. 주석은 한글로 작성되어야 해.
```

## 2. JavaScript 함수

#### - 함수 선언

```javascript
function greet(name) {
  return `Hello, ${name}!`;
}
console.log(greet("Alice"));
```

#### - 함수 표현식

```javascript
const add = function (a, b) {
  return a + b;
};
console.log(add(2, 3));
```

#### - 기본 매개변수

```javascript
function multiply(a, b = 2) {
  return a * b;
}
console.log(multiply(3)); // 6
```

#### - 콜백 함수

```javascript
function process(callback) {
  console.log("Before callback");
  callback();
  console.log("After callback");
}
process(() => console.log("Inside callback"));
```

#### - 클로저

```javascript
function outerFunction(outerValue) {
  return function innerFunction(innerValue) {
    return outerValue + innerValue;
  };
}
const addFive = outerFunction(5);
console.log(addFive(3)); // 8
```

#### - 함수의 반환값

```javascript
function createMultiplier(multiplier) {
  return function (number) {
    return number * multiplier;
  };
}
const double = createMultiplier(2);
console.log(double(4)); // 8
```

## 3. 화살표 함수 심화

#### - 화살표 함수

```javascript
const square = (num) => num * num;
console.log(square(4)); // 16
```

#### - 여러 줄 본문과 this 바인딩 차이

```javascript
const obj = {
  value: 10,
  regularFunction: function () {
    console.log(this.value);
  },
  arrowFunction: () => {
    console.log(this.value);
  },
};
obj.regularFunction(); // 10
obj.arrowFunction(); // undefined (화살표 함수는 this를 바인딩하지 않음)
```

## 4. 고차 함수

#### - map

```javascript
const numbers = [1, 2, 3];
const squared = numbers.map((num) => num * num);
console.log(squared); // [1, 4, 9]
```

#### - filter

```javascript
const evens = numbers.filter((num) => num % 2 === 0);
console.log(evens); // [2]
```

#### - reduce 살짝 (고인물들의 장난감 같은 존재)

```javascript
const sumTotal = numbers.reduce((acc, num) => acc + num, 0);
console.log(sumTotal); // 6
```

#### - forEach 살짝 (이건 그냥 쓰지말라고 하셨음)
```javascript
numbers.forEach((num) => console.log(num));
```

## 5. 구조 분해 할당

#### - 배열

```javascript
const [first, second] = [10, 20];
console.log(first, second); // 10, 20
```

#### - 객체

```javascript
const person = { name: "Alice", age: 25 };
const { name, age } = person;
console.log(name, age); // Alice, 25
```

## 6. 스프레드 연산자

#### - 배열

```javascript
const arr1 = [1, 2, 3];
const arr2 = [...arr1, 4, 5];
console.log(arr2); // [1, 2, 3, 4, 5]
```

#### - 객체

```javascript
const obj1 = { a: 1, b: 2 };
const obj2 = { ...obj1, c: 3 };
console.log(obj2); // { a: 1, b: 2, c: 3 }
```

## 7. 나머지 매개변수

```javascript
function sum(...numbers) {
  return numbers.reduce((acc, num) => acc + num, 0);
}
console.log(sum(1, 2, 3, 4)); // 10
```

---

## 배운 점

- JavaScript 함수 문법을 빠르게 찍먹으로 학습함.
- 최신 JavaScript 문법과 잘 사용되지 않는 문법을 구분하며 배움.
- AI를 활용한 코딩 테스트 학습법이 특히 도움이 되었음.

## 느낀 점

- 코딩 테스트에서 어려운 문제를 풀 때 AI의 프롬프팅이 큰 도움이 될 것 같음.
- 함수 개념을 완벽히 이해하기에는 아직 부족함.
- Java 학습을 진행할 때 함수를 더욱 깊이 공부할 계획.

## 오늘의 난관

- 함수 개념이 다양하고 복잡하여 헷갈리는 부분이 많았음.
- 특히 화살표 함수와 this 바인딩 개념이 어려웠음.
- map, filter 같은 고차 함수의 동작 원리를 완전히 이해하는 데 시간이 걸림.

## 문제 해결 과정

- 여러 가지 예제 코드를 실습하며 함수의 동작을 직접 확인함.
- 기존의 함수 선언 방식과 화살표 함수의 차이를 비교하면서 this 바인딩 차이를 이해함.
- map, filter를 실습해 보면서 동작 원리를 익힘.
- AI를 활용하여 추가적인 예제를 찾아보고 분석함.

## 앞으로의 계획

- 코딩 테스트 문제를 레벨 순서대로 풀어보며 알고리즘 학습 강화.
- 함수 개념을 완전히 익히기 위해 AI와 함께 다양한 실습 진행.
- JavaScript의 최신 문법과 잘 쓰이지 않는 문법을 구별하면서 학습 지속.

---

_작성일: 2025-01-31_
