# React Interview Questions & Answers

1. ### What is ReactJS?

   _React_ is a popular JavaScript library for building user interfaces, particularly for single-page applications where you need a dynamic, responsive user experience. It was developed and is maintained by Facebook, and it allows developers to create large web applications that can update and render efficiently in response to data changes.

   #### Key Concepts of React

   1. **Components:**
      
      _Components_ are the building blocks of a React application. They are reusable pieces of code that define how a user interface should appear. Components can be either functional or class-based.
      - **Functional Components:** Simple JavaScript functions that return JSX (JavaScript XML) elements. They are often used for stateless components.
      - **Class Components:** ES6 classes that extend React.Component and have a render method to return JSX. They can hold local state and lifecycle methods.
   2. **JSX (JavaScript XML):**
      
      _JSX_ is a syntax extension that allows you to write HTML-like code within JavaScript. It makes it easier to create and visualize the structure of your UI.
      ```javascript
      const element = <h1>Hello, world!</h1>;
      ```
   3. **State:**
      
      _State_ is an object that holds data that may change over time. It is managed within a component and can be updated using the setState method in class components or the useState hook in functional components.

      - _Using `setState` in Class Components_

        ```javascript
        import React, { Component } from "react";

        class Counter extends Component {
          constructor(props) {
            super(props);
            this.state = {
              count: 0,
            };
          }

          increment = () => {
            this.setState((prevState) => ({
              count: prevState.count + 1,
            }));
          };

          render() {
            return (
              <div>
                <p>Count: {this.state.count}</p>
                <button onClick={this.increment}>Increment</button>
              </div>
            );
          }
        }

        export default Counter;
        ```

      - _Using `setState` in Class Components_

        ```javascript
        import React, { useState } from "react";

        const Counter = () => {
          const [count, setCount] = useState(0);

          const increment = () => {
            setCount((prevCount) => prevCount + 1);
          };

          return (
            <div>
              <p>Count: {count}</p>
              <button onClick={increment}>Increment</button>
            </div>
          );
        };

        export default Counter;
        ```
    4. **Props:**
        
        _Props_ (short for properties) are used to pass data from parent components to child components. They are read-only and allow you to customize and configure components.
        ```javascript
        function Welcome(props) {
            return <h1>Hello, {props.name}</h1>;
        }

        function App() {
            return <Welcome name="Alice" />;
        }
        ```
    5. **Lifecycle Methods:**
        
        _Lifecycle methods_ are special methods in class components that allow you to hook into different stages of a component's lifecycle, such as mounting, updating, and unmounting.
        ```javascript


