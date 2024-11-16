# Technical Writing Assignment

For guidance on setting up and submitting this assignment, refer to the Marcy lab School Docs How-To guide for [Working with Short Response and Coding Assignments](https://marcylabschool.gitbook.io/marcy-lab-school-docs/fullstack-curriculum/how-tos/working-with-assignments#how-to-work-on-assignments).

## Prompt 1

Do some research on semantic and non-semantic elements and share your findings. Your response should include:
* Examples of semantic and non-semantic tags
* The differences between semantic and non-semantic tags
* The benefits of using semantic tags (when possible)

### Response 1
    Some examples of semantic tags are <header>,<footer>, <article>, <section>, <aside>, and <nav> which are all used to describe their purpose in ways that both the devloper and the web page can clearly understand.

    Some examples of non-semantic tags are <div> <span>, <b>, <i>, <hr>, and <font> which doesn't express what content is held within them. These tages are meant for styling purposes which is one of the main things that set them apart from semantic tags.

    The benefits of using semantic tags is a more effecient layout due to how easy it is to understand. It also makes it more easy to organize and manage especially for allowing screen readers.

## Prompt 2

Do some research on accessibility. What are some ways to make your website more accessible? Explain why it is important for developers to create websites that meet accessibility standards.

### Response 2

The goal of web accessibility is to ensure that all users, including those using assistive technologies like screen readers, voice commands, or alternative input devices, can access and interact with web content.

## Prompt 3

It is possible to add "inline" CSS styles to our html elements using the `style` attribute like so:

```html
<p style="color: red;" >hello world</p>
```

While this is possible, it is a best practice to instead write styles in a separate CSS file. Provide at least one argument for why it _might_ be considered useful to write inline styles, and then provide a more compelling argument for writing styles in a separate CSS file.

### Response 3

One situation where inline styles might be considered useful is for quick prototyping or testing. When you're rapidly trying out new styles or adjusting a small element on a page without the overhead of creating or modifying an external CSS file, inline styles provide an quicker way to make changes. This can be especially helpful in a development or debugging situation when you're experimenting with different styles and want to see results immediately without switching between files.

However, the best practice is to write styles in a separate CSS file, and this approach offers many advantages:

* Seperating the two: Keeping HTML and CSS separate makes your code cleaner and easier to maintain. HTML should be concerned with the structure and content of the page, while CSS handles the styling. This separation makes your code more readable.

* Reusability: A single external CSS file can be linked to multiple HTML pages, allowing for a consistent look and feel across an entire website. Inline styles, on the other hand, would need to be repeated in every individual element, making it harder to maintain.

* Performance: When using external CSS, the browser can cache the CSS file, leading to faster page loads on subsequent visits. Inline styles, being part of the HTML itself, are not cached and would be reloaded each time the page is accessed, potentially leading to slower load times.

On top of all of these arguments, using external css allows for an overall more clean and easier to maintain application.

## Prompt 4

Imagine you are teaching a brand new programmer a brief lesson about the `class` and `id` attributes in HTML as well as how to use them to style elements using CSS. Your lesson should have the following components:

* An explanation of the concept of "classes" and "ids" with an analogy.
* An example of the usage using an HTML code block and a CSS code block.
* An explanation of the syntax using the terms: **attribute**, **selector** 

### Response 4
This is an example of how to use "ids" and "classes":

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <h1 id="title">Welcome to My Website</h1>
  <p class="highlight">This paragraph will be highlighted.</p>
  <p class="highlight">Another paragraph with the same class.</p>
  <p>This paragraph has no class or ID.</p>
</body>
</html>
```

And this is an example of css:

```css

/* Using ID selector to style the element with id="main-title" */
#main-title {
  color: blue;          /* Blue text color */
  font-size: 2em;       /* Larger text for the title */
  text-align: center;   /* Center the title */
}

/* Using Class selector to style elements with class="highlight" */
.highlight {
  background-color: yellow;  /* Yellow background */
  font-weight: bold;         /* Bold text */
}
```

__Explaining Syntax__ 

* Attributes: In HTML, `class` and `id` are attributes of HTML elements. An attribute is a characteristic or property that gives more information about an element.

* ID Attribute: `id="main-title"` gives the `h1` element a unique identifier. It’s used to identify and target a single element.

* Class Attribute: `class="highlight"` gives the `p` elements a shared label, meaning they belong to the same group. This allows you to apply the same style to all elements with the same class.

* Selectors: In CSS, a selector is used to target specific HTML elements in order to apply styles. The selector tells the browser which elements the style rules should apply to.

* ID Selector: To select an element with a specific `id`, you use `#` followed by the `id` name. For example, `#main-title` targets the element with `id="main-title"`.

* Class Selector: To select elements with a specific `class`, you use `.` followed by the `class` name. For example, `.highlight` targets all elements with `class="highlight"`.


## Prompt 5

The Document Object Model (DOM) API provides functions for manipulating HTML documents. It is possible to build an entire website using only JavaScript and the DOM API, however is that the best practice?

When building a website, how can I decide which content I should write using HTML/CSS and which content I should create using the JavaScript and the DOM API?

### Response 5

It is possible to build an entire web application using those two but it's not reccomended. HTML and CSS should be used for static content and structure (e.g., defining page layout, headings, and styles), while JavaScript and the DOM API should be used to add dynamic behavior and interactivity (e.g., modifying the DOM, responding to user input, fetching data).
