# Virtual DOM
- Creation Date: 2024-10-17
- Last Update: 2024-10-17
- Id: 
- Tags / Categories: #react #coding 
- State: 🌱
- Type: 
- Related: 
- Origin:
> [!TL:DR]
> 
>  The Virtual DOM is a lightweight copy of the real DOM, which allows react to make changes efficiently whenever something needs update. After the Virtual DOM is updated, react goes through a process known as Reconciliation, where only the necessary parts of the real DOM are updated, allowing for much more efficient updates on the GUI.
- References: 

## Context

Whenever you render a new JSX element in your application, the entire Virtual DOM is updated. Although it might sound inefficient, it is still faster that manipulating the real DOM. This is caused because React stores a copy of the Virtual DOM before making changes to it, via a process called Diffing, which only updates the JSX elements that have changed, and only updates those to the real DOM.

## Key Insights

By making constant comparisons between the last Virtual DOM and the one you are modifying, React is able to make efficient updates to the real DOM by only touching what has really changed.

## Key Arguments


## Connections


## Open Questions


## Applications

