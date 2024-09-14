
## Creating a React project
- Install Node.js
- Run npm install create-react-app -g //* deprecated, now we use Vite
- Go to cd “Your-project”
- Run npm start
- Start coding

## History of React
- Open source Library developed in Javascript for building user interfaces.
- Freed for open source in 2013.
- Created by Facebook.
- Based in XHP, an evolution from PHP
- Born for giving a response to Single Page Aplications
## Characteristics
- Declarative
- Component Based
We tell the program what we are expecting, but not how we are giving it making the code more flexible for future changes.
- Reactive Programming
- Virtual DOM and diffing
- Synthetic events

![[Pasted image 20240626105059.png]]
![[Pasted image 20240626105123.png]]

Ways to build components
![[Pasted image 20240626105138.png]]
![[Pasted image 20240626105158.png]]

## Components

React components are the building blocks of a React application. They are self-contained, reusable pieces of code that represent parts of the user interface. Components can be either functional or class-based:

1. **Functional Components**: These are simple functions that return JSX (a syntax extension that looks like HTML). They can accept props (inputs) and can use hooks for managing state and side effects.

```jsx
function MyComponent(props) {
  return <div>Hello, {props.name}!</div>;
}
```

2. **Class Components**: These are ES6 classes that extend from `React.Component`. They have a render method that returns JSX and can manage their own state and lifecycle methods.

```jsx
class MyComponent extends React.Component {
  render() {
    return <div>Hello, {this.props.name}!</div>;
  }
}
```

Components can be nested within each other to create complex user interfaces. They help in organizing the code, making it more modular, maintainable, and easier to understand.
## Props

Take in mind that all components made in React must obey the pure function properties.

- We can stablish default props in React components to ensure that these ones have default values.
## State

- We should treat it as immutable data
- We can only update it using the _setState_ method
- It is asynchronous
React has an unidirectional way of handling state, meaning that each time the parent component is updated, the subsequent children are updated.

Note that if you make a component stateful, no other components are aware of its `state`. Its `state` is completely encapsulated, or local to that component, unless you pass state data to a child component as `props`. This notion of encapsulated `state` is very important because it allows you to write certain logic, then have that logic contained and isolated in one place in your code.
![[Pasted image 20240626105236.png]]
## Conditional rendering

We are showing a Component depending on the value of *showA*.

![[Pasted image 20240626105304.png]]

## Lifecycle Methods

### Mounting (When a component is being created and inserted into the DOM)

1. **constructor(props)**
    
    - Initializes the component's state and binds event handlers.
    - Rarely used directly; state is often set using `useState` in functional components.
2. **componentDidMount()**
    
    - Invoked immediately after a component is mounted.
    - Commonly used for making API calls or setting up subscriptions.

### Updating (When the component's state or props change)

3. **shouldComponentUpdate(nextProps, nextState)**
    
    - Determines whether the component should re-render based on changes in props or state.
    - Used to optimize performance by preventing unnecessary renders.
4. **componentDidUpdate(prevProps, prevState, snapshot)**
    
    - Called after the component's updates are flushed to the DOM.
    - Useful for performing DOM operations or making API calls based on prop or state changes.

### Unmounting (When a component is being removed from the DOM)

5. **componentWillUnmount()**
    - Invoked immediately before a component is unmounted and destroyed.
    - Used for cleanup tasks such as invalidating timers, canceling network requests, or cleaning up subscriptions.

### Error Handling

6. **componentDidCatch(error, info)**
    - Called when there is an error during rendering, in a lifecycle method, or in the constructor of any child component.
    - Used to log errors or display a fallback UI.

### Example Usage in Class Component

Here's an example demonstrating some lifecycle methods in a class component:

```tsx
class MyComponent extends React.Component {
	constructor(props) {
		super(props);
		this.state = { data: null };
	}
	
	componentDidMount() {
    // Fetch data when the component mounts
    fetch('/api/data')
		.then(response => response.json())
		.then(data => this.setState({ data }));
	}
	
	componentDidUpdate(prevProps, prevState) {
		// Perform actions when the component updates
		if (this.state.data !== prevState.data) {
			console.log('Data updated:', this.state.data);
		}
	}
	
	componentWillUnmount() {
		// Cleanup before the component unmounts
		console.log('Component will unmount');
	}
	
	render() {
		return (
			<div>
				<h1>Data: {this.state.data}</h1>
			</div>
		);
	}
}
```