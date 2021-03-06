# Strategy Pattern
- 행위 패턴으로 분류됨
- 행위를 클래스로 캡슐화해 동적으로 행위를 자유롭게 바꿀 수 있게 해주는 패턴
    - 같은 문제를 해결하는 여러 알고리즘이 클래스별로 캡슐화되어 있고 이들이 필요할 때 교체할 수 있도록 함으로써 동일한 문제를 다른 알고리즘을 해결할 수 있게하는 디자인 패턴
- 전략을 쉽게 바꿀 수 있도록 해주는 디자인 패턴
    - 전략이란 어떤 목적을 달성하기 위해 일을 수행하는 방식, 비지니스 규칙, 문제를 해결하는 알고리즘 등

## 역할이 수행하는 작업
- ### Strategy 
    - 인터페이스나 추상 클래스로 외부에서 동일한 방식으로 알고리즘을 호출하는 방법을 명시
- ### ConcreteStarategy
    - 스트래티지 패턴에서 명시한 알고리즘을 실제로 구현한 클래스
- ### Context
    - 스트래티지 패턴을 이용하는 역할을 수행
    - 필요에 따라 동적으로 구체적인 전략을 바꿀 수 있도록 `setter` 메서드 제공