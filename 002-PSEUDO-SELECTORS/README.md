# Pseudo Selectors

- Special Keyword that go after selectors.
- They can be used to target.
  - special behavioral states
  - Advanced structural element.

## pseudo Class Groups

- Dynamic
- Structural
- Based on behaviour
- Advanced Structural

Eg: Hover effect

## Dynamic Pseudo Classes

Allow us to style element in relation to user action.

| `:hover` | `:active` | `:visited` |
| -------- | --------- | ---------- |

- Whether a link will have hover
- is Button pressed ?
- is checkbox is checked?

## Structural Pseudo classes

Allow us to style elements based on advanced structural techniques not possible from ordinary css selectors.

- The fifth <li\> tag from a list.
- A parent tag that has no children.

## : hover

- when cursor over then add styles.

```html
<div class="title">
  <h1>hellog G</h1>
</div>
```

- Add hover effrect to h1

```CSS
.title h1:hover{
    color:red;
}
```

## : active

- The :active CSS pseudo-class represents an element (such as a button) that is being activated by the user. When using a mouse, "activation" typically starts when the user presses down the primary mouse button.

```html
<a href="https://www.w3schools.com/css/css_colors.asp">W3 School</a>
```

- Change the color of link during click can be done using :active.

```css
a:active {
  color: white;
}
```

## : visited

Visited is used if you visited any thing then when you return back then it reminds that you visited this.

```html
<a href="https://www.w3schools.com/css/css_colors.asp">Visited</a>
```

- change the color of link after visiting

```css
a:visited {
  color: black;
}
```

## : first-child

it will apply styling on first child of any nested tags.

```html
<div>
  <!-first child--->
  <p>1-st</p>
  <p>2-nd</p>
  <p>3-rd</p>
</div>
```

- change color of first child

```css
div p:first-child {
  color: green;
}
```

## : last-child

it will apply styling on last child of any nested tags.

```html
<div>
  <p>1-st</p>
  <p>2-nd</p>
  <!-last child--->
  <p>3-rd</p>
</div>
```

- change last child color

```css
div p:last-child {
  color: red;
}
```

## : first-of-type

- it is a psedo selector to select first item from a content

```css
div p:first-of-type {
  color: greenyellow;
}
```

## : last-of-type

- to select last element

```css
article p:last-of-type {
  color: hotpink;
}
```

## : nth-child(n)

- where n can be

  - even -for position
  - odd
  - 1 to n
  - any formula like 2n + 1 or 3n + 1

- select 2nd tag

```css
ul li:nth-child(2) {
  color: green;
}
```

- select even-positioned tags

```css
ul li:nth-child(even) {
  color: pink;
}
```

- select odd-child tags

```css
ul li:nth-child(odd) {
  color: pink;
}
```

- select 2nd and 4th child

```CSS
ul li:nth-child(2),li:nth-child(4){
    color:black;
}
```

- select 2n+3 rd element

```css
ul li:nth-child(2n + 3) {
  color: pink;
}
```

## : nth-of-type(n)

- selects n th child of specific type

```css
article p:nth-of-type(1) {
  background: red;
}
```

# Pseudo element

## :: before

- before is a pseudo element used to add content before the content of any tag.
- in the below we have p tag ang we are adding some content before that .

```html
<p>I am Avinash</p>
```

```css
p::before {
  content: "hello G ";
  color: green;
  font-size: 1.3rem;
}
```

Output will be : hello G I am Avinash

## :: After

```html
<p>I am Avinash</p>
```

```css
p::after {
  content: "hello G ";
  color: green;
  font-size: 1.3rem;
}
```

Output: I am Avinash hello G
