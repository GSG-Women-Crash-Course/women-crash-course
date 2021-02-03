# CSS Pseudo-class & Pseudo-element

<h2>
CSS Pseudo-class
</h2>

The **CSS Pseudo-class** is a keyword with a colon preceding it,
added to a selector and used to define the special state of the selected selector.

**Syntax:**

```CSS
selector:pseudo-class {
  property:value;
}
```

**There are many _Pseudo-class_ in _CSS_ but in this workshop, we will talk about the most used are as follows:**

### Basic Pseudo-classes

- hover
- checked
- enabled
- disabled
- first-child
- last-child
- nth-child(n)

* **:hover Pseudo-class:** used to apply style on the selected element after the user hovers the cursor over this element, for example:

```CSS
h1:hover{
  color: white;
  background-color: black;
}
```

[![](https://i.imgur.com/zUq6gi2.png)](https://codepen.io/fares98/pen/qBdRovE)

_In this example:_ when you `hove` the cursor over the specified element, the color will change to white and the background-color will change to black.

- **:checked Pseudo-class:** matches the checked selector (used for: radio button, checkbox button, and option element only), for example:

```CSS
input[type="checkbox"]:checked {
  margin-left: 30px;
}
```

[![](https://i.imgur.com/zUq6gi2.png)](https://codepen.io/fares98/pen/ExjZEBq)

_In this example:_ if any input with checkbox type was `Checked` or if the user clicked any `checkbox input`, this input will move 30px to the right.

> Read more about the **Attribute selectors** (The selector that used in the example) [here](https://developer.mozilla.org/en-US/docs/Web/CSS/Attribute_selectors)

<br />

- **:enabled Pseudo-class:** matches the enabled selector (the selectors that you can take an action on it, mostly with inputs), for example:

```CSS
input:enabled {
  background-color: gray;
  font-weight: bold;
}
```

_In this example:_ if any input with text type was `Enabled` will be with a gray background.

- **:disabled Pseudo-class:** matches the disabled selector (not enable: the selectors that you can't take any action on it, mostly with inputs ), for example:

```CSS
input:disabled {
  background-color: black;
}
```

_In this example:_ if any input with text type was `Disabled` will be with a black background.

[![](https://i.imgur.com/zUq6gi2.png)](https://codepen.io/fares98/pen/GRJrdWO)

- **:first-child Pseudo-class:** matches the first selector in the same parent, for example:

```CSS
h1:first-child {
  border: 1px solid red;
}
```

_In this example:_ this style will be applied to every first `h1` element in the same parent.

[![](https://i.imgur.com/zUq6gi2.png)](https://codepen.io/fares98/pen/RwPKyQx)

- **:last-child Pseudo-class:** matches the last selector in the same parent, for example:

```CSS
.class-1:last-child {
  background-color: blue;
}
```

_In this example:_ this style will be applied to every last element that has the `class-1` class in the same parent.

[![](https://i.imgur.com/zUq6gi2.png)](https://codepen.io/fares98/pen/dyoNKOK)

> **sometimes you need access to an element, but not the first or last element, maybe the second, the third, or the fourth ...etc. How you can do it?**

- **:nth-child(n) Pseudo-class:** take an argument(n) and matches the selector that is the nth-child, for example:

```CSS
p:nth-child(3) {
  border: 1px solid red;
}
```

_In this example:_ this style will be applied to every `p` element that is the `Third` element in the same parent.

[![](https://i.imgur.com/zUq6gi2.png)](https://codepen.io/fares98/pen/abOpKBL)

<br />

> The **:nth-child(n)** not only take a number, you can read more about it [here](https://developer.mozilla.org/en-US/docs/Web/CSS/:nth-child)

<br />

**We just talked about the basic pseudo class, if you interested you can read more [here](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes)**

---

<h2>
CSS Pseudo-elements
</h2>

The **CSS pseudo-element** is a keyword with two colons preceding it to differentiate them from pseudo-classes, added to a selector and lets you style a specific part of the selected element.

**_Syntax:_**

```CSS
selector::pseudo-element {
  property:value;
}
```

**The _pseudo-element_ in CSS, follow to learn it:**

### All Pseudo-element:

- first-letter
- first-line
- selection
- after
- before

* **::first-letter Pseudo-element:** apply styles to the first letter in the element selected.

```CSS
p::first-letter{
  font-size: 25px;
  font-weight: bold;
}
```

_In this example:_ this style will be applied to the `first-letter` within every `p` element on your page.

[![](https://i.imgur.com/zUq6gi2.png)](https://codepen.io/fares98/pen/RwPKyBQ)

- **::first-line Pseudo-element:** apply styles to the first line in the element selected.

```CSS
h3::first-line{
  font-weight: bold;
  font-size: 20px;
  color: blue;
}
```

_In this example:_ this style will be applied to the `first-line` within every `h3` element on your page.

[![](https://i.imgur.com/zUq6gi2.png)](https://codepen.io/fares98/pen/PoqWeyd)

- **::selection Pseudo-element:** apply styles to the part of an element that has been highlighted by a user, it's great for matching user-selected text to your site color scheme.

```CSS
p::selection{
  color: black;
  background-color: yellow
}
```

_In this example:_ this style will be applied to the part that you `selected` in all `p` elements on your page.

[![](https://i.imgur.com/zUq6gi2.png)](https://codepen.io/fares98/pen/WNvRJPB)

- **Other Examples**
  <div>
  <img  src="https://nicolasjengler.github.io/life-after-modern-layout-properties/images/text-selection.gif" /></div>

* **::after Pseudo-element:** insert new `content` after the selector, without adding new content in the `HTML`, for example:

```CSS
h3::after{
  content: 'Hello from CSS';
  color: red;
}
```

_In this example:_ you will see `Hello from CSS` `after` every `h3` element in your page.

[![](https://i.imgur.com/zUq6gi2.png)](https://codepen.io/fares98/pen/LYVxrPO)

- **::before Pseudo-element:** insert new `content` before the selector, without adding new content in the `HTML`, for example:

```CSS
p::before{
  content:'';
  display: inline-block;
  width: 12px;
  height: 12px;
  background-color: blue;
  border-radius: 50%;
  margin-right: 5px;
}
```

_In this example:_ you will see `blue circle` `before` every `p` element in your page.

[![](https://i.imgur.com/zUq6gi2.png)](https://codepen.io/fares98/pen/GRJrGJw)

**Notes:**

- This Pseudo element should contain the "content" property.
- The content prop may be empty, string, or image, you can read more about it [here](https://css-tricks.com/almanac/selectors/a/after-and-before/)
- using `after` you can make a style not insert text only
- the result appears as a Dom element but actually it's not a Dom element.
- It is inline by default.

---

<h2>
What's the difference between the Pseudo-classes & Pseudo-elements?
</h2>

| Pseudo-classes                                                                         | Pseudo-elements                                            |
| -------------------------------------------------------------------------------------- | ---------------------------------------------------------- |
| sets style properties for an element when the element is in a particular special state | styled some specific parts of the elements.                |
| use to style element that already finds in the HTML elements                           | use to create elements that not found in the HTML elements |

<br />
<br />

**Finally**: Can we combine Pseudo-classes and Pseudo-element, Why not?

You can combine between it by this syntax:

```CSS
selector:pseudo-class::pseudo-element{
  property: value;
  property: value;
  property: value;
}
```

**_Try it_**
