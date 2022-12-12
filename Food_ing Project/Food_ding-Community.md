# 오늘 작업한 HTML,CSS,STYLED-COMPONENT

```
import React from "react";
import styled from "styled-components";
import "./List.css";

const List = ({ title, imageUrl, body }) => {
  return (
    <Cardcontainer>
      <Imagecontainer>
        <img src={imageUrl} alt="" />
      </Imagecontainer>
      <Cardcontent>
        <Title>
          <h3>{title}</h3>
        </Title>
        <p style={{ wordBreak: "break-all" }}>{body}</p>
      </Cardcontent>
      <Btn>
        <Button>
          <Href>
            <a href="https://www.youtube.com/watch?v=Q3I_NwaCZI8">View more</a>
          </Href>
        </Button>
      </Btn>
    </Cardcontainer>
  );
};

const Cardcontainer = styled.div`
  width: 250px;
  height: 400px;
  box-shadow: 0px 0px 15px -5px;
  transition: 0.3s;
  animation: ease-in;
  &:hover {
    transform: scale(1, 1);
    box-shadow: 0px 0px 15px 0px;
  }
`;
const Imagecontainer = styled.div`
  overflow: hidden;
  height: 200px;
  width: 250px;
`;
const Cardcontent = styled.div`
  margin: 1rem;
  margin-top: 0.3rem;
`;
const Title = styled.div`
  color: #003881;
`;
const Btn = styled.div`
  display: flex;
  justify-content: center;
`;
const Button = styled.div`
  padding: 1rem;
  background-color: transparent;
  border: none;
  transition: 0.2s;
  margin-bottom: 0.5rem;
  border-radius: 3px;
  margin-top: -1rem;
  &:hover {
    background: rgba(114, 194, 255, 0.1);
    transform: scale();
  }
`;
const Href = styled.div`
  color: #003881;
`;

export default List;
```

CSS 너무 어렵다.. CLASSNAME으로 하는 것도 헷갈리는데 STYLED-COMPONENT로 하려니 더 헷갈려서 CSS파일 따로 만들어서 완성 후 다시 STYLED-COMPONENT로 만드는 중이다. 하지만 쉽지않다.. DIV안의 DIV에 STYLE을 주는 게 헷갈린다.
