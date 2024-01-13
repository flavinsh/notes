---
tags:
  - CSS
---
A **selector** is used to find the HTML element you want to style.

| HTML element                  | CSS selector | CSS declaration block   |
|:----------------------------- |:------------ |:----------------------- |
| `<p>`                         | `p`          | `p {` ... `;}`          |
| `<div>`                       | `div`        | `div {` ... `;}`        |
| `<h1>` and `<h2>`and `<h3>`   | `h1, h2, h3` | `h1, h2, h3 {` ... `;}` |
| `class="intro"`               | `.intro`     | `.intro {` ... `;}`     |
| `<p class="intro top large">` | `p.large`    | `p.large {`...`;}`      |
| `<div class="banana tomato">` | `div.banana`    | `div.banana {`...`;}`      |
| full page                     | `*`          | `*{`...`;}`              |
## Id
The `#id` selector uses the `id` attribute of an HTML element to select a specific element:
- The `id`element is unique within a page, so the `id`selector is used to **select one element**
- To select an element with a specific `id`, write a `#`character, followed by the `id`of the element

> [!example]
> - HTML element: `id="firstname"`
> - CSS declaration block `#firstname {` ... `}` will style all elements with the id "firstname".

## Class
The `.class`selector selects HTML elements with a specific **class attribute**:
- To select elements with a specific class, write a `.` character, followed by the `class`name
- HTML elements may refer to more than one class; use `element.class` to select one

> [!example] 
> - HTML element: `class="intro"`
> - CSS declaration block `.intro {` ... `}` will style all elements with the class "intro".

> [!example]
> - HTML element `<p class="intro top large">` ... `</p>`
> - CSS declaration block `p.large {` ... `}` will style paragraph with the class "large".

## Universal selector
The universal selector `*` selects all HTML on the page: 

> [!example]
>  `* {` ... `}` will style all elements on the page.

## Group selectors
To minimise the code, it is better to group the selectors: `element, element, element`

> [!example]
> `h1, h2, p {` ... `}` will style headings 1, headings and paragraphs.
  