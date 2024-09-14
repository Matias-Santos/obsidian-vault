
CSS Grid Layout is a powerful layout system available in CSS. It allows you to design complex web layouts easily and more efficiently. Below are examples ranging from basic to advanced use cases, including `grid-template-columns`, `grid-template-rows`, `grid-row`, `grid-column` using `span`, and `grid-template-areas`.  
## Basic Usage  
### Simple Grid
To create a simple grid, you can use `display: grid` and define the columns using `grid-template-columns`.  
```css
.container {
	display: grid;
	grid-template-columns: 1fr 1fr;
	gap: 10px;
}
.item {
	background: lightblue;
	padding: 20px;
	border: 1px solid #ccc; 
}
```

```html
<div class="container">
	<div class="item">Item 1</div>
	<div class="item">Item 2</div>
	<div class="item">Item 3</div>
	<div class="item">Item 4</div>
</div>
```

This creates a 2-column grid with equal-width columns and a gap of 10px between the items.

## Medium Usage

### Using Grid Template Rows

You can define the rows using `grid-template-rows` similarly.


```css
.container {
	display: grid;
	grid-template-columns: 1fr 2fr;
	grid-template-rows: 100px 200px;
	gap: 10px;
}
.item {
	background: lightcoral;
	padding: 20px;
	border: 1px solid #ccc;
}
```

```html
<div class="container">
	<div class="item">Item 1</div>
	<div class="item">Item 2</div>
	<div class="item">Item 3</div>
	<div class="item">Item 4</div>
</div>
```

This creates a grid with two columns where the first column is 1fr and the second is 2fr, and two rows with fixed heights.

### Spanning Rows and Columns

You can make items span multiple rows or columns using `grid-row` and `grid-column`.

```css
.container {
	display: grid;
	grid-template-columns: 1fr 1fr 1fr;
	grid-template-rows: 100px 100px;
	gap: 10px;
}
.item1 {
	grid-column: span 2;
	background: lightgreen;
}
.item2 {
	grid-row: span 2;
	background: lightpink;
}
.item {
	background: lightyellow;
	padding: 20px;
	border: 1px solid #ccc;
}
```

```html
<div class="container">
	<div class="item item1">Item 1</div>
	<div class="item item2">Item 2</div>
	<div class="item">Item 3</div>
	<div class="item">Item 4</div>
</div>
```

Item 1 spans two columns, and Item 2 spans two rows.

## Advanced Usage

### Using Grid Template Areas

Grid template areas allow you to define regions of the grid to position items more easily.

```css
.container {
	display: grid;
	grid-template-columns: 1fr 1fr 1fr;
	grid-template-rows: 100px 100px 100px;
	grid-template-areas: "header header header"
						"sidebar content content"
						"footer footer footer";
	gap: 10px;
}
.header {
	grid-area: header;
	background: lightblue;
}
.sidebar {
	grid-area: sidebar;
	background: lightcoral;
}
.content {
	grid-area: content;
	background: lightgreen;
}
.footer {
	grid-area: footer;
	background: lightpink;
}
```

```html
<div class="container">
	<div class="header">Header</div>
	<div class="sidebar">Sidebar</div>
	<div class="content">Content</div>
	<div class="footer">Footer</div>
</div>
```

In this example, we use `grid-template-areas` to define a grid layout with named areas. Each item is then placed in its respective area using the `grid-area` property.

## Conclusion

CSS Grid is a powerful tool for creating complex layouts with ease. With `grid-template-columns`, `grid-template-rows`, `grid-row`, `grid-column`, and `grid-template-areas`, you can create flexible and responsive grid layouts. Experiment with these properties to see the wide range of layouts you can achieve!