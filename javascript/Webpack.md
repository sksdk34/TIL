# Webpack
## Module
- 프로그램을 구성하는 구성 요소의 일부
- 관련된 데이터와 함수들이 묶여서 모듈을 형성하고 파일 단위로 나뉘는 것이 일반적임
- 모듈화 프로그래밍은 기능별로 파일을 나눠가며 프로그래밍을 하는 것이 유지보수가 쉬움

## Bundler
- 지정한 단위로 파일들을 하나로 만들어서 요청에 대한 응답으로 전달할 수 있는 환경을 만들어주는 역할
- 번들러를 사용하면 소스 코드를 모듈별로 작성할 수 있고 모듈간 또는 외부 라이브러리의 의존성도 쉽게 관리할 수 있음

## Webpack
- JS 정적 모듈 번들러
- `Webpack`에서는 모든 것(e.g. js, stylesheet, image ...)이 모듈이고 JS 모듈로 로딩해서 사용

### 사용 이유
1. #### 네트워크 병목현상 해결
    - `HTML`에서는 `<script>` 태그로 자바스크립트 파일을 실행할 수 있지만 많은 파일을 로드할 경우 네트워크 병목현상이 발생
    - 병목 현상을 줄이기 위해서는 하나의 자바스크립트 파일로 로드하면 되지만 하나의 자바스크립트에 여러 모듈을 합치면 가독성, 유지보수 효율이 떨어짐
    - 웹팩은 여러 파일을 하나의 파일로 묶어주어 병목 현상을 최소화할 수 있음
2. #### 모듈 단위로 개발 가능
    - 모듈 번들러를 사용하면 모듈 단위로 코딩이 가능
3. #### 코드를 압축/최적화 할 수 있음
4. #### ES6 이상의 스크립트 사용 가능
5. #### LESS, SCSS 사용 가능

### 주요 개념 4가지(Entry, Output, Loader, Plugin)
#### 1. Entry
- 의존성 그래프의 시작점을 웹팩에서는 엔트리(Entry)라고함
- 웹팩은 엔트리를 통해서 필요한 모듈을 로딩하고 하나의 파일로 묶음
- 여러개의 엔트리가 존재할 수 있음

#### 2. Output
- 엔트리에 설정한 자바스크립트 파일을 시작으로 하나로 묶음
- 번들링된 결과물의 처리할 위치를 output 에 기록

#### 3. Loader
- 웹팩은 `JS`와 `JSON`만 이해할 수 있음
- 로더는 다른 타입의 파일(e.g. img, stylesheet ...)을 웹팩이 이해하고 처리 가능한 모듈로 변환 시키는 작업을 함

#### 4. Plugin
- 로더가 파일 단위로 처리하는 반면 플러그인은 번들된 결과물을 처리
- 로더가 변환하는 동안 플러그인은 `bundle optimization`, `asset management and injection of environment`와 같은 일을 진행