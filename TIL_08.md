# TIL (Today I Learned) - Day 8: 생성형 AI 활용 백엔드 데브코스

# 오늘의 학습 내용
오늘은 **자바스크립트의 객체와 클래스**에 대해 학습했습니다. 주요 학습 내용은 다음과 같습니다:

- **객체 리터럴과 프로퍼티**: 객체를 선언하고 데이터를 구조화하는 방법.
- **함수와 메서드**: 객체 내부에서 동작을 정의하는 방법.
- **클래스의 생성자와 메서드**: 클래스를 사용해 객체를 생성하고 동작을 추가하는 방법.
- **클래스 상속**: 상속을 통해 코드의 재사용성을 높이는 방법.

# 배운 점

### 1. 객체 리터럴과 프로퍼티
- 객체 리터럴은 데이터를 구조화하고 관리하기 쉽게 만들어 줍니다.
- 프로퍼티는 키-값 쌍으로 구성되며, 객체는 동적으로 프로퍼티를 추가하거나 삭제할 수 있습니다.

#### 예제 코드:
```javascript
const person = {
  name: 'Alice',
  age: 25,
  greet() {
    console.log(`Hello, my name is ${this.name}.`);
  }
};

console.log(person.name); // 'Alice'
person.greet(); // 'Hello, my name is Alice.'
```

### 2. 함수와 메서드
- 객체 내부에서 정의된 함수는 메서드라고 합니다.
- `this` 키워드는 해당 메서드를 호출한 객체를 참조합니다.

#### 예제 코드:
```javascript
const calculator = {
  add(a, b) {
    return a + b;
  },
  subtract(a, b) {
    return a - b;
  }
};

console.log(calculator.add(5, 3)); // 8
console.log(calculator.subtract(5, 3)); // 2
```

### 3. 클래스의 생성자와 메서드
- 클래스는 객체를 생성하는 템플릿 역할을 합니다.
- 생성자는 객체를 생성할 때 초기값을 설정하는 데 사용됩니다.

#### 예제 코드:
```javascript
class Animal {
  constructor(name, sound) {
    this.name = name;
    this.sound = sound;
  }

  makeSound() {
    console.log(`${this.name} says ${this.sound}`);
  }
}

const dog = new Animal('Dog', 'Woof');
dog.makeSound(); // 'Dog says Woof'
```

### 4. 클래스 상속
- `extends` 키워드를 사용하면 다른 클래스를 상속받을 수 있습니다.
- 부모 클래스의 속성과 메서드를 자식 클래스에서 재사용하거나 확장할 수 있습니다.

#### 예제 코드:
```javascript
class Vehicle {
  constructor(type, speed) {
    this.type = type;
    this.speed = speed;
  }

  move() {
    console.log(`${this.type} is moving at ${this.speed} km/h.`);
  }
}

class Car extends Vehicle {
  constructor(brand, speed) {
    super('Car', speed); // 부모 클래스의 생성자를 호출합니다.
    this.brand = brand;
  }

  honk() {
    console.log(`${this.brand} is honking!`);
  }
}

const myCar = new Car('Tesla', 120);
myCar.move(); // 'Car is moving at 120 km/h.'
myCar.honk(); // 'Tesla is honking!'
```

# 느낀 점
- 객체와 클래스는 코드의 구조화를 도와주며, 재사용성을 높이는 데 매우 유용한 도구라는 점을 알게 되었습니다.
- 상속을 활용하면 코드 중복을 줄일 수 있고, 유지보수가 훨씬 쉬워질 것 같습니다.

# 오늘의 난관
- 클래스 내부에서 `this`가 가리키는 대상을 이해하는 데 시간이 걸렸습니다.
- 상속 구조에서 `super` 키워드를 사용하는 방법이 처음에는 낯설었습니다.

# 문제 해결 과정
- MDN 웹 문서를 참고하여 `this`와 `super` 키워드의 동작 방식을 다시 학습했습니다.
- 간단한 예제를 작성하고 직접 실행하면서 개념을 익혔습니다.

# 앞으로의 계획
- 자바스크립트 객체(object)와 배열(array), 맵(map), 셋(set)과 관련한 것들을 더 학습할 예정입니다.
- 연휴에 객체와 클래스를 활용하여 간단한 프로젝트를 만들어 실습할 계획입니다.

