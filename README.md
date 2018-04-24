# FrontEnd
## Penn SD4x
### W1
- CSS Notes
  - [It's all about boxes](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/CSS_basics#Boxes_boxes_it's_all_about_boxes)
    - Read [this](https://developer.mozilla.org/en-US/docs/Learn/CSS)
    - Do excercises [here](https://www.w3schools.com/css/default.asp)
  - Element Selector
    - e.g. h1 { color:red; } <br>
        All h1 elements
  - Class selector
    - e.g. .address { ... } <br>
        All elements in class “address”
  - id selector
    - e.g. #section1 { ... } <br>
        Unique element with ID “section1”
- [MY WORK: **HW1 calendar**](https://codepen.io/l1n4n/pen/KRwovy/)
### W2
- js basics
  - for in [vs](https://www.typescriptlang.org/docs/handbook/iterators-and-generators.html) for of
    - for in: 
        - iterates and list out all the keys.
        - operates on any object; it serves as a way to inspect properties on this object.
    - for of: 
        - iterates and returns a list of values
        - values of iterable objects
  - [isNaN()](https://www.w3schools.com/jsref/jsref_isnan.asp); [Number()](https://www.w3schools.com/jsref/jsref_number.asp)
  - Array methods
    - [splice](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/splice)
- jQuery
  - core syntax<br>
  `$(selector).action(function)`
  - [selector](https://www.w3schools.com/jquery/jquery_selectors.asp) 
- [MY WORK: **HW3 calculator**](https://codepen.io/l1n4n/pen/NMGzao)
### W3
- [React](https://reactjs.org/)
  - An **element** describes what you want to see on the screen (like a single frame in a movie)
  - To **render** a React element into a root DOM node, pass both to ReactDOM.render()<br>
  ```
  const element = <h1>Hello, world</h1>;
  ReactDOM.render(element, document.getElementById('root'));
  ```
  - **Updating** the UI: create a new element, and pass it to ReactDOM.render()
  - **components** are like JavaScript functions: inputs----“props”; putputs----React elements describing what should appear on the screen.
  - 2 ways to define a component
    1. write a js function<br>
    ```javascript
    function Welcome(props) {
      return <h1>Hello, {props.name}</h1>;
    }
    ```
    2. Extends React.Component<br>
    ```javascript
    class Welcome extends React.Component {
      render() {
        return <h1>Hello, {this.props.name}</h1>;
      }
    }
    ```
  - elements can also represent user-defined components
  ```javascript
  function Welcome(props) {              //component accepting "props"(parameters) in this form: [name="xxx"]
    return <h1>Hello, {props.name}</h1>;  // return jsx --> html with tag<h1>
  }
  const element = <Welcome name="sara"/> // element representing the former component with its props(property name) as "sara"
  ReactDOM.render(
    element,                             //calls the Welcome component as the "props"
    document.getElementById('root')      //update the DOM
  );
  ```
  - syntax `ReactDOM.render(<ComponentName props1 parameter="argument" || parameter={const.argument} props2 props3 />`
  - **props** like the NAME of a class, its attributes are accessed by `.parameter`, props are immutable, like you do not change a class's name after defining it
  - **state** can change-------this.props.attribute cannot change, but this.state.attribute can be changed
    - define a component by `.extend React.Component`
    - define this.state={parameter: data} within `constructor(props)`
    - refer as `this.state.parameter`
    - change state by `this.setState()`
- Event listener
  - a common pattern is for an event handler to be **a method on the class**.
  - must `bind(this)`
  - common structure
  ```javascript
  class Name extends React.Component {
    constructor(props) {
      super(props);
      this.state = {parameter: data};
      
      this.method = this.method.bind(this);
    }
    
    method() {
      this.setState({paramter: newdata});
    }
    
    render() {
      return (
        <tag method-do-stuff-to-state-according-to-event /tag>
        );
    }
  }
  ReactDOM.render(
    <Name />,
    document.getElementById('root')
  );
  ```
- [MY WORK: **HW4 fontchanger**](https://codepen.io/l1n4n/pen/aGdPwQ?editors=1010)
## [IT](http://www.jnshu.com/)
- [task 1](http://www.jnshu.com/task/1/33/detail//#0)
  - [Two solutions](https://codepen.io/l1n4n/pen/BxaaKR)
- [task 2](http://www.jnshu.com/task/1/34/detail//#0)
