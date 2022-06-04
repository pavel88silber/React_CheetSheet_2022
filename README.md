# React_CheetSheet_2022 :rocket:

| Components  | npm |
| ------------- | ------------- | 
| [Create Component](#create-component) | [npm install](#npm-install)
| hhhhhhhhhh| jjjjjjjjj |

---
## [npm install]
```
npm install express@4.16.1    // NPM: Install Specific Version of a Package
```


## [Create Component]
### with Class
```js
import React from "react";

class TestC extends React.Component {
    render() {
        return (
            <>
                <h3>Test, class component</h3>
            </>
        )
    }
}


export default TestC
```
### with Function
```js
function Test() {
    return (
        <>
            <h4>Test - functional component</h4>
        </>
    )
}

export default Test
```

---


## Create React App
```js
// create-react-app global installation
npm i -g create-react-app

// create app
create-react-app myapp                  // npx create-react-app

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
