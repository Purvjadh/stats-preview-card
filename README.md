# Frontend Mentor - Stats Preview Card Component Solution

This is a solution to the [Stats preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/stats-preview-card-component-8JqbgoU62). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

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
  - [AI Collaboration](#ai-collaboration)
- [Author](#author)

---

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size

### Screenshot

![Stats Preview Card Solution](./images/Screenshot_one.png)
![Stats Preview Card Solution](./images/Screenshot%20_two.png)

### Links

- Solution URL: [solution URL here](https://github.com/Purvjadh/stats-preview-card/blob/main/style.css)
- Live Site URL: [ live site URL here](https://joyful-cactus-11b68d.netlify.app/)

---

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow
- Google Fonts (Inter, Lexend Deca)

### What I learned

**1. Image Overlay using opacity and background color**

To create a purple tint over the image, I wrapped the image in a `header` element and gave it a background color, then reduced the image opacity:

```css
header {
  background: #5f0f91;
  overflow: hidden;
}

img {
  object-fit: cover;
  opacity: 0.4;
}
```

**2. Percentage units stretch with screen size**

I learned that `%` units are responsive — they grow and shrink with the viewport. But `px`, `rem`, and `em` stay fixed or font-relative and do not stretch with the screen:

```css
/* stretches with screen */
.card {
  width: 50%;
}

/* always fixed */
.card {
  width: 400px;
}
```

**3. CSS Grid for two-column layout on desktop**

On desktop I used CSS Grid to put the text on the left and image on the right:

```css
article {
  display: grid;
  grid-template-columns: 1fr 1fr;
}
```

**4. Reordering elements with `order`**

On desktop the image needed to appear on the right even though it comes first in HTML. I used the `order` property to swap them:

```css
.card__info {
  order: 1;
}

header {
  order: 2;
}
```

**5. Three column stats grid**

```css
.card__stats {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  gap: 1.8em;
}
```

### Continued development

- I want to learn how to avoid repeating the same CSS for similar elements — currently `.company__div`, `.templates__div`, and `.queries__div` all have the same styles written three times
- I want to get more comfortable using `::before` and `::after` for image overlays instead of using `opacity`
- I want to practice using `min-height: 100dvh` instead of `height: 100vh` for better mobile support
- I want to use CSS variables more consistently — I defined some variables that I never ended up using

### Useful resources

- [MDN Web Docs — CSS Grid](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_grid_layout) - Helped me understand grid columns and the `order` property
- [MDN Web Docs — object-fit](https://developer.mozilla.org/en-US/docs/Web/CSS/object-fit) - Helped me understand how to make images fill their container properly

### AI Collaboration

I used Claude (by Anthropic) during this project as a learning companion.

- **Tools used:** Claude by Anthropic
- **How I used it:** I asked concept questions when I got stuck — things like how `%` units behave differently from `px`/`rem`/`em`, the difference between `height` and `min-height`, and why `height: 100%` was not centering the card
- **What worked well:** Getting visual diagram explanations for confusing concepts like `vh` vs `dvh` vs `%`, and `width` vs `max-width`
- **What I made sure to do:** Write all the code myself. I used AI only to understand concepts, never to generate solutions

---

## Author

- Frontend Mentor - [@purvajadhav](https://www.frontendmentor.io/profile/purvajadhav)
- Name - Purva Jadhav
