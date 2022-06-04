# React_CheetSheet_2022 :rocket:

## Create React App
```js
// create-react-app global installation
npm i -g create-react-app

// create app
create-react-app myapp

// start app
npm start


```



## old version react 16.3.2
```js
import React from "react";
import ReactDom from "react-dom";

function TodoItem() {
  return <span>Drink Koncha</span>;
}

function TodoList() {
  return (
    <ul>
      <li>
        <TodoItem />
      </li>
      <li>
        <TodoItem />
      </li>
      <li>
        <TodoItem />
      </li>
    </ul>
  );
}

ReactDom.render(<TodoList />, document.getElementById("root"));
```
