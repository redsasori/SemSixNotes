## 1)targetting a DOM element using useRef?

To target a DOM element and access its values using the `useRef` hook in React, follow these steps:

1. Import the `useRef` hook from React.
2. Create a `useRef` instance with an initial value.
3. Attach the `useRef` instance to the DOM element using the `ref` attribute.
4. Access the DOM element's value using the `current` property of the `useRef` instance.

Here's an example of how to focus on an input field when a button is clicked:

```javascript
import React, { useRef } from 'react';

function MyForm() {
  const inputRef = useRef(null);

  const handleClick = () => {
    inputRef.current.focus();
  };

  return (
    <div>
      <input type="text" ref={inputRef} />
      <button onClick={handleClick}>Focus Input</button>
    </div>
  );
}
```

In this example, `inputRef` is created using the `useRef` hook with an initial value of `null`. The `inputRef` is then attached to the input field using the `ref` attribute. When the button is clicked, the `handleClick` function is called, which focuses on the input field by accessing its DOM element using the `current` property of the `inputRef`.

For managing previous values, you can use `useRef` in combination with `useState`:

```javascript
import React, { useState, useRef } from 'react';

function MyComponent() {
  const [a,b] = useState('');
  const previousValueRef = useRef('');

  const handleChange = (event) => {
    previousValueRef.current = a;
    b(event.target.value);
  };

  return (
    <div>
      <input value={a} onChange={handleChange} />
      <p>Previous Value: {previousValueRef.current}</p>
    </div>
  );
}
```

In this example, `previousValueRef` is created using the `useRef` hook with an initial value of an empty string. The `handleChange` function updates the `previousValueRef` with the current value before updating the state with the new value. This way, you can keep track of the previous value of the input field.


## 2)How shift and unshift works in Array?

In ReactJS, the `shift()` and `unshift()` methods are used to manipulate arrays just like in JavaScript. They are not specific to ReactJS, but they can be used in React components to modify the state of an array.The `shift()` method removes the first element from the original array and returns that removed element. This operation modifies the original array, and the updated array is reflected in the component's state. Here's an example of using `shift()` in a React component:

**shift() Syntax:**
let fruits = ['Apple', 'Orange', 'Mango'] 
fruits.shift()
OP:['Orange', 'Mango']

**unshift() Syntax:**
fruits.unshift('Date', 'Melon') 
OP:['Date', 'Melon', 'Orange', 'Mango']

## 3)Explain  removing and adding elements in Array using splice() method.

In ReactJS, the `splice()` method can be used to add or remove elements from an array. This method changes the original array and returns the removed elements (if any). Here’s a brief explanation:

**Removing Elements:** The `splice()` method can remove elements from an array by specifying the index from where elements need to be removed and the number of elements to remove.

```javascript
let array = [1, 2, 3, 4, 5];
let indexToRemove = 2;
let numberOfElementsToRemove = 1;

array.splice(indexToRemove, numberOfElementsToRemove);
// array is now [1, 2, 4, 5]
```

**Adding Elements:** The `splice()` method can also add elements to an array by specifying the index where new elements should be added, 0 as the number of elements to remove, and the new elements.

```javascript
let array = [1, 2, 4, 5];
let indexToAdd = 2;
let numberOfElementsToRemove = 0;
let elementsToAdd = [3];

array.splice(indexToAdd, numberOfElementsToRemove, ...elementsToAdd);
// array is now [1, 2, 3, 4, 5]
```

In ReactJS, state should not be mutated directly. So, create a copy of the state array before using `splice()`. This can be done using the `slice()` method or the spread operator (`...`).

```javascript
let arrayCopy = [...this.state.array];
```

Then, use `setState()` to update the state with the modified copy of the array.

```javascript
this.setState({ array: arrayCopy });
```

This ensures that React’s state is updated correctly, and the component re-renders as expected.

## 4)Explain every() and some() method of Array.

In JavaScript, which is used in ReactJS, the `every()` and `some()` methods are commonly used for checking conditions across all elements or at least one element in an array, respectively.

**every():** The `every()` method tests whether all elements in the array pass the test implemented by the provided function. It returns a Boolean value.

```javascript
let array = [1, 2, 3, 4, 5];
let allGreaterThanZero = array.every(num => num > 0);
// allGreaterThanZero is true
```

In this example, `every()` checks if all numbers in the array are greater than zero.

**some():** The `some()` method tests whether at least one element in the array passes the test implemented by the provided function. It returns a Boolean value.

```javascript
let array = [1, 2, 3, 4, 5];
let someGreaterThanThree = array.some(num => num > 3);
// someGreaterThanThree is true
```

In this example, `some()` checks if at least one number in the array is greater than three.

In ReactJS, these methods can be used in the render method or other lifecycle methods to manipulate state or props data. However, they should not be used to directly mutate state. Always use `setState()` when you need to update the state based on the result of these methods.

## 5)How to programaticallly navigate to different routes in ReactJS using useNavigate().

In ReactJS, the `useNavigate` hook from the `react-router-dom` library allows you to programmatically navigate to different routes. Here’s how you can use it:

```jsx
import { useNavigate } from 'react-router-dom';

function Component() {
  // Get the navigate function
  const navigate = useNavigate();

  // Use navigate to change routes
  const goToHomePage = () => {
    navigate('/home');
  };

  return (
    <button onClick={goToHomePage}>
      Go to Home Page
    </button>
  );
}
```

- `useNavigate()` is a hook from the `react-router-dom` library in ReactJS.
- It allows for programmatic navigation between different routes in a React application.
- You can use it to navigate to different routes based on user interaction or conditional logic.
- It works seamlessly with the rest of the `react-router-dom` library and your routing setup.
- It can only be used within components that are children of a `Routes` component.
- It’s essential for building dynamic and interactive web applications with React.
- Note: `useNavigate()` is available in React Router v6 or above. For older versions, you might need to use the `history` object.

## 6)Explain the purpose and usage of useEffect() hook in reactjs focusing mainly on dependency array

The `useEffect()` hook in ReactJS is a built-in hook that allows you to perform side effects in function components. Side effects could be data fetching, subscriptions, or manually changing the DOM, etc.

Here’s a basic usage of `useEffect()`:

```jsx
useEffect(() => {
  // Side effect goes here
}, [dependency1, dependency2]);
```

The `useEffect` hook takes two arguments:

1. **Effect callback function**: This is a function where you put the side effect code. This function runs after every render, including the first render.
2. **Dependency array**: This is an optional array of dependencies for your effect. The effect will only re-run if the values in this array change between renders. If you don’t provide an array, the effect runs after every render. If you provide an empty array (`[]`), the effect only runs once after the initial render, similar to `componentDidMount` in class components.

The dependency array is a powerful tool for optimizing your effects. By precisely specifying when your effect should re-run, you can avoid unnecessary work and make your component more efficient.

For example, if you have an effect that fetches user data based on a `userId`, you might write it like this:

```jsx
useEffect(() => {
  fetchUserData(userId);
}, [userId]); // Re-run the effect when `userId` changes
```

In this case, the effect re-runs whenever `userId` changes, ensuring that you always have the correct user data. But if `userId` stays the same between renders, the effect doesn’t run, saving you a potentially expensive network request.

`useEffect()` is a versatile hook for managing side effects in your React components, and the dependency array is a key part of controlling and optimizing these effects.

## 7)Demonstrate the use of useContext hook in reactjs

The `useContext` hook in ReactJS is used to create global state for your application and avoid prop drilling. Here’s a simple example of how you can use it:

First, you need to create a context:

```jsx
import React, { createContext, useContext } from 'react';

// Create a Context object
const MyContext = createContext();
```

Next, you can provide the context to your components:

```jsx
function App() {
  return (
    <MyContext.Provider value="Hello, world!">
      <ChildComponent />
    </MyContext.Provider>
  );
}
```

In this example, any child components of `App` can now access the value “Hello, world!” through `MyContext`.

Finally, you can use `useContext` in a child component to access the context value:

```jsx
function ChildComponent() {
  const value = useContext(MyContext);
  
  return <p>{value}</p>; // Outputs: "Hello, world!"
}
```

In this `ChildComponent`, we call `useContext` and pass in `MyContext`. This returns the current context value, which is “Hello, world!”. We then render this value in a paragraph element.

`useContext` will only return the current context value, or the default value if there’s no matching Provider up the tree. It will not trigger a re-render when the context value changes, for that you might want to use a state management library or React’s built-in `useReducer` hook.

This is a fundamental concept in managing global state in React, and it’s particularly useful for passing down data to deeply nested components.

## 8)iilustrate the concept of useImperativeHandle() hook in reactjs

Parent Component ->useRef() ->Child Component ->useImperativeHandle() ->Expose Functions ->Parent uses functions

Sure, here’s the theoretical explanation of the `useImperativeHandle()` hook in ReactJS:

The `useImperativeHandle()` hook is a built-in hook in React that allows you to customize the instance value that is exposed to parent components when using `ref`. This is particularly useful when you need to expose specific properties and methods of a child component to a parent component.

Here are the key points you need to understand:

1. **Customizing Refs**: Normally, when you use `ref` on a component, it exposes the entire component instance. However, with `useImperativeHandle`, you can choose what properties and methods get exposed to parent components. This gives you more control over how child components interact with their parents.
    
2. **Syntax**: The `useImperativeHandle()` hook takes two parameters: `ref` and a function. The function returns an object containing the properties and methods that you want to expose. Here’s the basic syntax:
    
    ```jsx
    useImperativeHandle(ref, () => ({
      method1: () => {},
      method2: () => {},
      // ...
    }));
    ```
    
3. **Usage with forwardRef**: `useImperativeHandle` is often used in conjunction with `forwardRef`. `forwardRef` is a technique in React for passing `ref` down to a child component. This is necessary because `ref` is not a normal prop, so it can’t be passed in the usual way.
    
4. **Use Cases**: `useImperativeHandle` should be used sparingly. It’s often better to lift state up to parent components or use other communication methods instead of relying on imperative methods. However, there are cases where `useImperativeHandle` can be useful, such as focusing on inputs, triggering animations, or managing media playback.

## 9)Compare link and navlink with an example

`Link` and `NavLink` are both components provided by the `react-router-dom` library in ReactJS for creating navigational links in your application. Here’s a comparison of the two:

1. **Link Component**: The `Link` component is used to create basic navigational links. It renders an anchor tag (`<a>`) in the DOM and takes a `to` prop, which tells it where to navigate when the link is clicked.

```jsx
import { Link } from 'react-router-dom';

<Link to="/about">About</Link>
```

In this example, clicking on “About” will navigate to the “/about” route.

2. **NavLink Component**: The `NavLink` component is a special type of `Link` that can be “active” or “inactive” based on the current route. It takes an additional `activeClassName` prop, which applies a CSS class to the link when it’s active (i.e., when the current route matches the `to` prop).

```jsx
import { NavLink } from 'react-router-dom';

<NavLink to="/about" activeClassName="active-link">About</NavLink>
```

The “active-link” class is applied to the link when the current route is “/about”. This allows you to style active links differently (e.g., highlight the current page in your navigation menu).

While both `Link` and `NavLink` can be used to create navigational links, `NavLink` provides additional functionality for styling active links. You would typically use `Link` for regular links and `NavLink` for your navigation menu

## 11) forwardRef use and useImperativeHandle

**React.forwardRef**
`React.forwardRef` is a method in React that allows you to pass a `ref` from a parent component down to a child component. This is useful when you need to access a child’s DOM node directly from a parent component.

```jsx
import React, { forwardRef } from 'react';

const MyComponent = forwardRef((props, ref) => (
  <button ref={ref}>Click me</button>
));

// Usage
const App = () => {
  const myRef = React.createRef();

  return <MyComponent ref={myRef} />;
};
```

In this example, `MyComponent` is a functional component that takes `props` and `ref` as arguments. The `ref` is then attached to the `button` element. When `MyComponent` is used in `App`, a `ref` created by `React.createRef()` is passed to it. This `ref` can now be used in `App` to access the `button` DOM node directly.

**React.useImperativeHandle**
`React.useImperativeHandle` is a hook in React that allows you to customize the instance value that is exposed to parent components when using `ref`. This is useful when you want to expose specific properties or methods to a parent component.

```jsx
import React, { forwardRef, useRef, useImperativeHandle } from 'react';

const MyComponent = forwardRef((props, ref) => {
  const inputRef = useRef();

  useImperativeHandle(ref, () => ({
    focus: () => {
      inputRef.current.focus();
    }
  }));

  return <input ref={inputRef} />;
});

// Usage
const App = () => {
  const myRef = React.createRef();

  return (
    <div>
      <MyComponent ref={myRef} />
      <button onClick={() => myRef.current.focus()}>
        Focus the input
      </button>
    </div>
  );
};
```

In this example, `MyComponent` uses `useImperativeHandle` to expose a `focus` method to the parent component. This `focus` method focuses the `input` element. When the button in `App` is clicked, the `focus` method is called via the `ref`, focusing the `input` element.

Remember, `useImperativeHandle` should be used sparingly as it breaks the usual flow of data down the component tree. It’s best to fully understand its implications before using it in your code.

## 12) Make use of asynchronous JS and async-await syntax in example.


```js
import React, { useState, useEffect } from 'react';

function FdataComp() {
  const [post, setPost] = useState({});

  useEffect(() => {
     const fetchData = async () => {
      const response = await   fetch('https://jsonplaceholder.typicode.com/posts/1');
      const data = await response.json();
      setPost(data);
    };

    fetchData();
  }, []);

  return (
    <div>
      <h3>{post.title}</h3>
      <p>{post.body}</p>
    </div>
  );
}

export default FdataComp;

```

**Asynchronous JavaScript and Fetch API:**

Asynchronous JavaScript allows you to perform tasks that can take some time to complete, such as fetching data from an API, without blocking the rest of your code. This is crucial in JavaScript, which is single-threaded, to prevent your application from becoming unresponsive.

**Async/Await Syntax:**

`async` and `await` are syntactic sugar for working with Promises in a more readable and logical way. An `async` function returns a Promise, and the `await` keyword can only be used inside an `async` function. `await` pauses the execution of the `async` function until the Promise is resolved or rejected.

**React and Fetching Data:**

In React, data fetching is typically done in the `useEffect` hook. This hook runs after the first render and after every update (unless you provide a dependency array), making it a good place to put data fetching logic.

When you fetch data in a React component, you usually store this data in the component’s state using the `useState` hook. This allows the component to re-render when the data is received.

1. Initialize state for the data using the `useState` hook.
2. Use the `useEffect` hook to fetch data when the component mounts.
3. Inside the `useEffect` hook, declare an `async` function for the fetch operation.
4. Call the fetch API with the desired URL inside the `async` function.
5. Use the `await` keyword to pause execution of your function until the fetch operation completes. The fetch API returns a Promise that resolves to the Response object.
6. Call the `json` method on the Response object to parse the body text as JSON. This also returns a Promise, so use `await` again.
7. Once the data is parsed, call the state setter function returned by `useState` to update your component’s state with the fetched data.
8. Handle any errors that may occur during the fetch operation with a `catch` block.

## 13) Keyboard & Window events explaination with 2 examples 

**Keyboard Events in React:**

Keyboard events are triggered when the user interacts with the keyboard. In React, you can handle keyboard events such as `onKeyDown`, `onKeyPress`, and `onKeyUp`.

- `onKeyDown`: This event is fired when a key is pressed down.
- `onKeyPress`: This event is fired when a key is pressed and released.
- `onKeyUp`: This event is fired when a key is released.

Example: Handling `onKeyDown` event

```jsx
function InputComponent() {
  const handleKeyDown = (event) => {
    console.log(`Key pressed: ${event.key}`);
  };

  return <input onKeyDown={handleKeyDown} />;
}
```

In this example, we have an input field that listens for the `onKeyDown` event. When a key is pressed, the `handleKeyDown` function is called, and it logs the pressed key to the console.

**Window Events in React:**

Window events are triggered by the window object. Some common window events include `resize`, `scroll`, `load`, etc. In React, you can use the `useEffect` hook to add event listeners to the window object.

Example: Handling window `resize` event

```jsx
import React, { useEffect } from 'react';

function ResizeComponent() {
  useEffect(() => {
    const handleResize = () => {
      console.log(`Window width: ${window.innerWidth}`);
    };

    window.addEventListener('resize', handleResize);

    // Cleanup
    return () => {
      window.removeEventListener('resize', handleResize);
    };
  }, []);

  return <div>Resize the window</div>;
}￼

```

In this example, we have a component that listens for the window `resize` event. When the window is resized, the `handleResize` function is called, and it logs the new window width to the console. The event listener is added when the component mounts and removed when the component unmounts to prevent memory leaks.

Remember, when working with events in React, it’s important to understand the concept of synthetic events. React wraps the browser’s native event system with its own event system, called synthetic events, for performance and cross-browser compatibility reasons.

## 14)Give the importance of useState() & useReducer() hook in reactJS

**useState Hook:**

`useState` is a built-in hook in React that allows you to add state to your functional components. It returns a pair: the current state value and a function that lets you update it.

The importance of `useState` lies in its ability to enable state management in functional components, which was previously only possible in class components. This makes your components more readable and easier to test.

Example of `useState`:

```jsx
import React, { useState } from 'react';

function Counter() {
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>
        Click me
      </button>
    </div>
  );
}
```

**useReducer Hook:**

`useReducer` is another built-in hook in React that is usually preferable to `useState` when you have complex state logic that involves multiple sub-values or when the next state depends on the previous one. It also lets you optimize performance for components that trigger deep updates because you can pass dispatch down instead of callbacks.

The importance of `useReducer` lies in its ability to handle more complex state logic in a more organized and predictable way, similar to how Redux works.

Example of `useReducer`:

```jsx
import React, { useReducer } from 'react';

const initialState = {count: 0};

function reducer(state, action) {
  switch (action.type) {
    case 'increment':
      return {count: state.count + 1};
    case 'decrement':
      return {count: state.count - 1};
    default:
      throw new Error();
  }
}

function Counter() {
  const [state, dispatch] = useReducer(reducer, initialState);

  return (
    <div>
      Count: {state.count}
      <button onClick={() => dispatch({type: 'increment'})}>+</button>
      <button onClick={() => dispatch({type: 'decrement'})}>-</button>
    </div>
  );
}
```

In conclusion, both `useState` and `useReducer` are essential hooks in React that allow you to manage state in your functional components. The choice between `useState` and `useReducer` depends on the complexity of the state you’re dealing with

## 15)BrowserRouter in reactJS with example

**BrowserRouter in React:**

`BrowserRouter` is a component provided by React Router that uses the HTML5 history API to keep your user interface in sync with the URL¹². It creates a browser history that uses clean URLs (i.e., URLs without the `#` hash symbol) and listens for changes in the current location that are pushed onto the stack¹.

Here are some key features of `BrowserRouter`:

- **Declarative routing**: With `BrowserRouter`, you define your routes using JSX syntax². This makes your routing logic more readable and easier to understand.
- **HTML5 history API**: `BrowserRouter` uses the HTML5 history API (pushState, replaceState, and the popstate event) to keep your UI in sync with the URL². This allows for forward and backward navigation that aligns with the user's expectations of how the browser should behave.
- **Clean URLs**: Unlike `HashRouter`, which uses in-page anchors (i.e., hashes), `BrowserRouter` uses the HTML5 history API to manipulate the browser history programmatically¹. This results in clean, readable URLs.

Here's a simple example of how to use `BrowserRouter`:

```jsx
import React from 'react';
import { BrowserRouter as Router, Route } from 'react-router-dom';
import HomePage from './HomePage';
import AboutPage from './AboutPage';

function App() {
  return (
    <Router>
      <Route exact path="/" component={HomePage} />
      <Route path="/about" component={AboutPage} />
    </Router>
  );
}

export default App;
```

In this example, `BrowserRouter` (aliased as `Router`) is used as the root component, and `Route` components are used to define the application's routes. When the URL matches the `path` prop of a `Route`, the corresponding component is rendered

# 16)Effectiveness of Navlink over Link

**Link and NavLink in React Router:**

In a single-page application (SPA) like those built with React, routing is a key aspect. Routing refers to how an application’s endpoints (URIs) respond to client requests. For an SPA, this means controlling the navigation among views and sharing URLs for users to bookmark and share.

React Router is a standard library for routing in React. It keeps your UI in sync with the URL. It has a simple API with powerful features like lazy code loading, dynamic route matching, and location transition handling built right in.

**Link Component:**

The `Link` component is used to create links in your application. It’s equivalent to using anchor tags in HTML, but it works within the context of React Router. When a `Link` is clicked, the URL updates and the component that corresponds to the new URL is rendered. This happens without a server request, providing a smooth user experience.

**NavLink Component:**

`NavLink` is a special type of `Link` that can be styled based on whether it matches the current URL. This is particularly useful for navigation menus, where you want to highlight the currently active page. `NavLink` includes `style` and `activeClassName` props to apply styles to the active link.

**Effectiveness of NavLink over Link:**

While `Link` provides basic navigation functionality, `NavLink` goes a step further by allowing you to style the active link. This can improve user experience by providing visual feedback about the current location in the application.

However, if you just need a simple link without any active styling, using `Link` would be more straightforward. Therefore, the choice between `Link` and `NavLink` depends on the specific needs of your application.

In conclusion, both `Link` and `NavLink` are essential components in React Router that allow you to manage navigation in your React application. They enable you to build single-page applications with multiple views that can be bookmarked and shared, all while maintaining a smooth user experience

## 17)Window-Resize and Keyboard event in ReactJS

**Window Resize Event in React:**

In React, there isn't a built-in event for window resizing. However, we can use the native `resize` event provided by web browsers⁶. This event fires when the window has been resized⁸. 

To listen for this event, we can use the `addEventListener` method on the `window` object inside a `useEffect` hook⁶. When the component mounts, the event listener is added. When the component unmounts, the event listener should be removed to prevent memory leaks⁶.

Here's an example of how to use the window resize event in React:

```jsx
import React, { useState, useLayoutEffect } from 'react';

function App() {
  const [windowSize, setWindowSize] = useState([0, 0]);

  useLayoutEffect(() => {
    function updateWindowSize() {
      setWindowSize([window.innerWidth, window.innerHeight]);
    }
    window.addEventListener('resize', updateWindowSize);
    updateWindowSize();

    return () => window.removeEventListener('resize', updateWindowSize);
  }, []);

  return (
    <div>
      Window width: {windowSize[0]}, height: {windowSize[1]}
    </div>
  );
}
```

In this example, we're using a custom hook to store window dimensions as state values. Therefore, state values will update whenever window size changes, triggering a re-render⁶.

**Keyboard Events in React:**

Keyboard events are triggered when the user interacts with the keyboard. In React, you can handle keyboard events such as `onKeyDown`, `onKeyPress`, and `onKeyUp`⁴.

- `onKeyDown`: This event is fired when a key is pressed down⁴.
- `onKeyPress`: This event is fired when a key is pressed and released¹.
- `onKeyUp`: This event is fired when a key is released⁴.

Here's an example of how to use the `onKeyPress` event in React:

```jsx
import React from 'react';

function InputComponent() {
  const handleKeyPress = (event) => {
    if(event.key === 'Enter'){
      console.log('Enter key pressed');
    }
  };

  return <input type="text" onKeyPress={handleKeyPress} />;
}
```

In this example, we have an input field that listens for the `onKeyPress` event. When the 'Enter' key is pressed, the `handleKeyPress` function is called, and it logs a message to the console¹


## 18)Scenario useRef hook for parent child component interaction in ReactJS & explain its implementation.

**useRef Hook in React:**

`useRef` is a built-in hook in React that allows you to create a ‘ref’ to a DOM element or an instance of a component. Refs are used in React to access the properties of an element or component, manipulate the element, or to persist values across re-renders.

Unlike state variables, refs do not cause a component to re-render when they change. This makes them useful for values that need to persist across renders but do not affect rendering.

**Parent-Child Interaction using useRef:**

In React, data flows down from parent to child via props. However, there are cases where the parent needs to interact with the child directly. This is where `useRef` comes in handy.

The parent can create a ref using `useRef`, and attach it to the child component. The child component can then expose some methods using `useImperativeHandle`, which the parent can call using the ref.

This pattern is known as “imperative methods” and is typically used for actions that a parent component might need to trigger in a child component, such as focusing an input, playing a video, or triggering animations.

```jsx
import React, { useRef, useImperativeHandle, forwardRef } from 'react';

const ChildComponent = forwardRef((props, ref) => {
  useImperativeHandle(ref, () => ({
    sayHello() {
      console.log('Hello from the child component!');
    }
  }));

  return <div>Child Component</div>;
});

function ParentComponent() {
  const childRef = useRef();

  const onClick = () => {
    childRef.current.sayHello();
  };

  return (
    <div>
      <ChildComponent ref={childRef} />
      <button onClick={onClick}>Call Child Method</button>
    </div>
  );
}

export default ParentComponent;
```

## 19)Discuss Params and UseParams in Reactjs with example

**Params in React Router:**

In React Router, parameters are variables that are part of the URL. They are denoted by a colon `:` followed by the parameter name in the path of a `Route`¹. Parameters allow for creating dynamic routes where some portion of the route can change¹. These changing parts of the route are the parameters¹.

For example, in a route defined as `/users/:id`, `:id` is a parameter. This route can match `/users/1`, `/users/2`, etc., with `id` being `1`, `2`, etc., respectively¹.

**useParams Hook in React Router:**

`useParams` is a hook provided by React Router that allows you to access the parameters of the current route¹. It returns an object of key/value pairs of the dynamic params from the current URL that were matched by the `Route` path².

Here's a simple example of how to use `useParams`:

```jsx
import { useParams } from 'react-router-dom';

function User() {
  let { id } = useParams();
  return <h2>User ID: {id}</h2>;
}
```

In this example, the `User` component is rendered when the URL matches `/users/:id`. The `id` parameter from the URL is accessed using the `useParams` hook¹.

In conclusion, `Params` and `useParams` are essential parts of React Router that allow you to create and manage dynamic routes in your application. They enable you to build more flexible and interactive applications.