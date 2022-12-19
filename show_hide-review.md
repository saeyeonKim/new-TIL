# show hide 기능

```
import React from "react';
import {useState} from "react";

const Myreview = () => {
    const [review, setReview] = useState("");

    const onChangeReview = (e) => {
        setReview(e.target.value);
    };

    return (
        <>
        <div>
          <input value = {review} onChange={onChangeReview} />
        </div>
        <div>
          <Reviewtext></Reviewtext>
          <Upbtns>
            <Upload>등록하기</Upload>
            <Upload>취소하기</Upload>
          </Upbtns>
        </div>
        </>
    );
};

export default Myreview;
```

위는 component에 따로 나눈 review.jsx 파일

```
// 원래 본문에 들어갔던 내용이 있던 자리에

{visible && <Myreview />}를 입력한다.
// visible이 true이면 review 컴포넌트가 보여짐.

그리고 위에
const [visible, setVisible] = useState(false);
를 입력한다.

import Myreview from "./Myinfo";
로 import 해주고 useState도 import 해준다.
```

위는 원래 app.jsx 파일
