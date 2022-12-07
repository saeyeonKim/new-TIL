#CSS-in-JS 키워드

```
styled-components의 GlobalStyles 이란 무엇이고, 어떻게 사용해야 할까?

전역 스타일을 뜻하며, 공통으로 필요한 스타일은 createGlobalStyle 함수를 사용해 전역 스타일 컴포넌트를 만들 수 있다.
css nesting 이란 무엇일까?

스타일을 선언을 중첩하는 것으로 후손 셀럭터를 간단하게 스타일 할 수 있다.
const styles = styled.div`
	width : 200px;
	height : 200px;
	// css nesting
	p {
		font-size : 20px;
		color : red;
	}
`
CSS reset 이란, 무엇이고 왜 필요한가?

각 브로우저 마다 기본으로 설정된 스타일이 모두 다릅니다. 우리는 크로스 브라우징을 고려해서 개발을 해야 합니다. 쉽게 말하면 각 브라우저 플랫폼의 관계없이 우리가 원했던 스타일, 기능이 같이 움직이게 만들어야 합니다. 따라서 CSS reset을 사용해 스타일을 초기화 시켜 다양한 브라우저에서 같은 스타일이 적용되도록 설정을 해야 합니다.
React Hooks (useState) 키워드
왜 리액트팀은 useState가 위 방식으로 동작하도록 만들었을까?
React에서 업데이트된 상태는 비동기적 특성 때문에 즉시 반영되지 않고 리렌더링된 후에야 업데이트된 state가 반영되게 했다. 이유는 효율적으로 렌더링 하기 위해 여러 번의 상태값 변경 요청을 배치로 처리하기 때문입니다. 이처럼 불필요한 렌더링을 방지하기 위해 함수형 업데이트를 사용해 동기로 처리해 원하는 값을 추출하는 게 좋다.
React Hooks (useState) 키워드
Strict mode란 무엇일까?
https://ko.reactjs.org/docs/strict-mode.html#identifying-unsafe-lifecycles
React 라이프 사이클이란 무엇일까?
https://velog.io/@dea8307/React-라이프사이클Life-Cycle-이해
https://velog.io/@jinyoung985/React-함수형-컴포넌트의-생명주기-Life-Cycle
React에서 말하는 mount와 unmount란 무엇일까?
mount
컴포넌트가 새롭게 생성되는 시점 컴포넌트가 실행되고 나온 element 들이 가상 DOM에 삽입되고 실제 DOM 업데이트하기까지의 과정
unmount
해당하는 컴포넌트가 DOM 상에서 제거가 될 때 실행되는 라이프사이클
react-router-dom part 1 키워드
HTTP란 무엇일까?
HTTP란 서버와 클라이언트가 모델을 따라 데이터를 주고 받기 위한 프로토콜입니다 http는 암호화가 되는 않은 평문 데이터를 전송하기 때문에 보안에는 취약하는 단점이 있습니다.
HTTP / HTTPS 차이점
HTTP의 보안의 취약점을 보안하기 위해 등장한 HTTPS이며 SSL 인증서를 사용해 데이터를 암호화해서 보안을 증가시켰습니다 또한 보안에 안전해 방문률을 높혀주므로 SEO에 더 친화적입니다.
URI (URL, URN)
Uniform Resourece Locators의 약자로 사용자가 원하는 정보 자원을 찾기 위해서 해당 정보 자원의 위치와 종류를 파악해야할 때 사용하는 일련의 규칙이며 이 안에는 네트워크 상에 퍼져있는 특정 정보 자원의 종류와 위치가 기록되어 있다.
react-router-dom part 2 키워드
query parameter, query string, path variable 이란 각각 무엇인가?
https://velog.io/@jcinsh/Query-string-path-variable
https://velog.io/@newdana01/TIL-RESTful-API#4-path-parameter--query-parameter
```
