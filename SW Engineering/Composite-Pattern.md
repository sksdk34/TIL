# Composite Pattern
- 구조 패턴
- 부분-전체의 관계를 갖는 객체들을 정의할 때 사용하는 패턴
- 전체와 부분을 구분하지 않고 동일한 인터페이스 사용
- 전체 클래스도 부분 클래스처럼 일반화되기 때문에 전체도 부분이 될 수 있음
- 트리 구조의 객체를 표현할 때 유용

## 역할이 수행하는 작업
- ### Componenet
    - 구체적인 부분
    - Leaf 클래스와 전체에 해당하는 Composite 클래스의 공통 인터페이스를 정의
- ### Leaf
    - 구체적인 부분 클래스로 Composite 객체의 부품
- ### Composite
    - 전체 클래스로 복수 개의 Component를 갖도록 정의
    - 복수 개의 Leaf와 복수 개의 Composite 객체를 부분으로 가질 수 있음