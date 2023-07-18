# Advanced CSS

CSS (Cascading Style Sheets) is a powerful language used to control the presentation and layout of HTML documents. In this markdown file, we'll explore some advanced CSS techniques and features that can take your web design skills to the next level.
![Advanced Css image](https://bs-uploads.toptal.io/blackfish-uploads/components/blog_post_page/content/cover_image_file/cover_image/686791/retina_1708x683_0811-Eight_CSS_Tips_for_Advanced_Layouts_and_Effects_Dan_Newsletter___blog-caee7061d7279f9b5e3d8ab0db5e3622.png)

## Table of Contents

1. [Effortless Transitions](#effortless-transitions)
2. [Color Values](#color-values)
3. [Using Custom Properties (Variables)](#using-custom-properties)
4. [Managing Fonts with Variables](#managing-fonts-with-variables)

### 1. Effortless Transitions

When it comes to scrolling on web pages, smooth and fluid transitions enhance the user experience. By adding a simple CSS property, we can achieve this effect:

```css
/* In styles/1-style.css */

html {
  scroll-behavior: smooth;
}
```

Now, scrolling will be much more enjoyable, providing a seamless flow between sections on the page.

### 2. Color Values

Precise color choices can greatly impact the visual appeal of a website. We can set specific foreground colors for various elements in the CSS:

```css
/* In styles/2-style.css */

body {
  color: #161616; /* Set foreground color value for body */
}

a {
  color: #161616; /* Set foreground color value for all anchor elements */
}

.visually-hidden {
  display: none; /* Hide elements with the class visually-hidden */
}

.card-category {
  color: #D73953; /* Set foreground color for elements with class card-category */
}

.section-tagline {
  color: #D73953; /* Set foreground color for elements with class section-tagline */
}
```

### 3. Using Custom Properties

Custom properties (variables) in CSS allow us to define reusable values that can be used throughout the stylesheet. By targeting the root element, we can set and reuse these variables:

```css
/* In styles/3-style.css */

:root {
  --color-primary: #d73953; /* Custom property for primary color */
  --color-black: #090909; /* Custom property for black color */
  --color-white: #ffffff; /* Custom property for white color */
  --color-light-grey: #f3f3f3; /* Custom property for light grey color */
  --color-dark-grey: #353535; /* Custom property for dark grey color */
  --text-color: var(--color-black); /* Custom property for text color */
}

/* Reuse custom properties to set colors for elements */
.section-tagline,
.card-category {
  color: var(--color-primary); /* Reset color to color-primary */
}

body,
a {
  color: var(--text-color); /* Reset color to text-color */
}
```

### 4. Managing Fonts with Variables

Custom properties can also be utilized to manage font families in CSS. We can define font choices and apply them to different elements:

```css
/* In styles/4-style.css */

:root {
  --font-family-base: 'Helvetica Neue', Helvetica, Arial, sans-serif; /* Custom property for base font-family */
  --font-family-title: 'Helvetica Neue', Helvetica, Arial, sans-serif; /* Custom property for title font-family */
}

/* Set body's font-family to font-family-base */
body {
  font-family: var(--font-family-base);
}

/* Apply title font-family to section headings */
h1, h2, h3, h4, h5, h6 {
  font-family: var(--font-family-title);
}
```

By organizing font families into variables, we can easily update the fonts for the entire website by modifying just a few lines of code.

These advanced CSS techniques can significantly improve the design and functionality of your web pages. Experiment with them in your projects and take your CSS skills to the next level!