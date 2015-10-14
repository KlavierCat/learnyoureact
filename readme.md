# Notes for React

### Lesson 1
Installing required modules:
<br/>
```
$ npm install express body-parser express-react-views node-jsx
```

### Lesson 2 - React components
ReactClass & domElement
  ```js
  var ReactClass = React.createClass({
    render: function() {
      return (
        //<myHtmlElement></myHtmlElement>
        //<MyReactComponent />
      );
    }
  });
  ```

### Lesson 3 - props
Passing properties from parents to children
```js
  <td style={{border: "1px solid black"}}{this.props.title}</td>
  <td style={{border: "1px solid black"}}{this.props.children}</td>
```
