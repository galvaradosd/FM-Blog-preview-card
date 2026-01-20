# Frontend Mentor - Blog preview card solution

This is a solution to the [Blog preview card challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/blog-preview-card-ckPaj01IcS). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- See hover and focus states for all interactive elements on the page
- View the optimal layout for the card on mobile (375px) and desktop (1440px) screens
- Experience smooth transitions and accessibility-friendly interactions

### Links

- Solution URL: [GitHub Repository](https://github.com/galvaradosd/FM-Blog-preview-card)
- Live Site URL: [Live Demo](https://galvaradosd.github.io/FM-Blog-preview-card/)

## My process

### Built with

- **Semantic HTML5 markup** - Using `<article>`, `<figure>`, `<time>`, and `<address>` for better structure
- **CSS Custom Properties** - For maintainable and scalable styling
- **CSS Logical Properties** - For internationalization support (RTL languages)
- **Flexbox** - For layout and alignment
- **Mobile-first workflow** - Starting with mobile design (375px) and scaling up
- **Local web fonts** - Figtree font family (variable and static)
- **BEM methodology** - Block Element Modifier naming convention for CSS classes

### What I learned

During this project, I deepened my understanding of several modern CSS concepts:

#### 1. CSS Logical Properties
I implemented logical properties throughout the entire stylesheet to ensure the design works seamlessly with different writing modes and text directions:

```css
.blog-card {
  inline-size: 100%;
  max-inline-size: 327px;
  padding: var(--card-padding);
  margin-block-end: var(--spacing-lg);
}
```

This approach makes the component ready for RTL languages like Arabic or Hebrew without additional CSS.

#### 2. CSS Custom Properties Architecture
I created a comprehensive design token system using CSS variables:

```css
:root {
  /* Colors */
  --color-yellow: hsl(47, 88%, 63%);
  --color-gray-950: hsl(0, 0%, 7%);
  
  /* Spacing Scale */
  --spacing-xs: 0.5rem;
  --spacing-sm: 0.75rem;
  --spacing-md: 1rem;
  --spacing-lg: 1.5rem;
  --spacing-xl: 2rem;
  
  /* Typography */
  --font-weight-medium: 500;
  --font-weight-extra-bold: 800;
}
```

This makes the design system scalable and easy to maintain.

#### 3. Semantic HTML for Better Accessibility
Using the right HTML elements improved both SEO and screen reader accessibility:

```html
<article class="blog-card">
  <time datetime="2023-12-21">Published 21 Dec 2023</time>
  <address class="blog-card__author">
    <span class="blog-card__author-name">Greg Hooper</span>
  </address>
</article>
```

#### 4. Modern CSS Reset
I implemented a comprehensive CSS reset that:
- Uses logical properties (`min-block-size` instead of `min-height`)
- Prevents font size inflation on mobile
- Implements text wrapping balance for headings
- Sets up proper image defaults

#### 5. Local Font Implementation
Implemented both variable and static fonts with proper fallbacks:

```css
@font-face {
  font-family: "Figtree";
  src: url("assets/fonts/Figtree-VariableFont_wght.ttf") format("truetype");
  font-weight: 100 900;
  font-display: swap;
}
```

### Continued development

Areas I want to focus on in future projects:

1. **CSS Container Queries** - Explore using `@container` for more flexible component-based responsive design
2. **Advanced Animations** - Implement more sophisticated micro-interactions using CSS animations and transforms
3. **CSS Grid** - Practice more complex layouts using Grid alongside Flexbox
4. **Design Systems** - Build more comprehensive design token systems with theming support
5. **Performance Optimization** - Implement critical CSS and font loading strategies


### Useful resources

- [MDN - CSS Logical Properties](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Logical_Properties) - Essential guide for understanding logical properties and their benefits for internationalization
- [Modern CSS Reset by Andy Bell](https://piccalil.li/blog/a-modern-css-reset/) - The foundation for my CSS reset approach
- [BEM Methodology](https://getbem.com/) - Helped structure my CSS class naming convention
- [CSS Custom Properties Guide](https://css-tricks.com/a-complete-guide-to-custom-properties/) - Comprehensive guide to CSS variables and design tokens
- [Web.dev Accessibility](https://web.dev/accessibility/) - Best practices for building accessible web components
- [CSS Tricks - Logical Properties](https://css-tricks.com/css-logical-properties-and-values/) - Practical examples of using logical properties

## Acknowledgments

Special thanks to:
- Frontend Mentor for providing high-quality design challenges
- The CSS community for promoting modern best practices like logical properties
- Andy Bell for the modern CSS reset approach
- The MDN documentation team for comprehensive CSS references
