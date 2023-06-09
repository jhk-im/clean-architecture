# 객체 지향 프로그래밍

## 객체 지향이란?

`좋은 아키텍처를 만드는 일은 객체 지향 설계원칙을 이해하고 응용하는 데서 출발한다.`

* 캡슐화(encapsulation), 상속(inheritance), 다형성(polymorphism)
* 객체 지향이란 위 3가지를 적절하게 조합하는 것
* 객체 지향 언어는 최소한 3가지 요소를 반드시 지원해야 함

### `캡슐화(encapsulation)`

* 데이터와 함수를 쉽고 효과적으로 캡슐화
* 완벽한 캡슐화는 C언어
* 대표적인 객체지향 언어들에 의해 캡슐화는 훼손되었음
* 객체 지향의 캡슐화 점수 = 0

### `상속(inheritance)`

* 객체지향 언어가 있기 이전부터 C언어에서 구현할 수 있었음
* 객체지향 언어가 완벽한 상속이라는 새로운 개념을 만든것이 아니라 편리한 방식으로 제공했다고 봐야함
* 객체지향의 상속 점수 = 0.5

### `다형성(polymorphism)`

* 마찬가지로 C언어에서도 다형성을 표현할 수 있음
* C언어의 다형성을 위한 단순한 기법이 모든 객체지향이 지닌 다형성의 근간이 됨
* 함수를 가리키는 포인터를 응용한 것이 다형성
* 객체지향 언어는 다형성을 조금 더 안전하고 편리하게 사용 할 수 있게 해줌
* 포인터를 다룰 때 준수해야 할 관례가 많고 객체지향 언어는 이러한 제어 흐름을 간접적으로 전환하는 규칙을 부과함

### 다형성이 가진 힘

플러그인 아키텍처는 입츌력 장치 독립성을 지원하기 위해 만들어 졌다. 객체 지향의 등장으로 언제 어디서든 프러그인 아키텍처를 적요할 수 있게 되었다.

### 의존성 역전

C -> #include, java -> import와 같이 모든 호출 함수는 피호출 함수가 포함된 모듈의 이름을 명시적으로 지정해야 한다. 이러한 제약 조건으로 인해 제어흐름은 시스템의 행위에 따라 결정되며, 소스코드 의존성은 제어흐름에 따라 결정된다.

객체지향 언어가 다형성을 안전하고 편리하게 제공한다는 것은 의존성을 어디에서든 역전시킬 수 있다는 의미이기도 하다. 객체지향 언어는 소스 코드 의존성이 제어흐름 방향과 일치되도록 제한되지 않는다. 호출하는 모듈이든 호출 받는 모듈이든 관계없이 소프트웨어 아키텍트는 소스코드 의존성을 원하는 방향으로 설정할 수 있다.

이것이 객체지향의 힘이다. 소스코드 변경시 해당 코드가 포함된 컴포넌트만 배포할 수 있는 배포 독립성(independent deploybility)을 구현할 수 있다. 시스템 모듈이 독립적으로 배포할 수 있다는 것은 서로 다른 팀에서 모듈을 독립적으로 개발할 수 있다는 의미미여 이것이 개발 독립성(independent developability)이다.

### 결론

객체지향이란 다형성을 이용하여 전체 시스템의 모든 소스 코드 의존성에 대한 절대적 제어 권한을 획득할 수 있는 능력이다. 고수준의 정책을 포함하는 모듈은 저수준의 세부사항을 포함하는 모듈에 대해 독립성을 보장한다.
