# Web Technology

# CSS

## What is CSS

CSS stands for Cascading Style Sheets. It is the language for describing the presentation of Web pages, including colors, layout, and fonts, thus making our web pages presentable to the users.

CSS is designed to make style sheets for the web. It is independent of HTML and can be used with any XML-based markup language. The acronym stands for:

- Cascading: Falling of Styles
- Style: Adding designs/Styling our HTML tags
- Sheets: Writing our style in different documents

## **CSS Syntax**

The selector points to the HTML element you want to style.

The declaration block contains one or more declarations separated by semicolons.

Each declaration includes a CSS property name and a value, separated by a colon.

Multiple CSS declarations are separated with semicolons, and declaration blocks are surrounded by curly braces.

```css
p {
  color: red;
  text-align: center;
}
```

- `p` is a selector in CSS (it points to the HTML element you want to style: <p>).
- `color` is a property, and `red` is the property value
- `text-align` is a property, and `center` is the property value

## ****CSS How-To****

- There are 3 ways to write CSS in our HTML file.
    - Inline CSS
    - Internal CSS
    - External CSS
- Priority order
    - Inline > Internal > External
    
    ### Inline
    
    ```jsx
    <h3 style=” color:red”> Have a great day </h3>
    <p  style =” color: green”> I did this , I did that </p>
    ```
    
    ### Internal CSS
    
    ```jsx
    < style>
                  h1{
                         color:red;
                       }
         </style>  
        <h3> Have a great day </h3>
    ```
    
    ### External CSS
    
    ```jsx
    <head>
     <link rel="stylesheet" type="text/css" href="name of the Css file">
    </head>
                h1{
                         color:red;         //.css file
                     }
    ```
    
    ## **CSS Comments**
    
    Comments are used to explain the code, and may help when you edit the source code at a later date.
    
    Comments are ignored by browsers.
    
    A CSS comment is placed inside the `<style>` element, and starts with `/*` and ends with `*/`:
    
    ```html
    /* This is
    a multi-line
    comment */
    
    p {
      color: red;
    }
    ```
    
    ## ****CSS Selectors****
    
    CSS selectors are used to "find" (or select) the HTML elements you want to style.
    
    We can divide CSS selectors into five categories:
    
    1. Simple selectors (select elements based on name, id, class)
    2. Combinator selectors (select elements based on a specific relationship between them)
    3. Pseudo-class selectors (select elements based on a certain state)
    4. Pseudo-elements selectors (select and style a part of an element)
    5. Attribute selectors (select elements based on an attribute or attribute value)
    
    ### 1.1 **The CSS element Selector**
    
    The element selector selects HTML elements based on the element name.
    
    ```css
    p {
      text-align: center;
      color: red;
    }
    ```
    
    ### 1.2 **The CSS id Selector**
    
    The id selector uses the id attribute of an HTML element to select a specific element.
    
    The id of an element is unique within a page, so the id selector is used to select one unique element!
    
    To select an element with a specific id, write a hash (#) character, followed by the id of the element.
    
    ```css
    #para1 {
      text-align: center;
      color: red;
    }
    ```
    
    ### 1.3 **The CSS class Selector**
    
    The class selector selects HTML elements with a specific class attribute.
    
    To select elements with a specific class, write a period (.) character, followed by the class name.
    
    ```css
    .center {
      text-align: center;
      color: red;
    }
    ```
    
    You can also specify that only specific HTML elements should be affected by a class.
    
    In this example the <p> element will be styled according to class="center" and to class="large":
    
    ```css
    p.center {
      text-align: center;
      color: red;
    }
    ```
    
    ### 1.4 **The CSS Universal Selector**
    
    The CSS rule below will affect every HTML element on the page:
    
    ```css
    * {
      text-align: center;
      color: blue;
    }
    ```
    
    ### 1.5 **The CSS Grouping Selector**
    
    The grouping selector selects all the HTML elements with the same style definitions.
    
    Look at the following CSS code (the h1, h2, and p elements have the same style definitions):
    
    ```css
    h1 {
      text-align: center;
      color: red;
    }
    
    h2 {
      text-align: center;
      color: red;
    }
    
    p {
      text-align: center;
      color: red;
    }
    ```
    
    It will be better to group the selectors, to minimize the code.
    
    To group selectors, separate each selector with a comma.
    
    ```css
    h1, h2, p {
      text-align: center;
      color: red;
    }
    ```
    
    ### 2.1 **Descendant Selector**
    
    The descendant selector matches all elements that are descendants of a specified element.
    
    The following example selects all <p> elements inside <div> elements:
    
    ```css
    div p {
      background-color: yellow;
    }
    ```
    
    ### 2.2 Child Selector
    
    The child selector selects all elements that are the children of a specified element.
    
    The following example selects all <p> elements that are children of a <div> element:
    
    ```css
    div > p {
      background-color: yellow;
    }
    ```
    
    ### 2.3 **Adjacent Sibling Selector (+)**
    
    The adjacent sibling selector is used to select an element that is directly after another specific element.
    
    Sibling elements must have the same parent element, and "adjacent" means "immediately following".
    
    The following example selects the first <p> element that are placed immediately after <div> elements
    
    ```css
    div + p {
      background-color: yellow;
    }
    ```
    
    ### 2.4 **General Sibling Selector (~)**
    
    The general sibling selector selects all elements that are next siblings of a specified element.
    
    The following example selects all <p> elements that are next siblings of <div> elements:
    
    ```css
    div ~ p {
      background-color: yellow;
    }
    ```
    
    ### 3. **Pseudo-classes**
    
    A pseudo-class is used to define a special state of an element.
    
    For example, it can be used to:
    
    - Style an element when a user mouses over it
    - Style visited and unvisited links differently
    - Style an element when it gets focus
    
    syntax of pseudo-class
    
    ```css
    **selector:pseudo-class {
      property: value;
    }**
    ```
    
    ### 3.1 **Anchor Pseudo-classes**
    
    ```css
    a:link {
      color: #FF0000;
    }
    
    a:visited {
      color: #00FF00;
    }
    
    a:hover {
      color: #FF00FF;
    }
    
    a:active {
      color: #0000FF;
    }
    ```
    
    ### 3.2 **Pseudo-classes and HTML Classes**
    
    Pseudo-classes can be combined with HTML classes:
    
    ```css
    a.highlight:hover {
      color: #ff0000;
    }
    ```
    
    ### 3.3 **Hover on <div>**
    
    An example of using the `:hover` pseudo-class on a <div> element:
    
    ```css
    div:hover {
      background-color: blue;
    }
    ```
    
    ### 3.3 **Simple Tooltip Hover**
    
    Hover over a <div> element to show a <p> element (like a tooltip):
    
    ```css
    p {
      display: none;
      background-color: yellow;
      padding: 20px;
    }
    
    div:hover p {
      display: block;
    }
    ```
    
    ### 3.4 **CSS - The :first-child Pseudo-class**
    
    The `:first-child` pseudo-class matches a specified element that is the first child of another element.
    
    **Match the first <p> element**
    
    In the following example, the selector matches any <p> element that is the first child of any element:
    
    ```css
    p:first-child {
      color: blue;
    }
    ```
    
    **Match the first <i> element in all <p> elements**
    
    In the following example, the selector matches the first <i> element in all <p> elements:
    
    ```css
    p i:first-child {
      color: blue;
    }
    ```
    
    **Match all <i> elements in all first child <p> elements**
    
    In the following example, the selector matches all <i> elements in <p> elements that are the first child of another element:
    
    ```css
    p:first-child i {
      color: blue;
    }
    ```
    
    ### 3.5 **CSS - The :lang Pseudo-class**
    
    The `:lang` pseudo-class allows you to define special rules for different languages.
    
    In the example below, `:lang` defines the quotation marks for <q> elements with lang="no":
    
    ### 4. **CSS Pseudo-elements**
    

A CSS pseudo-element is used to style specified parts of an element.

For example, it can be used to:

- Style the first letter, or line, of an element
- Insert content before, or after, the content of an element

The syntax of pseudo-elements:

```css
selector::pseudo-element {
  property: value;
}
```

### 4.1 **The ::first-line Pseudo-element**

The `::first-line` pseudo-element is used to add a special style to the first line of a text.

The following example formats the first line of the text in all <p> elements:

```css
p::first-line {
  color: #ff0000;
  font-variant: small-caps;
}
```

### 4.2 **The ::first-letter Pseudo-element**

The `::first-letter` pseudo-element is used to add a special style to the first letter of a text.

The following example formats the first letter of the text in all <p> elements:

```css
p::first-letter {
  color: #ff0000;
  font-size: xx-large;
}
```

### 4.3 **Pseudo-elements and HTML Classes**

Pseudo-elements can be combined with HTML classes:

The example below will display the first letter of paragraphs with class="intro", in red and in a larger size.

```css
p.intro::first-letter {
  color: #ff0000;
  font-size: 200%;
}
```

### 4.4 **Multiple Pseudo-elements**

Several pseudo-elements can also be combined.

In the following example, the first letter of a paragraph will be red, in an xx-large font size. The rest of the first line will be blue, and in small-caps. The rest of the paragraph will be the default font size and color:

```css
p::first-letter {
  color: #ff0000;
  font-size: xx-large;
}

p::first-line {
  color: #0000ff;
  font-variant: small-caps;
}
```

### 4.5 **CSS - The ::before Pseudo-element**

The `::before` pseudo-element can be used to insert some content before the content of an element.

The following example inserts an image before the content of each <h1> element:

```css
h1::before {
  content: url(smiley.gif);
}
```

### 4.6 **CSS - The ::after Pseudo-element**

The `::after` pseudo-element can be used to insert some content after the content of an element.

The following example inserts an image after the content of each <h1> element:

```css
h1::after {
  content: url(smiley.gif);
}
```

### 4.7 **CSS - The ::marker Pseudo-element**

The `::marker` pseudo-element selects the markers of list items.

The following example styles the markers of list items:

```css
::marker {
  color: red;
  font-size: 23px;
}
```

### 4.8 **CSS - The ::selection Pseudo-element**

The `::selection` pseudo-element matches the portion of an element that is selected by a user. The following CSS properties can be applied to `::selection`: `color`, `background`, `cursor`, and `outline`.

The following example makes the selected text red on a yellow background:

```css
::selection {
  color: red;
  background: yellow;
}
```

### 5.**CSS [attribute] Selector**

The `[attribute]` selector is used to select elements with a specified attribute.

The following example selects all <a> elements with a target attribute:

```css
a[target] {
  background-color: yellow;
}
```

### 5.1 **CSS [attribute="value"] Selector**

The `[attribute="value"]` selector is used to select elements with a specified attribute and value.

The following example selects all <a> elements with a target="_blank" attribute:

```css
a[target="_blank"] {
  background-color: yellow;
}
```

### 5.2 **CSS [attribute~="value"] Selector**

The `[attribute~="value"]` selector is used to select elements with an attribute value containing a specified word.

The following example selects all elements with a title attribute that contains a space-separated list of words, one of which is "flower":

The example below will match elements with title="flower", title="summer flower", and title="flower new", but not title="my-flower" or title="flowers".

```css
[title~="flower"] {
  border: 5px solid yellow;
}
```

### 5.3 **CSS [attribute|="value"] Selector**

The `[attribute|="value"]` selector is used to select elements with the specified attribute, whose value can be exactly the specified value, or the specified value followed by a hyphen (-).

**Note:** The value has to be a whole word, either alone, like class="top", or followed by a hyphen( - ), like class="top-text".

```css
[class|="top"] {
  background: yellow;
}
```

### 5.3 **CSS [attribute$="value"] Selector**

The `[attribute$="value"]` selector is used to select elements whose attribute value ends with a specified value.

The following example selects all elements with a class attribute value that ends with "test":

**Note:** The value does not have to be a whole word!

```css
[class$="test"] {
  background: yellow;
}
```

### 5.4 **CSS [attribute*="value"] Selector**

The `[attribute*="value"]` selector is used to select elements whose attribute value contains a specified value.

The following example selects all elements with a class attribute value that contains "te":

**Note:** The value does not have to be a whole word!

```css
[class*="te"] {
  background: yellow;
}
```

# CSS Border Style

The `border-style` property specifies what kind of border to display.

The following values are allowed:

- `dotted` - Defines a dotted border
- `dashed` - Defines a dashed border
- `solid` - Defines a solid border
- `double` - Defines a double border
- `groove` - Defines a 3D grooved border. The effect depends on the border-color value
- `ridge` - Defines a 3D ridged border. The effect depends on the border-color value
- `inset` - Defines a 3D inset border. The effect depends on the border-color value
- `outset` - Defines a 3D outset border. The effect depends on the border-color value
- `none` - Defines no border
- `hidden` - Defines a hidden border

The `border-style` property can have from one to four values (for the top border, right border, bottom border, and the left border).

## Margins

The CSS `margin` properties are used to create space around elements, outside of any defined borders.

With CSS, you have full control over the margins. There are properties for setting the margin for each side of an element (top, right, bottom, and left).

---

### Margin - Individual Sides

CSS has properties for specifying the margin for each side of an element:

- `margin-top`
- `margin-right`
- `margin-bottom`
- `margin-left`

All the margin properties can have the following values:

- auto - the browser calculates the margin
- *length* - specifies a margin in px, pt, cm, etc.
- *%* - specifies a margin in % of the width of the containing element
- inherit - specifies that the margin should be inherited from the parent element

**Tip:** Negative values are allowed.

```css
p {
  margin-top: 100px;
  margin-bottom: 100px;
  margin-right: 150px;
  margin-left: 80px;
}
```

## Padding

The CSS `padding` properties are used to generate space around an element's content, inside of any defined borders.

With CSS, you have full control over the padding. There are properties for setting the padding for each side of an element (top, right, bottom, and left).

### Padding - Individual Sides

CSS has properties for specifying the padding for each side of an element:

- `padding-top`
- `padding-right`
- `padding-bottom`
- `padding-left`

All the padding properties can have the following values:

- *length* - specifies a padding in px, pt, cm, etc.
- *%* - specifies a padding in % of the width of the containing element
- inherit - specifies that the padding should be inherited from the parent element

**Note:** Negative values are not allowed.

```css
div {
  padding-top: 50px;
  padding-right: 30px;
  padding-bottom: 50px;
  padding-left: 80px;
}
```

## Navigation Bar

A navigation bar needs standard HTML as a base.

In our examples we will build the navigation bar from a standard HTML list.

A navigation bar is basically a list of links, so using the <ul> and <li> elements makes perfect sense:

```html
<ul>
  <li><a href="default.asp">Home</a></li>
  <li><a href="news.asp">News</a></li>
  <li><a href="contact.asp">Contact</a></li>
  <li><a href="about.asp">About</a></li>
</ul>
```

## **CSS Box Model**

In CSS, the term "box model" is used when talking about design and layout.

The CSS box model is essentially a box that wraps around every HTML element. It consists of: margins, borders, padding, and the actual content. The image below illustrates the box model:

Explanation of the different parts:

- **Content** - The content of the box, where text and images appear
- **Padding** - Clears an area around the content. The padding is transparent
- **Border** - A border that goes around the padding and content
- **Margin** - Clears an area outside the border. The margin is transparent

The box model allows us to add a border around elements, and to define space between elements.

```html
div {
  width: 300px;
  border: 15px solid green;
  padding: 50px;
  margin: 20px;
}
```

# Bootstrap

- Bootstrap is a free front-end framework for faster and easier web development
- Bootstrap includes HTML and CSS based design templates for typography, forms, buttons, tables, navigation, modals, image carousels and many other, as well as optional JavaScript plugins
- Bootstrap also gives you the ability to easily create responsive designs

Advantages of Bootstrap:

- **Easy to use:** Anybody with just basic knowledge of HTML and CSS can start using Bootstrap
- **Responsive features:** Bootstrap's responsive CSS adjusts to phones, tablets, and desktops
- **Mobile-first approach:** In Bootstrap 3, mobile-first styles are part of the core framework
- **Browser compatibility:** Bootstrap is compatible with all modern browsers (Chrome, Firefox, Internet Explorer, Edge, Safari, and Opera)

## Breakpoints

Breakpoints are customizable widths that determine how your responsive layout behaves across device or viewport sizes in Bootstrap.

- **Breakpoints are the building blocks of responsive design.** Use them to control when your layout can be adapted at a particular viewport or device size.
- **Use media queries to architect your CSS by breakpoint.** Media queries are a feature of CSS that allow you to conditionally apply styles based on a set of browser and operating system parameters. We most commonly use `min-width` in our media queries.
- **Mobile first, responsive design is the goal.** Bootstrap’s CSS aims to apply the bare minimum of styles to make a layout work at the smallest breakpoint, and then layers on styles to adjust that design for larger devices. This optimizes your CSS, improves rendering time, and provides a great experience for your visitors.

### Available Breakpoints

Bootstrap includes six default breakpoints, sometimes referred to as *grid tiers*, for building responsively. These breakpoints can be customized if you’re using our source Sass files.

| Breakpoint | Class infix | Dimensions |
| --- | --- | --- |
| Extra small | None | <576px |
| Small | sm | ≥576px |
| Medium | md | ≥768px |
| Large | lg | ≥992px |
| Extra large | xl | ≥1200px |
| Extra extra large | xxl | ≥1400px |

Each breakpoint was chosen to comfortably hold containers whose widths are multiples of 12.

## ****Containers****

Containers are a fundamental building block of Bootstrap that contain, pad, and align your content within a given device or viewport.

Containers are the most basic layout element in Bootstrap and are **required when using our default grid system**. Containers are used to contain, pad, and (sometimes) center the content within them. While containers *can* be nested, most layouts do not require a nested container.

Bootstrap comes with three different containers:

- `.container`, which sets a `max-width` at each responsive breakpoint
- `.container-{breakpoint}`, which is `width: 100%` until the specified breakpoint
- `.container-fluid`, which is `width: 100%` at all breakpoints

|  | Extra small<576px | Small≥576px | Medium≥768px | Large≥992px | X-Large≥1200px | XX-Large≥1400px |
| --- | --- | --- | --- | --- | --- | --- |
| .container | 100% | 540px | 720px | 960px | 1140px | 1320px |
| .container-sm | 100% | 540px | 720px | 960px | 1140px | 1320px |
| .container-md | 100% | 100% | 720px | 960px | 1140px | 1320px |
| .container-lg | 100% | 100% | 100% | 960px | 1140px | 1320px |
| .container-xl | 100% | 100% | 100% | 100% | 1140px | 1320px |
| .container-xxl | 100% | 100% | 100% | 100% | 100% | 1320px |
| .container-fluid | 100% | 100% | 100% | 100% | 100% | 100% |

### Default Containers

Our default `.container` class is a responsive, fixed-width container, meaning its `max-width` changes at each breakpoint.

```html
<div class="container">
  <!-- Content here -->
</div>
```

### ****Responsive containers****

Responsive containers allow you to specify a class that is 100% wide until the specified breakpoint is reached, after which we apply `max-width`s for each of the higher breakpoints. For example, `.container-sm` is 100% wide to start until the `sm` breakpoint is reached, where it will scale up with `md`, `lg`, `xl`, and `xxl`.

```html
<div class="container-sm">100% wide until small breakpoint</div>
<div class="container-md">100% wide until medium breakpoint</div>
<div class="container-lg">100% wide until large breakpoint</div>
<div class="container-xl">100% wide until extra large breakpoint</div>
<div class="container-xxl">100% wide until extra extra large breakpoint</div>
```

## **Fluid containers**

Use `.container-fluid` for a full width container, spanning the entire width of the viewport.

```html
<div class="container-fluid">
  ...
</div>
```

## **Grid System**

Bootstrap's grid system allows up to 12 columns across the page.

If you do not want to use all 12 columns individually, you can group the columns together to create wider columns:

### Grid classes

The Bootstrap grid system has four classes:

- `xs` (for phones - screens less than 768px wide)
- `sm` (for tablets - screens equal to or greater than 768px wide)
- `md` (for small laptops - screens equal to or greater than 992px wide)
- `lg` (for laptops and desktops - screens equal to or greater than 1200px wide)

The classes above can be combined to create more dynamic and flexible layouts.

### How it works

Breaking it down, here’s how the grid system comes together:

**Our grid supports six responsive breakpoints.** Breakpoints are based on `min-width` media queries, meaning they affect that breakpoint and all those above it (e.g., `.col-sm-4` applies to `sm`, `md`, `lg`, `xl`, and `xxl`). This means you can control container and column sizing and behavior by each breakpoint.

- **Containers center and horizontally pad your content.** Use `.container` for a responsive pixel width, `.container-fluid` for `width: 100%` across all viewports and devices, or a responsive container (e.g., `.container-md`) for a combination of fluid and pixel widths.
- **Rows are wrappers for columns.** Each column has horizontal `padding` (called a gutter) for controlling the space between them. This `padding` is then counteracted on the rows with negative margins to ensure the content in your columns is visually aligned down the left side. Rows also support modifier classes to [uniformly apply column sizing](https://getbootstrap.com/docs/5.3/layout/grid/#row-columns) and [gutter classes](https://getbootstrap.com/docs/5.3/layout/gutters/) to change the spacing of your content.
- **Columns are incredibly flexible.** There are 12 template columns available per row, allowing you to create different combinations of elements that span any number of columns. Column classes indicate the number of template columns to span (e.g., `col-4` spans four). `width`s are set in percentages so you always have the same relative sizing.
- **Gutters are also responsive and customizable.** [Gutter classes are available](https://getbootstrap.com/docs/5.3/layout/gutters/) across all breakpoints, with all the same sizes as our [margin and padding spacing](https://getbootstrap.com/docs/5.3/utilities/spacing/). Change horizontal gutters with `.gx-*` classes, vertical gutters with `.gy-*`, or all gutters with `.g-*` classes. `.g-0` is also available to remove gutters.
- **Sass variables, maps, and mixins power the grid.** If you don’t want to use the predefined grid classes in Bootstrap, you can use our [grid’s source Sass](https://getbootstrap.com/docs/5.3/layout/grid/#sass) to create your own with more semantic markup. We also include some CSS custom properties to consume these Sass variables for even greater flexibility for you.

### Equal width

- The following example shows how to get two various-width columns starting at tablets and scaling to large desktops:

```html
<div class="container text-center">
  <div class="row">
    <div class="col">
      1 of 2
    </div>
    <div class="col">
      2 of 2
    </div>
  </div>
  <div class="row">
    <div class="col">
      1 of 3
    </div>
    <div class="col">
      2 of 3
    </div>
    <div class="col">
      3 of 3
    </div>
  </div>
</div>
```

### **Setting one column width**

Auto-layout for flexbox grid columns also means you can set the width of one column and have the sibling columns automatically resize around it. You may use predefined grid classes (as shown below), grid mixins, or inline widths. Note that the other columns will resize no matter the width of the center column.

```html
<div class="container text-center">
  <div class="row">
    <div class="col">
      1 of 3
    </div>
    <div class="col-6">
      2 of 3 (wider)
    </div>
    <div class="col">
      3 of 3
    </div>
  </div>
  <div class="row">
    <div class="col">
      1 of 3
    </div>
    <div class="col-5">
      2 of 3 (wider)
    </div>
    <div class="col">
      3 of 3
    </div>
  </div>
</div>
```

### **Variable width content**

Use `col-{breakpoint}-auto` classes to size columns based on the natural width of their content.

```
<div class="container text-center">
  <div class="row justify-content-md-center">
    <div class="col col-lg-2">
      1 of 3
    </div>
    <div class="col-md-auto">
      Variable width content
    </div>
    <div class="col col-lg-2">
      3 of 3
    </div>
  </div>
  <div class="row">
    <div class="col">
      1 of 3
    </div>
    <div class="col-md-auto">
      Variable width content
    </div>
    <div class="col col-lg-2">
      3 of 3
    </div>
  </div>
</div>
```