# CSS(Cascading Style Sheets) DevRef <!-- omit in toc -->

CSS is a stylesheet language that is used to describe the presentation of a HTML document. It describes how the elements should be rendered on screen, paper or any other medium.

---

## Contents

- [Contents](#contents)
- [Linking CSS to HTML](#linking-css-to-html)
  - [Inline CSS](#inline-css)
  - [Style Tag](#style-tag)
  - [External CSS](#external-css)
- [CSS Selectors](#css-selectors)
  - [CSS Selectors For Tags](#css-selectors-for-tags)
  - [CSS Selectors For Classes](#css-selectors-for-classes)
  - [CSS Selectors For ID's](#css-selectors-for-ids)
  - [CSS Selectors For Peudo-Classes](#css-selectors-for-peudo-classes)
  - [CSS Selectors For Attributes](#css-selectors-for-attributes)
  - [Multiple Selectors](#multiple-selectors)

---

## Linking CSS to HTML

There are three ways in which we can link CSS to HTML.

- Inline CSS
- External CSS
- Style Tag

### Inline CSS

```html
<p style="color: red;">I'm learning to code!</p>
```

You can add multiple style rules to inline styles.

```css
<p style="color: red; font-size: 20px;">I'm learning to code!</p>
```

Inline styles have the highest precedence. They will overwrite any CSS declared in the `<style>` element or in an external file.

### Style Tag

"MUST EDIT"

HTML allows you to write CSS code in its own dedicated section with the `<style>` element. CSS can be written between opening and closing `<style>` tags. To use the `<style>` element, it **must be placed _inside_** of the `<head>` element.

```html
<head>
  <style>
    p {
      color: red;
      font-size: 20px;
    }
  </style>
</head>
```

### External CSS

"MUST EDIT"

When HTML and CSS code are in separate files, the files must be linked. Otherwise, the HTML file won’t be able to locate the CSS code, and the styling will not be applied.

You can use the `<link>` element to link HTML and CSS files together. The `<link>` element must be placed within the head of the HTML file. It is a self-closing tag and requires the following three attributes:

- `href` — like the anchor element, the value of this attribute must be the address, or path, to the CSS file.
- `type` — this attribute describes the type of document that you are linking to (in this case, a CSS file). The value of this attribute should be set to text/css.
- `rel` — this attribute describes the relationship between the HTML file and the CSS file.
  Because you are linking to a stylesheet, the value of rel should be set to stylesheet.

When linking an HTML file and a CSS file together, the <link> element will look like the following:

```html
<link href="www.abc.com/style.css" type="text/css" rel="stylesheet" />
```

If the CSS file is stored in the same directory as your HTML file, then you can specify a relative path instead of a URL, like so:

```html
<link href="./style.css" type="text/css" rel="stylesheet" />
```

## CSS Selectors

CSS can utilize different types of selectors to target different types of elements on an HTML page.

SYNTAX :

```css
selector {
  property: value;
}

// example
h1 {
  color: purple;
}

.highlight {
  background-color: red;
  font-size: 1.2rem;
}
```

You can use the HTML code snippet below to experiment with the different CSS selectors that we talk about in this section.

```html
<!-- Selectors for tags -->
<h1>Have you heard of Bees?</h1>

<h2>They are the saviors of the planet!</h2>

<p>Bees are flying insects closely related to wasps and ants, known for their role in pollination and, in the case of the best-known bee species, the western honey bee, for producing honey and beeswax. They are found on every continent except Antarctica, in every habitat on the planet that contains insect-pollinated flowering plants.</p>

<h3>Bee facts<span class="small">(for kids)<span></h3>

<ul>
  <li>Beekeepers use smoke to calm bees when they are collecting honey or relocating a hive</li>
  <li>Bees make honey to feed their young and so they have something to eat during the winter.</li>
  <li>Certain species of bees die after stinging.</li>
  <li></li>
  <li></li>
</ul>
```

### CSS Selectors For Tags

Tag selectors are used to target HTML tags.

SYNTAX:

```css
tag {
  property: value;
}

// example
h1 {
  color: red;
}

p {
  font-size: 1.2rem;
}
```

### CSS Selectors For Classes

Class selectors are used to target all elements that belong to class. To target the class we use a dot `.` before the class name to specify the selector.

For example, if the class name is `title`, in CSS we would target the elements with `.title`.

SYNTAX:

```css
.class {
  property: value;
}

// example
.title {
  font-size: 1.5rem;
}
```

### CSS Selectors For ID's

ID selectors are used to target the specific element that is assigned the ID. To target the ID we use a hash `#` before the ID name to specify the selector.

For example, if the class name is `special`, in CSS we would target the elements with `#special`.

SYNATAX:

```css
#id {
  property: value;
}

// example
#special {
  font-size: 1.5rem;
}
```

### CSS Selectors For Peudo-Classes

dasdf

### CSS Selectors For Attributes

asdf

### Multiple Selectors

Imagine if we needed to set the same CSS Style for a bunch of elements. Say, for example, we wanted to set the same style for all levels of headings, we could write something like this:

```css
h1 {
  font-family: "Arial", sans-serif;
}

h2 {
  font-family: "Arial", sans-serif;
}

h3 {
  font-family: "Arial", sans-serif;
}

h4 {
  font-family: "Arial", sans-serif;
}

h5 {
  font-family: "Arial", sans-serif;
}

h6 {
  font-family: "Arial", sans-serif;
}
```

This would become very cumbersome, hard to scale and over time as the project grows, it will become harder to maintain.

Instead, we can combine all the style declarations and define them together like this:

```css
h1,
h2,
h3,
h4,
h5,
h6 {
  font-family: "Arial", sans-serif;
}
```

The advantage of doing this is that all the declartions are in a single place and when we do want to make changes to the headings, we will need to do it at a single place.
