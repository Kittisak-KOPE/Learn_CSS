## CSS phase 3

### Advance Selectors

```
Targeted Selectors
    Descendant Selector
    Child Selector
Style By Attribute
Special Attribute
Pseudo Selectors
    first-child
    last-child
    nth-child
Before & After Pseudo
```

#### Targeted Selectors

```
<div>
    <p>
    Lorem, ipsum dolor sit amet consectetur adipisicing elit. Officiis,
    corporis.
    </p>
    <ul>
    <li><p>Item 1</p></li>
    <li><p>Item 2</p></li>
    <li><p>Item 3</p></li>
    </ul>
    <p>
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Quo maxime
    doloremque, illo magnam rem necessitatibus?
    </p>
</div>
<p>
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Obcaecati
    aliquid, voluptas consectetur hic fugiat iusto illum qui, ipsum recusandae
    aut non, optio in et nobis aperiam provident. Nesciunt, assumenda sit?
</p>
```

```
/* Descendant Selector */
p {
  background: green;
}
div p {
  background-color: greenyellow;
}

/* Child Selector */
div > p {
  background-color: yellow;
}
```

#### Style By Attribute

```
<a href="#" target="_blank">Google</a>
<a href="#" target="_self">Youtube</a>
<a href="#">Facebook</a>
```

```
a {
  background-color: orange;
}
a[target] {
  background-color: whitesmoke;
  color: red;
}
a[target="_blank"] {
  background-color: black;
  color: pink;
}
a[target="_self"] {
  color: purple;
}
```

#### Special Attribute

```
<form>
<input type="email" placeholder="e-mail" />
<input type="text" placeholder="message" />
<input type="submit" value="บันทึก" />
</form>
```

```
input[type="email"],
input[type="text"] {
  width: 80%;
  margin-bottom: 5px;
}
input[type="submit"] {
  color: white;
  background-color: red;
  border-radius: 10px;
}

```

#### Pseudo Selectors

```
<ul>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
    <li>Item 4</li>
    <li>Item 5</li>
    <li>Item 6</li>
    <li>Item 7</li>
    <li>Item 8</li>
    <li>Item 9</li>
    <li>Item 10</li>
    <li>Item 11</li>
    <li>Item 12</li>
    <li>Item 13</li>
    <li>Item 14</li>
    <li>Item 15</li>
    <li>Item 16</li>
    <li>Item 17</li>
    <li>Item 18</li>
    <li>Item 19</li>
    <li>Item 20</li>
</ul>
```

```
li {
  padding: 0.25rem;
  margin: 0.25rem;
  list-style: none;
}
li:first-child {
  background-color: red;
}
li:last-child {
  background-color: orange;
}
li:nth-child(3) {
  background-color: green;
}
li:nth-child(4) {
  background-color: cyan;
}
li:nth-last-child(3) {
  background-color: yellow;
}
```

```
li {
  padding: 0.25rem;
  margin: 0.25rem;
  list-style: none;
}
/* li:nth-child(3n) { */
/* li:nth-child(3n + 1) {
  background-color: orange;
} */

li:nth-child(odd) {
  background-color: yellow;
}
```

#### Before & After Pseudo

```
<label for="" class="is-required">Name</label>
<input type="text">
```

```
.is-required::before {
  content: "*";
  color: red;
  padding-left: 2px;
}
```

```
body {
  background-color: #333;
  color: #fff;
}
header {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  height: 100vh;
}
header > h1 {
  font-size: 4rem;
  margin: 1rem;
}
header::before {
  content: "";
  background: url("https://cdn.pixabay.com/photo/2023/02/07/00/25/relaxed-7772958_960_720.jpg")
    no-repeat center center/cover;
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: -1;
  opacity: 0.4;
}
```

### text-shadow

```
<h1>kittisak hanheam</h1>
```

```
h1 {
  text-shadow: 2px 2px red;
  text-shadow: 2px 2px 10px red;
}
```

### CSS Variable

```
<div class="box-1">
    <h3>Heading 1</h3>
    <p>
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusamus,
    exercitationem.
    </p>
</div>
<div class="box-2">
    <h3>Heading 2</h3>
    <p>
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusamus,
    exercitationem.
    </p>
</div>
<div class="box-3">
    <h3>Heading 3</h3>
    <p>
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusamus,
    exercitationem.
    </p>
</div>
```

```
:root {
  --box: 1px solid red;
  --them-color: pink;
  --shadow: 5px 5px var(--them-color);
  --spacing: 20px;
  --font: 20px;
}
.box-1 {
  border: var(--box);
  background-color: var(--them-color);
  box-shadow: var(--shadow);
  margin: var(--spacing);
  font-size: var(--font);
}
.box-2 {
  border: var(--box);
}
.box-3 {
  border: var(--box);
  background-color: var(--them-color);
}
```

### CSS Transform

```
translate(x, y)
scale(x, y)
retate(deg)
skewX(deg)
skewY(deg)
```

```
<div class="box">hi</div>
```

```
.box {
  width: 100px;
  height: 100px;
  background-color: red;
  border: 2px solid black;
  margin: 100px;

  /* transform: translate(200px, 100px); */
  /* transform: rotate(45deg); */
  /* transform: rotateX(40deg); */
  /* transform: rotateY(40deg); */
  /* transform: scale(2); */
  /* transform: scale(1.2, 2); */

  /* transform: skewX(10deg);
  transform: skewY(20deg); */
  transform: skew(10deg, 20deg);
}
```

### CSS Transition

```
transition-properties
transition-duration
transition-timing-function
transition-delay
```

```
<div class="box">hi</div>
```

```
body {
  background: #333;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100vh;
}
.box {
  background: white;
  width: 100px;
  height: 100px;

  /* transition-property: background-color;
  transition-duration: 2s;
  transition-timing-function: ease-in-out;
  transition-delay: 3s; */
  /* transition: background-color 2s ease-in-out 3s; */

  /* transition: background 3s, width 3s ease-in 0.5s; */
  /* transition: background 3s, width 3s, border-radius 3s ease-in 0.5s; */
  transition: all 3s ease-in 0.5s;
}
.box:hover {
  background: red;
  width: 300px;
  border-radius: 50%;
}
```

### CSS Animation

```
animation-name
animation-duration
animation-timing-function
animation-iteration-count
animation-direction
animation-delay
```

```
<div class="box">hi</div>
```

```
body {
  background-color: #333;
}
.box {
  background-color: white;
  width: 100px;
  height: 100px;

  animation-name: animate1;
  animation-duration: 3s;
  animation-iteration-count: infinite;
  animation-direction: alternate;
  animation-timing-function: ease-in;
}

@keyframes animate1 {
  form {
    width: 100px;
  }
  to {
    width: 400px;
  }
}
```

```
body {
  background-color: #333;
}
.box {
  background-color: white;
  width: 100px;
  height: 100px;
  position: relative;
  /* animation-name: animate2;
  animation-iteration-count: infinite;
  animation-duration: 5s; */
  animation: animate2 5s infinite;
}

@keyframes animate2 {
  0% {
    top: 0;
    left: 0;
    transform: rotate(0deg);
    background-color: red;
  }
  25% {
    top: 0;
    left: 300px;
    transform: rotate(45deg);
    background-color: yellow;
  }
  50% {
    top: 300px;
    left: 300px;
    transform: rotate(90deg);
    background-color: green;
  }
  75% {
    top: 300px;
    left: 0px;
    transform: rotate(270deg);
    background-color: orange;
  }
  100% {
    top: 0px;
    left: 0px;
    transform: rotate(360deg);
    background-color: red;
  }
}
```
