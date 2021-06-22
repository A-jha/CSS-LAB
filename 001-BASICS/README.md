## What is CSS?

- CSS stands for Cascading Style Sheets

- CSS describes how HTML elements are to be displayed on screen, paper, or in other media

- CSS saves a lot of work. It can control the layout of multiple web pages all at once

- External stylesheets are stored in CSS files

## CSS Syntax

- CSS is a collection of Rules

```html
<p>hello</p>
```

- to style the paragraph select p tag and add properties and values.

```css
p {
  color: yellow;
  text-align: cnter;
}
```

## CSS Selectors

A CSS selector selects the HTML element(s) you want to style.

We can divide CSS selectors into five categories:

- Simple selectors (select elements based on name, id, class)

```css
/*--------Class Selctor----*/
.classname {
}
/*---------id selector----*/
#IDname {
}
/*---------Tag-name-------*/
h1 {
}
div {
}
```

- Combinator selectors

  - select elements based on a specific relationship between them.

- Pseudo-class selectors

  - select elements based on a certain state

- Pseudo-elements selectors
  - select and style a part of an element.
- Attribute selectors
  - select elements based on an attribute or attribute value

## Three Ways to Insert CSS

There are three ways of inserting a style sheet:

- External CSS

```html
<head>
  <link rel="stylesheet" src="./style.css/" />
</head>
```

- Internal CSS

```html
<head>
  <style>
    #id1 {
      color: #123456;
      font-weight: 800;
    }
  </style>
</head>
```

- Inline CSS
  - it can override any style applied to this.

```html
<p style="color:blue;text-align:center">This is inline CSS</p>
```

# CSS Comments

Comments are used to explain the code, and may help when you edit the source code at a later date.

Comments are ignored by browsers.

```css
/*--------Comment---------*/
```

## Class And Id

- Both are ways to describe content.
- one class can have multiple tag.

```html
<p class="className"></p>
```

- One id has only one tag associated with that.

```html
<p id="Id1"></p>
```

## Inheritance tree

```html
<body>
  <h1>Head</h1>
  <div>
    <p>Text</p>
  </div>
</body>
```

- here if we cahnge the color of parent child then color of child will cahnge by default.

## Selector Specificity

```CSS
p{
    color:red;
}
p{
    color:white;/*this will be applied*/
}
```

- Specify the path

```CSS
#main p{
    color:red;/*This will win*/
}
p{
    color:white;
}
```

- How CSS Decides
  - ID 100 points
  - Classes 10 points
  - Elements 1 points

```html
<p class="c1" id="id1">Example</p>
```

```css
#id1 {
  color: red;
}
.c1 {
  color: white;
}
p {
  color: black;
}
```

- In the above case id has more specificity than other and styles of id is applied.

## !important

```CSS
#id1{
    color:red;
}
.c1{
    color:yellow !important;
}
```

- this time c1 will win because it use special declaration i.e. !important.

## Targetting Multiple element

```css
p,
span,
li,
a {
  color: black;
  font-size: 1.2rem;
}
```

## Decendent Selectors

```html
<main id="id1">
  <div class="div1">
    <p>Hello</p>
  </div>
  <p>Bye</p>
</main>
```

```CSS
#id1 .div1 p{
    color : green;
}

#id1 p{
    color:red;
}
```

## Children

```Html
<div class = "pd">
    <p>Direct Children-1</p>
    <p>Direct Children-2</p>
    <div>
        <p>Indirect Decendent</p>
    </div>
    <p>Direct Children-4</p>
</div>
```

```css
.pd > p {
  color: red;
}
```

## Adjecent Selector

- targets the element directly after the selector.

  ```html
  <div class="all-article">
    <h2>Artical-1</h2>
    <p>Hello I am adjecent</p>
    <p>I am Second adjecent</p>
    <p>I am third adject</p>
    <p>I am i am fourth</p>
  </div>
  ```

  ```CSS
  /*------Sectect first adjecent---*/
  .all-article h2 + p{
      color:red;
  }

  /*------Select second p tag---*/
  .all-artical h2 + p + p{
      color:blue;
  }

  /*----select such that all p after first    p----*/
  .all-article p + p{
      color:red;
  }
  ```

## Attribute Selectors

```html
<span>Hello i am span with no class</span>
<span class="c1">Hello i am span1-with class</span>
<span class="c2">Hello i am span1-with class</span>
<span class="c1">Hello i am span1-with class</span>
<span class="c1">Hello i am span1-with class</span>

<a href="hello.pdf">Hello pdf</a>
<a href="hello.txt">Hello txt</a>
<a href="hello.c">Hello c</a>
```

- select all span with class

```CSS
span[class]{
    color:blue;
}
```

- Select all with class c1

```css
span[class="c1"] {
  color: red;
}
```

- select a tag wth href with extension .pfd

```css
a[href$="pdf"] {
  color: red;
}
```
