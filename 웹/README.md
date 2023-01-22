## 브라우저의 작동원리
<details>
<summary>브라우저 렌더링 방식에 대해 설명하세요⭐️⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->
브라우저라는 것은 인터넷에 접속할 때 사용하는 크롬, 사파리, 파이어폭스 등을 말함

1. HTML 파일과 CSS 파일을 파싱해서 각각 Tree를 만든다. (Parsing)

2. 두 Tree를 결합하여 Rendering Tree를 만든다. (Style)

3. Rendering Tree에서 각 노드의 위치와 크기를 계산한다. (Layout)

4. 계산된 값을 이용해 각 노드를 화면상의 실제 픽셀로 변환하고, 레이어를 만든다. (Paint)

5. 레이어를 합성하여 실제 화면에 나타낸다. (Composite)
</details>

<details>
<summary>리플로우와 리페인트에 대해 설명하세요⭐️⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->
리플로우: 생성된 DOM 노드의 레이아웃 수치 변경 시 영향 받은 모드 노드의 수치를 다시 계산하여 렌더 트리를 재생성하는 과정, DOM 요소의 기하학적 속성이 변경될 때, 브라우저 사이즈가 변할 때, 스타일시트가 로딩되었을 때 발생하는 변화들을 다시 계산해주는 과정을 뜻하며, 레이아웃이라고도 함
리페인트: 리플로우 과정이 끝난 후 생성된 렌더 트리를 다시 그리는 과정, 변경된 요소를 실제로 화면에 그려주는 작업을 뜻함, 리플로우가 발생하면 필연적으로 리페인트가 실행됨, 리플로우보다는 상대적으로 훨씬 가벼운 작업임
</details>

<details>
<summary>웹사이트 속도를 개선하는 방법에 대해 아는대로 말해보세요⭐️⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->

</details>

<details>
<summary>반응형 웹은 무엇이고 장단점에 대해 설명하세요⭐️⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->
정의: 한 가지의 웹사이트로 다양한 종류의 기기에 최적화된 화면을 보여주는 것

장점

하나의 템플릿만을 사용해 다양한 사용자와 기긱에 대응할 수 있어 개발이 간편하다는 장점을 가짐

화면 크기가 해상도에 상관없이 웹 사이트를 잘 보여줌

어느기기, 어떤 접속 환경에서도 url이 같음

최신 웹 표준을 따름

트래픽 관리도 용이

단점

브라우저와 호환성에 문제가 있을 수 있음

디자인 자유도 떨어짐. 100% 맞춤 디자인이 어려움

성능 문제 있을 수 있음(로딩속도, 이미지 리사이징)
</details>
<br></br>

## 이벤트 핸들링이란
<details>
<summary>이벤트 핸들링이란⭐️⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->

</details>

<details>
<summary>이벤트 버블링(Event-Bubbling)과 이벤트캡쳐링(Event-Capturing)이란⭐️⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->

</details>

<details>
<summary>event.preventDefault메서드는 언제, 왜 사용하는지 설명해주세요⭐️⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->
- 정의: 이벤트를 명시적으로 처리하지 않은 경우, 해당 이벤트의 default 동작을 실행하지 않도록 지정하는 함수

- 언제:
'a태그'를 클릭했을 때 지정된 href 링크로 이동하지 않게 하고 싶을 때
'form태그'내의 submit 역할을 하는 버튼을 클릭했을 때, 새로 실행하지 않게 하고 싶을 때
</details>

<details>
<summary>이벤트 위임(event delegation)이란⭐️⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->

</details>
<br></br>

## CORS
<details>
<summary>CORS 오류란⭐️⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->
Cross-Origin Resource Sharing의 약자로
타 도메인 간에 자원을 공유할 수 있게 해주는 것을 의미한다
cors표준은 웹 브라우저가 사용하는 정보를 읽을 수 있도록 허가된 출처 집합을
서버에게 알려주도록 허용하는 특정 http헤더를 추가함으로써 동작한다
브라우저가 리소스 요청됨(coross-origin 요청) -> 보안상의 이유로 제한(Same-Origin-Policy동일 근원 정책) -> 요청하는 대상과 프로토콜과 포트가 같아야함 -> JSONP와 cors가 나옴
</details>

<details>
<summary>CORS 요청의 종류⭐️</summary>
<!-- 한칸 공백 필요  -->

</details>

<details>
<summary>Preflight Request는 무엇인가요⭐️⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->

</details>
<br></br>

## Document Object Model
<details>
<summary>Document Object Model를 설명하세요⭐️⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->

</details>
<details>
<summary>Document Object Model를 설명하세요⭐️⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->

</details>
<br></br>

## 크로스 브라우징
<details>
<summary>크로스 브라우징은 무엇인가요⭐️⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->

</details>
<br></br>

## HTTP
<details>
<summary>HTTP란⭐️⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->

</details>

<details>
<summary>HTTP Method의 종류는⭐️</summary>
<!-- 한칸 공백 필요  -->

</details>

<details>
<summary>BEM(Block Element Modifier)이란⭐️⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->

</details>
<br></br>

## 서버 사이드 렌더링 vs 클라이언트 사이드 렌더링
<details>
<summary>서버 사이드 렌더링 vs 클라이언트 사이드 렌더링은 무엇인가요⭐️⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->

</details>

<details>
<summary>서버 사이드 렌더링 vs 클라이언트 사이드 렌더링은 무엇인가요⭐️⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->

</details>
<br></br>

## CSS Methodology
<details>
<summary>CSS Methodology란⭐️</summary>
<!-- 한칸 공백 필요  -->

</details>

<details>
<summary>SMACSS(Scalable and Modular Architecture for CSS)이란⭐️⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->

</details>

<details>
<summary>OOCSS(Object Oriented CSS)이란⭐️⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->

</details>


<details>
<summary>BEM(Block Element Modifier)이란⭐️⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->

</details>
<br></br>

## Normalize.css vs Reset.css
<details>
<summary>Normalize.css와 Reset.css 의 차이는⭐️</summary>
<!-- 한칸 공백 필요  -->

</details>
<br></br>

## 개발 환경
<details>
<summary>웹팩(webpack)은 무엇이고 왜 필요한가요⭐️⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->
기능별로 모듈화했던 자바스크립트 파일들을 묶는 것을 말함

대표 예시로는 웹팩이 있음

장점

이전에 각 파일마다 서버에 요청을 하여 자원을 얻어와야했던 반면, 같은 타입(html, css, js) 등 파일을 묶어서 요청/응답을 받아 네터워크 코스트가 감소함

다양한 모드가 지원되면서 최적화, 코드 압축 등 작업 지원

웹팩의 주요 구성 요소 중 하나인 로더가 일부 브라우저에서 지원이 되지 않는 ES6 형식의 자바스크립트 파일을 ES5로 변환하여 사용가능, 다른 모든 브라우저에 대해서도 커버 가능
</details>

<details>
<summary>바벨과 폴리필이란⭐️⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->

</details>

<details>
<summary>CI와 CD란⭐️⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->

</details>
<br></br>

