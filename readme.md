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

### Lesson 4 - propTypes
Validate that components are passed with all needed properties by:
```propTypes``` and ```React.PropTypes```. Example:
```js
React.createClass({
  propTypes: {
    name: React.PropTypes.string.isRequired,
    id: React.PropTypes.number.isRequired,
    alt: React.PropTypes.string
  },
  /* ... */
);
```

### Lesson 5 - state
Define mutable values with ```this.state```, which is private to each component.
Change state by using ```this.setState```.
<br/>
https://facebook.github.io/react/docs/component-api.html
https://facebook.github.io/react/docs/component-specs.html

### Lesson 6 - css
Define style as variable:
```js
var style = {
  tableContent: {
    border: "1px solid black"
  }
};
```
```html
<td style={style.tableContent}>
```
https://facebook.github.io/react/tips/inline-styles.html

### Lesson 7 - Props from Server
React makes use of a ```key``` attribute to keep track of each component in the VirtualDOM. This allows it to update the real DOM as sensibly and infrequently as possible.
```html
<TodoList data = {this.props.data} />
```
```js
var todo = this.props.data.map(function(obj) {
  return <Todo title={obj.title} key={obj.title}>{obj.detail}</Todo>
});
```
