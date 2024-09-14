## Introduction

React hooks are functions that let you "hook into" React state and lifecycle features from function components. They were introduced in React 16.8 to provide a more direct API to the concepts React developers are familiar with — state, lifecycle, and context.

## Basic Hooks

### useState

`useState` is a Hook that lets you add React state to function components.

```jsx
import React, { useState } from 'react';

function Counter() {
	const [count, setCount] = useState(0);
	
	return (
		<div>
	      <p>You clicked {count} times</p>
	      <button onClick={() => setCount(count + 1)}>Click me</button>
	    </div>
	);
}
```

### useEffect

`useEffect` is a Hook that lets you perform side effects in function components.

```jsx
import React, { useState, useEffect } from 'react';

function Example() {
	const [count, setCount] = useState(0);
	
	useEffect(() => {
	    document.title = `You clicked ${count} times`;
	}, [count]);
	
	return (
	    <div>
	      <p>You clicked {count} times</p>
	      <button onClick={() => setCount(count + 1)}>Click me</button>
	    </div>
	);
}
```

### useContext

`useContext` is a Hook that lets you subscribe to React context without introducing nesting.

```jsx
import React, { useContext } from 'react';

const ThemeContext = React.createContext('light');

function ThemedButton() {
	const theme = useContext(ThemeContext);
	
	return <button className={theme}>I am styled by theme context!</button>;
}
```

## Additional Hooks

### useReducer

`useReducer` is usually preferable to `useState` when you have complex state logic that involves multiple sub-values or when the next state depends on the previous one.

```jsx
import React, { useReducer } from 'react';

function reducer(state, action) {
	switch (action.type) {
	    case 'increment':
	      return { count: state.count + 1 };
	    case 'decrement':
	      return { count: state.count - 1 };
	    default:
	      throw new Error();
	}
}

function Counter() {
	const [state, dispatch] = useReducer(reducer, { count: 0 });
	
	return (
	    <div>
	      <p>Count: {state.count}</p>
	      <button onClick={() => dispatch({ type: 'increment' })}>+</button>
	      <button onClick={() => dispatch({ type: 'decrement' })}>-</button>
	    </div>
	);
}
```

### useCallback

`useCallback` returns a memoized callback.

```jsx
import React, { useState, useCallback } from 'react';

function Parent() {
	const [count, setCount] = useState(0);
	
	const increment = useCallback(() => {
	    setCount(count + 1);
	}, [count]);
	
	return <Child increment={increment} />;
}

function Child({ increment }) {
	return <button onClick={increment}>Increment</button>;
}
```

### useMemo

`useMemo` returns a memoized value.

```jsx
import React, { useState, useMemo } from 'react';

function Example() {
	const [count, setCount] = useState(0);
	
	const memoizedValue = useMemo(() => computeExpensiveValue(count), [count]);
	
	return <div>{memoizedValue}</div>;
}

function computeExpensiveValue(count) {
	// Expensive computation here
	return count * 2;
}
```

### useRef

`useRef` returns a mutable ref object whose `.current` property is initialized to the passed argument.

```jsx
import React, { useRef } from 'react';

function TextInputWithFocusButton() {
	const inputEl = useRef(null);
	const onButtonClick = () => {
		inputEl.current.focus();
	};
	
	return (
		<>
		    <input ref={inputEl} type="text" />
		    <button onClick={onButtonClick}>Focus the input</button>
		</>
	);
}
```

### useImperativeHandle

`useImperativeHandle` customizes the instance value that is exposed when using `ref`.

```jsx
import React, { useImperativeHandle, useRef } from 'react';

const FancyInput = React.forwardRef((props, ref) => {
	const inputRef = useRef();
	
	useImperativeHandle(ref, () => ({
		focus: () => {
		    inputRef.current.focus();
		},
	}));
	
	return <input ref={inputRef} />;
});

function Parent() {
	const ref = useRef();
	
	return (
		<>
		    <FancyInput ref={ref} />
		    <button onClick={() => ref.current.focus()}>Focus the input</button>
	    </>
	);
}
```

### useLayoutEffect

`useLayoutEffect` is the same as `useEffect`, but it fires synchronously after all DOM mutations.

```jsx
import React, { useState, useLayoutEffect, useRef } from 'react';

function LayoutEffectExample() {
	const [value, setValue] = useState(0);
	const inputRef = useRef();
	
	useLayoutEffect(() => {
		inputRef.current.value = value;
	}, [value]);
	
	return (
	    <div>
		    <input ref={inputRef} />
		    <button onClick={() => setValue(value + 1)}>Increment</button>
		</div>
	);
}
```

### useDebugValue

`useDebugValue` can be used to display a label for custom hooks in React DevTools.

```jsx
import React, { useState, useDebugValue } from 'react';

function useFriendStatus(friendID) {
	const [isOnline, setIsOnline] = useState(null);
	
	useDebugValue(isOnline ? 'Online' : 'Offline');
	
	// Imagine a real API call here
	
	return isOnline;
}
```

## Custom Hooks

Custom Hooks let you reuse stateful logic between components. A custom Hook is a JavaScript function whose name starts with ”use” and that may call other Hooks.

```jsx
import React, { useState, useEffect } from 'react';

function useFriendStatus(friendID) {
	const [isOnline, setIsOnline] = useState(null);
	
	useEffect(() => {
		function handleStatusChange(status) {
	    setIsOnline(status.isOnline);
    }
	
    // Imagine a real API call here
	
    return () => {
		    // Cleanup
	    };
	}, [friendID]);
	
	return isOnline;
}

function FriendStatus(props) {
	const isOnline = useFriendStatus(props.friendID);
	
	if (isOnline === null) {
		return 'Loading...';
	}
	
	return isOnline ? 'Online' : 'Offline';
}
```

## Rules of Hooks

1. **Only Call Hooks at the Top Level**: Don’t call Hooks inside loops, conditions, or nested functions.
2. **Only Call Hooks from React Functions**: Don’t call Hooks from regular JavaScript functions.

## Conclusion

React Hooks provide a powerful way to use state and other React features in function components. They simplify code by removing the need for class components and making it easier to share stateful logic between components.

For more detailed information and examples, refer to the official React documentation on Hooks.