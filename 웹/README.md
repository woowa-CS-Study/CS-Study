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
<summary>리플로우와 리페인트에 대해 설명하세요⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->
리플로우: 생성된 DOM 노드의 레이아웃 수치 변경 시 영향 받은 모든 노드의 수치를 다시 계산하여 렌더 트리를 재생성하는 과정, DOM 요소의 기하학적 속성이 변경될 때, 브라우저 사이즈가 변할 때, 스타일시트가 로딩되었을 때 발생하는 변화들을 다시 계산해주는 과정을 뜻하며, 레이아웃이라고도 함

리페인트: 리플로우 과정이 끝난 후 생성된 렌더 트리를 다시 그리는 과정, 변경된 요소를 실제로 화면에 그려주는 작업을 뜻함, 리플로우가 발생하면 필연적으로 리페인트가 실행됨, 리플로우보다는 상대적으로 훨씬 가벼운 작업임
</details>

<details>
<summary>웹사이트 속도를 개선하는 방법에 대해 아는대로 말해보세요⭐️⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->
이미지 압축

코드 정리 및 압축

호스팅 업그레이드

브라우저 캐싱 활성화

웹 페이지 속도 개선 테스트
</details>

<details>
<summary>반응형 웹은 무엇이고 장단점에 대해 설명하세요⭐️⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->
정의: 한 가지의 웹사이트로 다양한 종류의 기기에 최적화된 화면을 보여주는 것

장점
- 하나의 템플릿만을 사용해 다양한 사용자와 기긱에 대응할 수 있어 개발이 간편하다는 장점을 가짐
- 화면 크기가 해상도에 상관없이 웹 사이트를 잘 보여줌
- 어느기기, 어떤 접속 환경에서도 url이 같음
- 최신 웹 표준을 따름
- 트래픽 관리도 용이

단점
- 브라우저와 호환성에 문제가 있을 수 있음
- 디자인 자유도 떨어짐. 100% 맞춤 디자인이 어려움
- 성능 문제 있을 수 있음(로딩속도, 이미지 리사이징)
</details>

<details>
<summary>크로스 브라우징은 무엇인가요⭐️⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->
웹 페이지 제작 시에 모든 브라우저에서 깨지지 않고 의도한 대로 올바르게(호환성) 나오게 하는 작업
</details>
<br></br>

## 이벤트 핸들링이란
<details>
<summary>이벤트 핸들링이란⭐️⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->
클릭, 키보드 입력 등 사용자의 어떤 행위를 처리하는 것을 이벤트 핸들링이라고 함

- 이벤트를 받아줄 요소를 선택합니다.
- 그 요소가 어떤 이벤트에 반응할지, 즉 요소와 이벤트를 연결해주는 바인딩을 합니다.
- 이벤트가 발생했을 때 실행될 코드를 작성합니다.
</details>

<details>
<summary>이벤트 버블링(Event-Bubbling)과 이벤트캡쳐링(Event-Capturing)이란⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->
Event Bubbling:
한 요소에 이벤트가 발생하면, 이 요소에 할당된 핸들러가 동작하고, 이어서 부모 요소의 핸들러가 동작함
가장 최상단의 조상 요소를 만날 때까지 이 과정이 반복되면서 요소 각각에 할당된 핸들러가 동작함

<img src="https://joshua1988.github.io/images/posts/web/javascript/event/event-bubble.png" height="200px" width="200px">

Event Capturing:
이벤트 캡쳐는 이벤트 버블링과 반대 방향으로 진행되는 이벤트 전파 방식입니다.

<img src="https://joshua1988.github.io/images/posts/web/javascript/event/event-capture.png" height="200px" width="200px">

</details>

<details>
<summary>event.preventDefault메서드는 언제, 왜 사용하는지 설명해주세요⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->
정의: 이벤트를 명시적으로 처리하지 않은 경우, 해당 이벤트의 default 동작을 실행하지 않도록 지정하는 함수

언제 사용:
- 'a태그'를 클릭했을 때 지정된 href 링크로 이동하지 않게 하고 싶을 때
- 'form태그'내의 submit 역할을 하는 버튼을 클릭했을 때, 새로 실행하지 않게 하고 싶을 때

자세한 설명:
preventDefalut는 해당 이벤트에 기본적으로 설정된 기본 액션을 동작하지 않게 만드는 메서드입니다.
이 메서드를 사용하는 이유는 다양합니다. 가장 대표적인 경우가 form 요소의 submit 이벤트입니다. submit 이벤트는 해당 폼의 정보를 서버로 요청을 보내려는 기본 동작을 가지고 있어서,submit 이벤트가 일어나고 나면 화면이 의도치 않게 전환되거나 새로고침이 되는 경우가 있습니다.
현대 웹 개발에 들어서는 이런 서버 요청은 JavaScript에서 처리하기 때문에 이런 이벤트의 기본 동작은 막아주는 것이 종종 필요합니다.
</details>

<details>
<summary>이벤트 위임(event delegation)이란⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->
이벤트 위임은 캡쳐링과 버블링을 이용한 것으로, 여러 엘리먼트마다 각각 이벤트 핸들러를 할당하지 않고, 공통되는 부모에 이벤트 핸들러를 할당하여 이벤트를 관리하는 방식

- 여러개의 자식 엘리먼트 이벤트 관리하기
- 동적 엘리먼트에 대한 이벤트 관리하기
</details>
<br></br>

## CORS
<details>
<summary>CORS 오류란⭐️⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->
Cross-Origin Resource Sharing의 약자로
타 도메인 간에 자원을 공유할 수 있게 해주는 것을 의미한다

cors표준은 웹 브라우저가 사용하는 정보를 읽을 수 있도록 허가된 출처 집합을 서버에게 알려주도록 허용하는 특정 http헤더를 추가함으로써 동작한다

1. 브라우저가 리소스 요청됨(coross-origin 요청) ->
2. 보안상의 이유로 제한(Same-Origin-Policy동일 근원 정책) ->
3. 요청하는 대상과 프로토콜과 포트가 같아야함 ->
4. JSONP와 cors가 나옴

[자세한 자료](https://inpa.tistory.com/entry/WEB-%F0%9F%93%9A-CORS-%F0%9F%92%AF-%EC%A0%95%EB%A6%AC-%ED%95%B4%EA%B2%B0-%EB%B0%A9%EB%B2%95-%F0%9F%91%8F#:~:text=%EA%B6%8C%EC%9E%A5%ED%95%98%EB%8A%94%20%EB%B0%94%EB%8B%A4.-,%EC%98%88%EB%B9%84%20%EC%9A%94%EC%B2%AD%20(Preflight%20Request),%EC%9D%B8%EC%A7%80%20%EB%AF%B8%EB%A6%AC%20%ED%99%95%EC%9D%B8%ED%95%98%EB%8A%94%20%EA%B2%83%EC%9D%B4%EB%8B%A4.)
</details>

<details>
<summary>CORS 요청의 종류⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->
Simple/Preflight, Credential/Non-Credential의 조합으로 4가지가 존재

1. Simple Request
2. Preflight Request
3. Request with Credential
4. Request without Credential
</details>

<details>
<summary>Preflight Request는 무엇인가요⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->
사실 브라우저는 요청을 보낼때 한번에 바로 보내지않고, 먼저 예비 요청을 보내 서버와 잘 통신되는지 확인한 후 본 요청을 보낸다.

즉, 예비 요청의 역할은 본 요청을 보내기 전에 브라우저 스스로 안전한 요청인지 미리 확인하는 것이다.

이때 브라우저가 예비요청을 보내는 것을 Preflight라고 부르며, 이 예비요청의 HTTP 메소드를 GET이나 POST가 아닌 OPTIONS라는 요청이 사용된다는 것이 특징이다.
</details>
<br></br>

## Document Object Model(DOM)
<details>
<summary>Document Object Model(DOM)를 설명하세요⭐️⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->
문서 객체 모델(DOM, Document Object Model)은 XML이나 HTML 문서에 접근하기 위한 일종의 인터페이스입니다.

이 객체 모델은 문서 내의 모든 요소를 정의하고, 각각의 요소에 접근하는 방법을 제공합니다.
</details>

<details>
<summary>DOM의 종류를 설명하세요⭐️</summary>
<!-- 한칸 공백 필요  -->
W3C DOM 표준은 세 가지 모델로 구분됩니다.

1. Core DOM : 모든 문서 타입을 위한 DOM 모델
2. HTML DOM : HTML 문서를 위한 DOM 모델
3. XML DOM : XML 문서를 위한 DOM 모델
</details>
<br></br>

## HTTP
<details>
<summary>HTTP 프로토콜의 특징에 대해 설명해주세요⭐️⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->
Hyper Text Transfer Protocol
요청 메서드 를 정의하여, 주어진 리소스에 수행하길 원하는 행동을 나타내는 것

www 상에서 서버와 클라이언트가 정보(데이터)를 주고 받을 수 있는 프로토콜로, HTML문서를 주고 받는데 사용됨.

TCP 방식 : client - server 중 한 곳이 연결을 끊을 때까지 연결을 유지함.
HTTP 방식 : client가 server에서 html을 다운받고 나면 연결을 끊어버림.(HTTP통신의 특징 - 비연결(stateless))

특징
Stateless
클라이언트와 서버가 연결을 성공한 후, 클라이언트의 요청에 대해 서버가 응답을 하고 나면 연결을 끊어버리는 것을 말한다.

장점
통신 간의 연결 상태 처리나 정보의 저장을 관리할 필요가 없어서 서버 디자인이 간단해진다.

단점
연결을 끊어버리기 때문에 서버에서 클라이언트의 현재 상태를 알 수 없음. 로그인을 이미 했는데 연결을 끊었기 때문에 이후 작업에서 Client가 로그인을 했었는지 안했었는지 알 수 없음.
=> 이 문제를 위해 Cookie와 Session으로 클라이언트의 상태를 저장해서 연결은 끊어졌지만 사용자에게 마치 연결이 되어 있는 것처럼 서비스를 제공한다.

Request, Response
Request(요청)
웹 브라우저(Client)에서 웹 서버로 보내는 요청. 서버에게 데이터를 전송할 때 Request 객체에 담아 전달하게 된다.

Response(수신)
웹 서버에서 웹 브라우저(Client)로의 응답. 클라이언트로부터 서버에게 요청이 일어나고 나면 서버는 브라우저에 전달할 데이터를 Response 객체를 통해 전달한다.
___
HTTP는 클라이언트가 서버에 요청을 보내면 서버는 그에 대한 응답을 보내는 클라이언트 서버 구조로 이루어져 있으며, 무상태성, 비연결성이라는 특징을 갖습니다.

무상태성은 서버가 클라이언트의 상태를 기억하지 않는다는 뜻입니다. 즉, 상태 기억의 주체가 클라이언트가 된다는 말이며, 중간에 요청을 처리하는 서버가 바뀌어도 클라이언트가 상태를 잘 담아서 요청을 보내면 응답을 제대로 받을 수 있습니다.
서버가 바뀌어도 응답에 문제가 없다는 뜻은, 필요에 따라 서버를 무한히 증설할 수 있다는 의미입니다. 즉, 무상태성이라는 특성 덕에 서버의 무한한 증설이 가능해집니다.

비연결성은 요청과 응답을 주고 받은 후에 서버와의 연결을 끊는 것을 의미합니다. 서버와의 연결을 지속하지 않고 필요할 때에만 연결하기 때문에 최소한의 자원만 사용하게 된다는 장점이 있습니다. 하지만 HTTP 1.0 버전은 여러 요청을 보내야 할 때에도 매 요청마다 서버 연결과 종료를 반복하는 비효율성이 발생한다는 한계가 있습니다. 이러한 한계점을 HTTP 1.1 버전에서는 지속 연결과 파이프라인, HTTP 2.0 버전에서는 멀티플렉싱을 활용해서 해결합니다.
</details>

<details>
<summary>HTTP Method의 종류는⭐️</summary>
<!-- 한칸 공백 필요  -->
GET
특정 리소스의 표시를 요청할 때 사용, 오직 데이터를 받기만 한다.
(SELECT 문을 이용한 데이터를 수신)

POST
특정 리소스에 엔티티를 제출할 때 사용
서버에 Data를 보내기 위한 용도

PUT
서버가 Client 요청의 Body를 확인하여 요청 URL에 새로운 Resouce를 생성
서버의 Resource에 Data를 저장하기 위한 용도

DELETE
요청 Resource를 삭제하도록 요청
BUT HTTP 규격에는 Client 요청에도 서버가 무효화 시킬 수 있다고 정의됨
DELETE Method는 항상 보장되지 않는다.
</details>
<br></br>

## Cookie와 Session
<details>
<summary>Cookie는 무엇인가요⭐️⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->
사용자의 디스크나 웹 브라우저 메모리에 저장된다.
클라이언트 측에 “key와 value”형태의 text 타입으로 데이터가 저장된다. 데이터의 크기에 제한이 있다.

프로세스
- 브라우저에서 웹 페이지 접속
- 웹 서버에서 쿠키를 생성.
- 생성한 쿠키에 데이터를 담아 요청에 응답할 때 클라이언트에게 함께 전송.
- 클라이언트가 보관하다가 서버에 재요청할 때 쿠키를 함께 전송.
- 클라이언트와 서버가 로그인 정보가 유지되어있는 것처럼 사용.
</details>

<details>
<summary>Session은 무엇인가요⭐️⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->
웹 서비스를 위한 사용자의 정보를 서버측에 저장한다.
서버 측에 객체 타입으로 저장된다. 서버가 수용 가능한 만큼 저장할 수 있다.

프로세스
- 클라이언트가 서버에 접속 시 세션 ID를 발급
- 클라이언트는 쿠키(쿠키이름 : JSESSIONID)를 이용해 세션 ID를 저장해서 가지고 있음.
- 클라이언트가 서버에 재 요청 시 쿠키(JSESSIONID)를 이용하여 세션ID 값을 서버에 전달.

저장 기간
session.invalidate() 혹은 웹 브라우저가 종료될 때까지 데이터가 유지된다.
</details>

<details>
<summary>Cookie와 Session의 차이는 무엇인가요⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->
쿠키와 세션의 역할은 비슷하다. 가장 큰 차이점은 사용자의 정보가 저장되는 위치이다.
보안 면에서는 세션이 더 우수하고, 세션의 경우 서버의 처리가 필요하기 때문에 요청 속도는 쿠키가 더 빠르다.
</details>
<br></br>

## 서버 사이드 렌더링 vs 클라이언트 사이드 렌더링
<details>
<summary>서버 사이드 렌더링 vs 클라이언트 사이드 렌더링은 무엇인가요⭐️⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->
SSR: 브라우저에 나타나는 형태 그대로를 HTML로 만들어 제공하며, 브라우저는 HTML을 표시하는 방식

CSR: SPA (Single Page Application), 서버는 JSON파일만 보내주고, HTML을 그리는 역할은 JavaScript를 통해 클라이언트 측에서 수행
</details>
<br></br>

## 디자인 패턴의 종류(MVC,MVVM)
<details>
<summary>디자인 패턴이란⭐️⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->
어떤 것을 개발할 때 발생했던 문제점들을 정리해서 좀 더 쉽고 편리하게 개발할 수 있도록 만든 특정한 방법들을 의미한다.
</details>

<details>
<summary>MVC Pattern⭐️⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->
Model-View-Controller의 약자로,
대표적인 디자인 패턴으로 개발할 때 구성요소를 Model, View, Controller로 역할을 나누어 개발을 하는 것을 의미한다.
사용자가 Controller를 조작하면 Controller는 Model을 통해 데이터를 가져오고 해당 데이터를 View에게 뿌려준다.
<br></br>
<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2F7IE8f%2FbtqBRvw9sFF%2FAGLRdsOLuvNZ9okmGOlkx1%2Fimg.png" width="200" height="200">
<br></br>
MVC 패턴의 동작 순서
사용자의 Action들은 Controller에 들어오게 된다.
Controller는 사용자의 Action를 확인하고, Model을 업데이트한다.
Controller는 Model을 나타내줄 View를 선택한다.
View는 Model을 이용하여 화면을 나타낸다.

MVC패턴을 사용하는 프레임워크/라이브러리
- Angular JS
- DJango
- React 등
</details>

<details>
<summary>MVVM Pattern⭐️⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->
MVVM 패턴은 Model + View + View Model를 합친 용어입니다. Model과 View은 다른 패턴과 동일합니다.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FCiXz0%2FbtqBQ1iMiVT%2FstaXr7UO95opKgXEU01EY0%2Fimg.png" width="200" height="200">

Model : 어플리케이션에서 사용되는 데이터와 그 데이터를 처리하는 부분입니다.

View : 사용자에서 보여지는 UI 부분입니다.

View Model : View를 표현하기 위해 만든 View를 위한 Model입니다. View를 나타내 주기 위한 Model이자 View를 나타내기 위한 데이터 처리를 하는 부분입니다.

MVVM 패턴의 동작 순서
1. 사용자의 Action들은 View를 통해 들어오게 됩니다.
2. View에 Action이 들어오면, Command 패턴으로 View Model에 Action을 전달합니다.
3. View Model은 Model에게 데이터를 요청합니다.
4. Model은 View Model에게 요청받은 데이터를 응답합니다.
5. View Model은 응답 받은 데이터를 가공하여 저장합니다.
6. View는 View Model과 Data Binding하여 화면을 나타냅니다.
7. 대표적인 디자인 패턴으로 개발할 때 구성요소를 Model, View, Controller로 역할을 나누어 개발을 하는 것을 의미한다.
8. 사용자가 Controller를 조작하면 Controller는 Model을 통해 데이터를 가져오고 해당 데이터를 View에게 뿌려준다.

장점

MVVM 패턴은 View와 Model 사이의 의존성이 없습니다. 또한 Command 패턴과 Data Binding을 사용하여 View와 View Model 사이의 의존성 또한 없앤 디자인패턴입니다. 각각의 부분은 독립적이기 때문에 모듈화 하여 개발할 수 있습니다.
</details>
<br></br>

## CSS Methodology
<details>
<summary>CSS Methodology란⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->
명확하고 일관성있는 규칙

SMACSS(Scalable and Modular Architecture for CSS): 범주화

OOCSS(Object Oriented CSS): 구조와 모양을 분리,컨테이너와 컨텐츠를 분리

BEM(Block Element Modifier): 블록(block), 요소(element), 상태(modifier)로 구분하여 클래스 작성하며 엄격한 네이밍 규칙을 가짐
</details>

<details>
<summary>SMACSS(Scalable and Modular Architecture for CSS)이란⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->
CSS를 범주화(Categorization)로 패턴화 하고자 하는 방법론이다

SMACSS는 작성할 CSS를 비슷한 종류끼리 모아 5가지 스타일로 나누고 각 유형에 맞는 선택자와 작명법, 코딩 기법을 제시한다. 기본(base), 레이아웃(layout), 모듈(module), 상태(state), 테마(theme) 다섯가지의 범주를 제시한다.

기본(base)
: Reset, Variable 등을 포함하고 !important를 쓰지 않는다.

레이아웃(layout)
: 주요 요소(id)와 하위 요소(class)로 구분하고 접두사를 사용한다.

모듈(module)
: 재사용성이 높은 구성 요소를 정의한다.

상태(state)
: 요소의 상태 변화를 표현하고 접두사 “is-“나 “s-“를 사용한다.

테마(theme)
: 사용자가 선택 가능 하도록 스타일을 재선언하여 사용한다.

SMACSS 사용시에는 지켜야 할 유의사항이 몇 가지 존재하는데, 대표적으로 아래의 4가지 유의사항들이 존재한다.
- 파생된 CSS셀렉터 사용금지
- Id 셀렉터 사용금지
- !Important 사용금지
- 다른 개발자들이 이해할 수 있도록 class 이름을 의미있게 지어야 함
</details>

<details>
<summary>OOCSS(Object Oriented CSS)이란⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->
CSS를 모듈 방식으로 작성하여 중복을 줄이는 방식의 방법론이다.
주요 원리는 구조와 스타일을 분리해서 작성하는 것이다.

2가지 기본원칙
- 구조(structure)와 모양(skin)의 분리 : 반복적인 시각적 기능(배경, 테두리..)을 별도의 “스킨”으로 정의하여 다양한 객체와 혼합하여 중복 코드없이 시각적 다양성을 표현할 수 있다.
- 콘테이너와 콘텐츠의 분리 : 스타일을 정의할때 위치에 의존적인 스타일을 사용하지 않는다. 사물의 모양은 어디에 위치 하던지 동일하게 보인다. (예: .object h2{} 사용하지 않고 h2에 .title(클래스 이름)을 부여하여 사용한다. 이렇게 하면 클래스가 없는 h2는 모두 동일한 모습이고, title 클래스 역시 동일하게 보일것이며, 불필요한 스타일을 중복해서 정의할 필요가 없다)

이점
- 많은 CSS 코드가 재사용되면서 코드의 길이가 줄어든다. 즉 css 파일 크기가 작아져서 속도를 향상 시킬 수 있다.
- 새로운 요소를 추가할때, 기존 모듈을 통해서 재사용이 가능하고 쉽게 확장 가능하여 유지보수성이 높아진다.
</details>


<details>
<summary>BEM(Block Element Modifier)이란⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->
CSS 제작 방법론으로, 일종의 네이밍 컨벤션이라고 볼 수 있다.
html 요소들을 각각 Block, Element, Modifier이렇게 세 가지로 분류해 작명한다.
이를 통해 복잡한 UI에서도 쉽고 빠르게 인터페이스를 개발할 수 있으며 복사 및 붙여 넣기없이 기존 코드를 재사용 할 수 있습니다.

- Block
재사용 가능한 독립적 블록, 가장 바깥쪽 상위요소
재사용을 위해 margin 또는 padding을 적용하지 않는다
블럭은 블럭을 감쌀 수 있다
- Element
블록을 구성하는 종속적인 하위요소
소속된 블록에 의존적이다
- Modifier
블록이나 엘리먼트의 변형, 속성을 의미 (모양,상태,동작 등)
기능은 같으나 모양 등이 다를 경우 사용한다
</details>

<details>
<summary>Normalize.css와 Reset.css 의 차이는⭐️</summary>
<!-- 한칸 공백 필요  -->
Reset.css는 초기화를 시키는 것에 집중
Normalize.css는 초기화를 시키지만 어느정도의 스타일이 가미되어있음
</details>
<br></br>

## 개발 환경
<details>
<summary>웹팩(webpack)은 무엇이고 왜 필요한가요⭐️⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->
기능별로 모듈화했던 자바스크립트 파일들을 묶는 것을 말함

장점
- 이전에 각 파일마다 서버에 요청을 하여 자원을 얻어와야했던 반면, 같은 타입(html, css, js) 등 파일을 묶어서 요청/응답을 받아 네터워크 코스트가 감소함
- 다양한 모드가 지원되면서 최적화, 코드 압축 등 작업 지원
- 웹팩의 주요 구성 요소 중 하나인 로더가 일부 브라우저에서 지원이 되지 않는 ES6 형식의 자바스크립트 파일을 ES5로 변환하여 사용가능, 다른 모든 브라우저에 대해서도 커버 가능
</details>

<details>
<summary>바벨(Babel)과 폴리필(Polyfill)이란⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->
바벨의 뜻:
바벨은 트랜스파일러로, 모던 자바스크립트 코드를 구 표준을 준수하는 코드로 바꿔줍니다.

바벨은 코드를 재작성해주는 트랜스파일러 프로그램입니다. 바벨은 개발자의 컴퓨터에서 돌아가는데, 이를 실행하면 기존 코드가 구 표준을 준수하는 코드로 변경됩니다. 변경된 코드는 웹사이트 형태로 사용자에게 전달되어 버전 차이로 인한 호환성 문제를 해결 해 줍니다. 웹팩과 같은 모던 프로젝트 빌드 시스템은 코드가 수정될 때마다 자동으로 트랜스파일러를 동작시켜줍니다.

폴리필의 뜻:
폴리필을 사전에서 찾아보면  충전솜이라는 의미를 가지고 있습니다. 폴리필의 역할은 사전 의미처럼 부족한 부분을 채워주는 역할을 합니다. 폴리필(polyfill)은 말 그대로 구현이 누락된 새로운 기능을 메꿔주는(fill in) 역할을 합니다.(쉽게 정의하면 크로스 브라우징을 뜻합니다.)

바벨과 폴리필이 필요한 이유?
브라우저마다 지원할 수 있는(랜더링 하는) 스펙이 다르기 때문입니다.
</details>

<details>
<summary>CI와 CD란⭐️⭐️⭐️</summary>
<!-- 한칸 공백 필요  -->
CI는 빌드/테스트 자동화 과정 과정
CD는 배포 자동화 과정

CI/CD는 자동화하여 애플리케이션을 더욱 짧은 주기로 고객에게 제공하는 방법

CI/CD는 새로운 코드 통합으로 인해 개발 및 운영팀에 발생하는 문제(일명 "통합 지옥(integration hell)")를 해결하기 위한 솔루션
</details>
<br></br>

