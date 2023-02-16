## CSS phase 2

### Media Query

```
<div id="smartphone"><h1>Smart Phone</h1></div>
<div id="tablets"><h1>Tablets</h1></div>
<div id="normal"><h1>Laptop, Desktop</h1></div>
<div id="widescreen"><h1>TV</h1></div>
<div id="landscape"><h1>Landscape</h1></div>
```

```
body {
  background: gray;
  color: white;
  text-align: center;
  padding: 100px;
}
h1 {
  display: none;
}
@media only screen and (max-width: 500px) {
  body {
    background-color: red;
  }
  #smartphone h1 {
    display: block;
  }
}
@media (min-width: 501px) and (max-width: 768px) {
  body {
    background-color: blue;
  }
  #tablets h1 {
    display: block;
  }
}
@media (min-width: 769px) and (max-width: 1200px) {
  body {
    background-color: green;
  }
  #normal h1 {
    display: block;
  }
}
@media (min-width: 1201px) {
  body {
    background-color: black;
  }
  #widescreen h1 {
    display: block;
  }
}
@media (max-height: 500px) {
  body {
    background-color: orange;
  }
  #landscape h1 {
    display: block;
  }
}
```

### Flexbox

```
<div class="flex-container">
  <div class="item item-1">
    <h3>Item 1</h3>
  </div>
  <div class="item item-2">
    <h3>Item 2</h3>
  </div>
  <div class="item item-3">
    <h3>Item 3</h3>
  </div>
  <div class="item item-4">
    <h3>Item 4</h3>
  </div>
  <div class="item item-5">
    <h3>Item 5</h3>
  </div>
  <div class="item item-6">
    <h3>Item 6</h3>
  </div>
  <div class="item item-7">
    <h3>Item 7</h3>
  </div>
  <div class="item item-8">
    <h3>Item 8</h3>
  </div>
  <div class="item item-9">
    <h3>Item 9</h3>
  </div>
  <div class="item item-10">
    <h3>Item 10</h3>
  </div>
</div>
```

```
* {
  box-sizing: border-box;
}
.flex-container {
  display: flex;
  background-color: aqua;
}
.item {
  background: orange;
  border: 1px solid black;
  width: 200px;
  margin: 10px;
  padding: 10px;
  text-align: center;
  border-radius: 10px;
}
```

#### flex-direction

```
row (default)
column
row-reverse
column-reverse
```

```
.flex-container {
  display: flex;
  background-color: aqua;
  flex-direction: row-reverse;
}
```

#### flex-wrap

```
nowrap
wrap
wrap-reverse
```

```
.flex-container {
  display: flex;
  background-color: aqua;
  flex-direction: row;
  flex-wrap: wrap;
}
```

#### Flex-properties (items)

```
flex-shrink
flex-grow
flex-basis
flex:1
```

```
.item-2 {
  flex-shrink: 3;
}
.item-3 {
  flex-grow: 2;
}
```

#### Flex Justify

```
flex-start
center
flex-end
space-around
space-between
```

```
.flex-container {
  display: flex;
  background-color: aqua;
  flex-direction: row;
  justify-content: center;
}
```

#### Flex Alignment

```
align-items(All items) & align-self(only item that you want)
stretch
flex-start
center
flex-end
```

```
.flex-container {
  display: flex;
  background-color: aqua;
  flex-direction: column;
  align-items: center;
}
```

```
.flex-container {
  display: flex;
  background-color: aqua;
  flex-direction: row;
  height: 50vh;
  align-items: stretch;
}
```

```
* {
  box-sizing: border-box;
}
.flex-container {
  display: flex;
  background-color: aqua;
  flex-direction: row;
  height: 50vh;
  align-items: flex-start;
}
.item {
  background: orange;
  border: 1px solid black;
  width: 200px;
  margin: 10px;
  padding: 10px;
  text-align: center;
  border-radius: 10px;
}
.item-2 {
  align-self: center;
}
.item-3 {
  align-self: flex-end;
}
```

### CSS Grid Layout

```
<div class="grid-container">
  <div class="item">Item 1</div>
  <div class="item">Item 2</div>
  <div class="item">Item 3</div>
  <div class="item">Item 4</div>
  <div class="item">Item 5</div>
  <div class="item">Item 6</div>
  <div class="item">Item 7</div>
  <div class="item">Item 8</div>
  <div class="item">Item 9</div>
</div>
```

```
.grid-container {
  display: grid;
  grid-template-rows: 100px 200px 100px;
  grid-template-columns: auto 100px 200px;
}
.item {
  padding: 3rem;
  border: 1px solid #ccc;
  background: orange;
  font-size: 1.3rem;
  font-weight: bold;
  text-align: center;
}
```

#### Grid-rows, Grid-columns

```
.item:first-child {
  background-color: green;
  /* grid-column-start: 1;
  grid-column-end: 4; */
  grid-column: 1/4;
}
```

```
.item:first-child {
  background-color: green;
  /* grid-row-start: 1;
  grid-row-end: 4; */
  grid-row: 1/4;
}
```

#### span

```
/* .item:first-child {
  grid-column: 1/4;
  grid-row-start: 1;
  grid-row-end: 3;
} */

.item:first-child {
  grid-row: 2 / span 2;
  grid-column: 1 / span 3;
}
```

#### fr, gap

```
.grid-container {
  display: grid;
  grid-template-rows: repeat(3, 1fr);
  grid-template-columns: 1fr 3fr 1fr;
  grid-row-gap: 10px;
  grid-column-gap: 10px;
}
```

#### grid-template-area

```
<div class="grid-container">
  <div class="header-item">Header</div>
  <div class="sidebar-item">Sidebar</div>
  <div class="content-item">Content</div>
  <div class="footer-item">Footer</div>
</div>
```

```
.grid-container {
  display: grid;
  /* grid-template-columns: 1fr 4fr;
  grid-template-rows: 3fr 10fr 2fr; */
  /* grid-template-areas: */
  grid-template:
    "header header" 3fr
    "sidebar content" 10fr
    "footer footer" 2fr
    / 1fr 4fr;
}

.header-item {
  background-color: greenyellow;
  grid-area: header;
}
.content-item {
  background-color: orange;
  grid-area: content;
}
.footer-item {
  background-color: black;
  color: white;
  grid-area: footer;
}
.sidebar-item {
  background-color: blue;
  grid-area: sidebar;
}
```
