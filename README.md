# React_CheetSheet_2022 :rocket:

| Components  | npm |
| ------------- | ------------- | 
| [Create Component](#create-component) | [npm install](#npm-install)  |
| [Props](#props)                       |                              |
| [key](#key)                           |                              |

---
## [key](#key)

**key={item.link}**
```js
const listItem = data.map(item => <li key={item.link}><a href="{item.link}">{item.text}</a></li>)
```
---
## [props](#props)

### App.js
**headerData** oject data passed by _props_ from __App__ to __Header__ by attr. __data={headerData}__
```js
const headerData = {
  sitename: 'my test site name',
  second_header: 'Best and very cool',
  nav: [
    { "link": "nav1", "text": "my link 1" },
    { "link": "nav2", "text": "my link 2" },
    { "link": "nav3", "text": "my link 3" }
  ]
}

function App() {
  return (
    <>
        <header className="App-header">
          <Header data={headerData} />
        </header>
    </>
  );
}
export default App;
```
### Header.js
Из __App__ через _props_ (attr. data) в __Header__, далее из Header через _props_ (attr. nv) в __Nav__
```js
function Header(props) {
    return (
        <header>
            <h2>{props.data.sitename}</h2>
            <h4>{props.data.second_header}</h4>
            <Nav nv={props.data.nav} />
        </header>
    )
}

function Nav(props) {

    let data = props.nv
    const listItem = data.map(item => <li key={item.link}><a href="{item.link}">{item.text}</a></li>)
    return (
        <nav>
            <ul>
                {listItem}
            </ul>
        </nav>
    )
}
export default Header
```


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
