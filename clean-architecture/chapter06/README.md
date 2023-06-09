# 함수형 프로그래밍

## 함수형 프로그래밍 개요

* 함수형 프로그래밍의 개요는 프로그래밍 그 자체보다 앞서 등장함
* 핵심이 되는 기반은 람다(lambda)계산법

* 캡슐화(encapsulation), 상속(inheritance), 다형성(polymorphism)
* 객체 지향이란 위 3가지를 적절하게 조합하는 것
* 객체 지향 언어는 최소한 3가지 요소를 반드시 지원해야 함

### `함수형 프로그래밍의 사례`

```java
// 자바 정수의 제곱 구현
for (int i = 0; i < 25; i++) {
    System.out.println(i * i);
}
```

```lisp
; 리스프의 정수의 제곱 구현
(println ;출력한다.
    (take 25 ;0 - 25 까지
        (map (fn [x] (* x x)) ;제곱을
            (range)))) ;정수의
```

* 자바는 가변 변수(mutable variable)를 사용하며 가변 변수는 프로그램 실행 중 상태가 변할 수 있음
* 자바의 i가 가변 변수
* 클로저 프로그램에선 가변 변수가 없음
* 리스프의 x와 같은 변수가 한 번 초기화되면 절대 불변
* 함수형 언어에서 변수는 변경되지 않음

### 불변성과 아키텍처

* 경합(race), 교착상태(deadlock) 조건, 동시 업데이트(concurrent update) 문제가 모두 가변 변수로 인해 발생함
* 다수의 스레드와 프로세스를 사용하는 애플리케이션에서 발생하는 모든 문제는 가변 변수가 없으면 발생하지 않음
* 불변성은 실현 가능하나 타협이 필요함

### 가변성의 분리

* 애플리케이션 내부 서비스를 가변 컴포넌트와 불변 컴포넌트로 분리
* 불변 컴포넌트는 함수형 방식으로 작업처리
* 트랜잭션 메모리와 같은 실천법을 사용하여 동시 업데이트와 경합 조건으로 부터 가변 변수 보호
* 가변성의 분리를 위해선 가변 변수들을 보호하는 적절한 수단이 뒷받침 되어야 함

### 이벤트 소싱(Event Sourcing)

* 애플리케이션의 수명주기 동안 문제없이 동작할 정도의 저장 공간과 처리 능력만을 요구
* 상태가 아닌 트랜잭션을 저장하는 전략
* 상태가 필요해지면 시작점부터 모든 트랜잭션 처리
* 저장 공간과 처리 능력이 충분하면 애플리케이션이 완전한 불변성을 갖도록 할 수 있고, 완전한 함수형으로 만들 수 있음
* 소스 코드 버전 관리 시스템이 정확히 이 방식으로 동작함

### 결론

* 구조적 프로그래밍은 제어흐름의 직접적인 전환에 부과되는 규율
* 객체 지향 프로그래밍은 제어흐름의 간접적인 전환에 부과되는 규율
* 함수형 프로그래밍은 변수 할당에 부과되는 규율

`소프트웨어는 급격히 발전하는 기술이 아니다.`

`소프트 웨어는 순차(sequnce), 분기(selection), 반복(iteration), 참조(indirection)로 구성된다.`
