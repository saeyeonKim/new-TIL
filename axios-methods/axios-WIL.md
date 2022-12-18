```
Axios는 브라우저, Node.js를 위한 Promise API를 활용하는 HTTP 비동기 통신 라이브러리입니다.
쉽게 말해서 백엔드랑 프론트엔드랑 통신을 쉽게하기 위해 Ajax와 더불어 사용합니다.
axios 특징
운영 환경에 따라 브라우저의 XMLHttpRequest 객체 또는 Node.js의 http api 사용
Promise(ES6) API 사용
요청과 응답 데이터의 변형
HTTP 요청 취소
HTTP 요청과 응답을 JSON 형태로 자동 변경
Axios 사용해보기
형태
	axios.get(url,[,config])
GET : 입력한 url에 존재하는 자원에 요청을 합니다.

🤔 Get이 데이터를 받아오는 것이라고 했는데, 저는 로그인을 구현할때 GET을 사용했는데용?

GET으로 로그인을 구현했을때 웹 사이트 주소창의 형태를 잘 보면 이러한 형태가 나올 것입니다.

	www.yourserver.com/login?id=Hnk&pw=1234
    // 실제로 없는 사이트입니다! 이해를 돕기 위해서 추가했습니다.
웹 사이트 뒤에 쿼리스트링이 붙여진 것을 확인하실 수 있습니다.
✔ GET은 서버에서 어떤 데이터를 가져와서 보여준다거나 하는 용도이다. 주소에 있는 쿼리스트링을 활용해서 정보를 전달하는 것이지 GET메서드는 값이나 상태등을 바꿀 수 없습니다.



POST
형태
	axios.post("url주소",{
    	data객체
    },[,config])

✔새로운 리소스를 생성(create)할 때 사용합니다.

post 메서드의 두 번째 인자는 본문으로 보낼 데이터를 설정한 객체 리터럴을 전달합니다.

🤔 Post는 새로운 리소스를 생성할 때 사용되는데 그러면 언제 POST를 사용하나요?

✔ 로그인, 회원가입 등 사용자가 생성한 파일을 서버에다가 업로드할때 사용합니다. Post를 사용하면 주소창에 쿼리스트링이 남지 않기때문에 👍 GET보다 안전해요!



Delete
REST 기반 API 프로그램에서 데이터베이스에 저장되어 있는 내용을 삭제하는 목적으로 사용합니다.

형태
	axios.delete(URL,[,config]);
✅ Delete메서드는 HTML Form 태그에서 기본적으로 지원하는 HTTP 메서드가 아닙니다!

Delete메서드는 서버에 있는 데이터베이스의 내용을 삭제하는 것을 주 목적으로 하기에 두 번째 인자를 아예 전달하지 않습니다.

예제 코드
axios.delete("/thisisExample/list/30").then(function(response){
    console.log(response);
      }).catch(function(ex){
      throw new Error(ex)
}




PUT
REST 기반 API 프로그램에서 데이터베이스에 저장되어 있는 내용을 갱신하는 목적으로 사용됩니다.

형태
	axios.put(url[, data[, config]])
✅ PUT메서드는 HTML Form 태그에서 기본적으로 지원하는 HTTP 메서드가 아닙니다!

PUT메서드는 서버에 있는 데이터베이스의 내용을 변경하는 것을 주 목적으로 하고 있습니다.
```
