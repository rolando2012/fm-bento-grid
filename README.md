# Frontend Mentor - Bento grid solution

This is a solution to the [Bento grid challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/bento-grid-RMydElrlOj). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the interface depending on their device's screen size

### Screenshot

#### Desktop
![Desktop view](./screenshots/desktop.jpeg)

#### Mobile
![Mobile view](./screenshots/mobile.png)

### Links

- Solution URL: [GitHub Repository](https://github.com/rolando2012/fm-bento-grid)
- Live Site URL: [Live Demo](https://rolando2012.github.io/fm-bento-grid/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow

### What I learned

Building this Bento Grid challenge helped me solidify my understanding of semantic HTML and modern CSS layout techniques without relying on external frameworks. Key takeaways from this project include:

- **Semantic HTML & Accessibility (`<article>`, `<em>`, and `alt` attributes):**
  - Used `<article>` for each card in the grid because every block represents a self-contained, independent piece of content.
  - Used `<em>` instead of a generic `<span>` for emphasized text (such as *"quicker"* in the create section) to convey meaningful stress emphasis to screen readers rather than purely visual styling.
  - Learned when to write descriptive `alt` text versus leaving it empty (`alt=""`): informational graphics that convey data or meaning received descriptive text, while purely decorative illustrations were given empty `alt` attributes so screen readers skip them cleanly.
- **Self-Hosting Variable Fonts (`@font-face`):** Instead of relying on external CDN links, I imported the downloaded variable font files directly from the local `assets/fonts` directory using `@font-face` with `font-display: swap` to ensure reliable loading and full weight control (`100 900`).
- **CSS Grid with `grid-template-areas`:** Mapping out the desktop layout visually using `grid-template-areas` (instead of counting line numbers with `grid-column` and `grid-row`) made the code much cleaner and easier to maintain across breakpoints.
- **Combining CSS Grid and Flexbox:** Used CSS Grid for the two-dimensional macro layout of the cards and Flexbox inside individual components (like `.posting-section` and `.grow`) to align text and images dynamically.
- **Clean Image Cropping & Mobile-First BEM:** Used `overflow: hidden` on the grid cards combined with negative margins and `max-width: none` to recreate cropped illustrations without fragile `position: absolute` hacks, keeping styles organized with custom properties (`:root`) and BEM naming conventions.

```css
@font-face {
  font-family: 'DM Sans';
  src: url('./assets/fonts/DMSans-VariableFont_opsz,wght.ttf') format('truetype');
  font-weight: 100 900;
  font-style: normal;
  font-display: swap;
}

@media (min-width: 768px) {
  .bento-grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    grid-template-areas:
      "create  review   review   schedule"
      "create  accounts posting  schedule"
      "content accounts posting  schedule"
      "content audience grow     grow";
  }
}
```

### Continued development

In my upcoming projects, I plan to focus on:

- **Strengthening Vanilla CSS & Responsive Fundamentals:** Complete two more Frontend Mentor challenges—starting with the **FAQ Accordion (Newbie)**—to reinforce interactive UI states, accessible disclosure patterns, and responsive CSS fundamentals before moving to frameworks.
- **Transitioning to Tailwind CSS:** Once I wrap up these final vanilla CSS challenges, I will transition to building responsive layouts with Tailwind CSS, applying the core Grid, Flexbox, and spacing concepts I practiced here using utility-first classes.
- **Accessibility & Interactive States:** Deepening my understanding of keyboard navigation, ARIA attributes, and semantic HTML elements (like `<details>` and `<summary>`) in upcoming interactive components.

## Author

- Frontend Mentor - [@rolando2012](https://www.frontendmentor.io/profile/rolando2012)
- Github - [@rolando2012](https://github.com/rolando2012)
- LinkedIn - [Rolando Mercado Rojas
](https://www.linkedin.com/in/rolando-mercado-rojas/)