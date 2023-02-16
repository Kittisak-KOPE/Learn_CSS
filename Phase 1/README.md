# Learn_CSS

## CSS phase 1

### CSS External

index.html

```
  <head>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <p id="message">
      Lorem, ipsum dolor sit amet consectetur adipisicing elit. Tempore, a!
    </p>
```

style.css

```
p#message {
  color: blue;
}
```

### Unit

Absolute

```
px : 1px = 0.75pt
pt : 1pt = 1/72 inchs
cm
mm
in : 1in = 96px = 2.54cm
pc : 1pc = 12pt
```

Relative

```
%
em
rem
vw
vh
vmin, vmax
```

### Font

[cssfontstack](https://www.cssfontstack.com/)
style.css

```
p {
  font-family: "monospace", "fantasy";
}
```

[Google Font](https://fonts.google.com/)

### Box Model

```
div {
  border: 2px dashed orange;
  margin-top: 10px;
  margin-bottom: 20px;
}
.box-1 {
  margin-left: 20px;
}
.box-2 {
  margin-right: 20px;
}
img {
  width: 100px;
  margin: 10px;
}
```

padding

```
.box-1 {
  padding-top: 10px;
  padding-left: 20px;
  padding-bottom: 30px;
  padding-bottom: 20px;
}
.box-2 {
  padding: 10px;
}
```

### Background image

```
.box-2 {
  background-image: url("https://cdn.pixabay.com/photo/2022/04/13/15/21/beach-7130484__340.jpg");
}
```

### Float

index.html

```
<div class="box-1">
    <p>
    <img
        src="https://cdn.pixabay.com/photo/2023/02/04/14/22/fish-7767315__340.jpg"
        alt=""
    />
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Impedit culpa
    tempora animi quisquam earum delectus, dolorem voluptatem? Enim dolore
    architecto ex laboriosam? Fuga possimus et perspiciatis itaque
    perferendis pariatur enim similique accusamus voluptates, earum hic
    dolor molestias corporis animi eos. Accusamus iure iste illo voluptatum
    quasi sit accusantium at nesciunt impedit, praesentium eum. Ratione
    necessitatibus aliquam magni, laudantium nemo iste.
    </p>
</div>
```

style.css

```
img {
  width: 200px;
}
.box-1 img {
  float: left;
}
.box-2 img {
  float: right;
}
.box-3 img {
  float: none;
}
```

### style for link

a:link
a:hover
a:visited
a:active

### inline, block, inline-block

#### inline

index.html

```
<ul>
    <li><a href="#">Home</a></li>
    <li><a href="#">About</a></li>
    <li><a href="#">Page</a></li>
    <li><a href="#">Contact</a></li>
</ul>
```

style.css

```
li {
  display: inline;
}

li a {
  padding-right: 20px;
}
```

#### block, inline-block

index.html

```
<div class="box">
    <h1>Title 1</h1>
    <p>
    Lorem ipsum dolor sit amet consectetur, adipisicing elit. Alias
    excepturi aliquid nihil quisquam earum, dolores quo delectus tenetur eos
    vero.
    </p>
</div>
```

```
.box {
  width: 30%;
  box-sizing: border-box;

  /* block */
  /* display: block; */

  /* inline-block */
  display: inline-block;
}
```
