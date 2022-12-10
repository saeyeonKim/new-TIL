# Axios Get방식 연습

```
// src/App.js

import React, { useEffect, useState } from "react";
import axios from "axios"; // axios import 합니다.

const App = () => {
  const [todos, setTodos] = useState(null);

  // axios를 통해서 get 요청을 하는 함수를 생성합니다.
  // 비동기처리를 해야하므로 async/await 구문을 통해서 처리합니다.
  const fetchTodos = async () => {
    const { data } = await axios.get("http://localhost:3001/todos");
    //axios의 GETmethod 사용하려면 인자로는 url과 config를 받으면 된다.
    //12번은 config를 설정하지 않은 상태
    //axios config 공식문서 url = "https://axios-http.com/kr/docs/req_config"
    //JSON-server 공식문서 url = "https://www.npmjs.com/package/json-server"
    // axios는 Promise 기반으로 하는데 이 때문에 async, await를 통해서 비동기처리를 한다.

    setTodos(data); // 서버로부터 fetching한 데이터를 useState의 state로 set 합니다.
  };
  // JSONserver에 있는 todos 데이터를 가지고 와서 setTodos해서 todos에 넣겠다(11-18)

  // 생성한 함수를 컴포넌트가 mount 됐을 떄 실행하기 위해 useEffect를 사용합니다.
  useEffect(() => {
    // effect 구문에 생성한 함수를 넣어 실행합니다.
    fetchTodos();
  }, []);
  // fetchTodos는 axios의 GETmethod를 이용해서 3001번에 todos JSON 서버에 있는 값을 불러온다.
  // 그 받아온 데이터를 useState의 setState를 이용해서 업데이트를 해주고 있다.

  // data fetching이 정상적으로 되었는지 콘솔을 통해 확인합니다.
  console.log(todos); // App.js:16
  return <div>App</div>;
};

export default App;


// json server 추가 : yarn add json-server
// json server 실행 : yarn json-server --watch db.json --port 3001
```
