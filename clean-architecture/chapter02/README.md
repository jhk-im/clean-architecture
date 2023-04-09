# 두 가지 가치에 대한 이야기

## 두 가지 가치

> 모든 소프트웨어 시스템은 이해관계자에게 `행위(behavior)`와 `구조(structure)`라는 가치를 제공하며 개발자는 두 가지 가치를 반드시 높게 유지해야 하는 책임을 가진다.

### 행위(behavior)

프로그래머를 고용하는 이유는 이해관계자를 위해 기계가 수익을 창출하거나 비용을 절약하도록 만들기 위해서다.

```txt
* 기능 명세서, 요구사항 문서 등을 구체화
* 기계가 이러한 요구사항을 만족하도록 코드 작성
* 기계가 요구사항을 위반 할 시 문제 해결

프로그래머의 역할은 위 내용이 전부가 아니다.
```

### 아키텍처(architecture)

`"소프트웨어를 만드는 이유는 기계의 행위를 쉽게 변경할 수 있도록 하기 위해서다."`

```txt
* 소프트웨어는 변경하기 쉬워야함
* 개발 비용 증가는 변경사항의 범위와 형태의 차이에 있음
```

새로운 변경 사항을 적용하는 경우 이전의 변경사항보다 조금 더 힘들어지는데, 단순히 시스템이 커지는 것이 원인이 아니라 `시스템의 형태와 요구사항의 형태가 서로 맞지 않기 때문이다.`

```txt
* 문제의 원인은 시스템 아키텍처에 있음
* 시스템 아키텍처가 특정 형태를 선호 할수록 구조에 맞추는게 어려워짐
* 아키텍처는 형태에 독립적이어야함
```

### 더 높은 가치

`"소프트웨어 시스템의 동작 보다 소프트웨어 시스템을 변경하기 쉽도록 하는 것이 더 가치가 높다. 결국 기능보다 아키텍처가 가치가 높다는 의미이다."`

### 아이젠하워 매트릭스

|||
|---|---|
|중요함/긴급함|중요함/긴급하지 않음|
|중요하지 않음/긴급함|중요하지 않음/긴급하지 않음|

```txt
* 긴급한 문제가 매우 중요한 문제일 경우는 거의 없음
* 중요한 문제가 매우 매우 긴그한 문제일 경우는 거의 없음
```

소프트웨어의 첫 번째 가치인 행위는 긴급하지만 매번 높은 중요도를 가지지 않는다. 두 번째 가치인 아키텍처는 중요하지만 긴급성을 필요로 하는 경우는 절대 없다.

```txt
소프트 웨어에서의 우선순위
1. 긴급하고 중요한
2. 긴급하지 않지만 중요한
3. 긴급하지만 중요하지 않은
4. 긴급하지도 중요하지도 않은
```

중요한 일(아키텍처)은 가장 높은 두 순위를 차지하지만 행위는 첫 번째와 세 번째에 위치한다. 개발자가 흔하게 저지르는 실수는 세 번째 항목을 첫 번째로 격상시키는 것이다. `긴급한 일과 중요한 일을 구분하지 못한다`는 것이다. 관리자는 보통 아키텍처의 중요성을 평가할 능력을 겸비하지 못한다.

소프트웨어 개발자라면 `긴급성이 아닌 아키텍처의 중요성을 설득해야 한다.`

### 아키텍처를 위해 투쟁하라

```txt
아키텍처가 후순위가 된다면?
* 개발비용이 늘어남
* 일부 혹은 전체 시스템 변경이 불가능해짐

-> 개발자 스스로 옳다고 믿는 가치를 위해 투쟁 해야한다.
```