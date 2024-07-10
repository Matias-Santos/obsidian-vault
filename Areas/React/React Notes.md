
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
## Media Queries in React

Media queries in React can be implemented in a few different ways:

1. **Inline styling:** React supports inline styling where you can apply media queries directly in your component's style attribute. However, this approach is not very clean and can make your code messy.
2. **CSS Modules:** If you're using CSS modules in your project, you can define media queries just like you would in a regular CSS file. Then, you simply import the styles and use them in your components.
3. **Styled Components:** Styled Components is a library that allows you to write actual CSS in your JavaScript. This means you can use media queries directly in your component files.
4. **React-responsive:** This is a powerful library for implementing media queries in React. It allows you to use media queries in the form of React components.

Remember, the best method depends on your project's needs and your personal preference.

Here's an example of a media query using CSS:

```
@media (max-width: 600px) {
	.sidebar {
		display: none;
	}
}
```
In this example, the sidebar will not display on screens that are 600px wide or less.


