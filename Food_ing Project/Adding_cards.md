# post에서 새로 입력할때마다 card 추가하기

```
import styled from "styled-components";
import List from "../components/list/List";
import { Link } from "react-router-dom";
import React, { useState, useEffect } from "react";
import axios from "axios";

const RecipeList = () => {
  const [recipes, setRecipes] = useState([]);
  console.log(recipes);

  const fetchRecipes = async () => {
    const { data } = await axios.get("http://localhost:3005/recipes");
    setRecipes(data);
  };

  useEffect(() => {
    fetchRecipes();
  }, []);

  // (9-20)은 db.json에서 데이터 받아오는 코드. (11)에 console 찍으면 db.json에 있는 데이터가 나옴. fetchRecipes에 axios를 이용해서 setRecipes로 recipes에 데이터를 가져온다.


  return (
    <div>
      <Wrapimg>
        <Title>
          <h1> Recipe Community</h1>
        </Title>
        <Nbutton>
          <Link to={`/board`}>
            <Newbutton>new Post</Newbutton>
          </Link>
        </Nbutton>

        <Card>
          {recipes.map((recipe) => (
            <List recipelist={recipe} />
          ))}
        </Card>
        // recipes에 map을 돌려서 recipe에 recipelist는 recipe를 넣는다.
      </Wrapimg>
    </div>
  );
};
```

```
import styled from "styled-components";
import "./List.css";
import { Link } from "react-router-dom";

const List = ({ recipelist }) => {
  //const { title, imgurl, recipe } = recipelist;
  //위에서 recipelist를 안에 title, imgurl, recipe가 있다고 선언하여 List를 정의한다.
  //이 List는 card의 내용.

  return (
    <Cardcontainer>
      <div>
        <Imagecontainer src={imgurl} alt="" />
      </div>
      <Cardcontent>
        <Title>
          <h3>{title}</h3>
        </Title>
        <Body>
          <Text style={{ wordBreak: "break-all" }}>{recipe}</Text>
        </Body>
      </Cardcontent>
      <Btn>
        <Stbutton>
          <Link to={`/listsx`}>View more</Link>
        </Stbutton>
      </Btn>
    </Cardcontainer>
  );
};
```
