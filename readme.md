# Google-Style Accordion Dropdowns

A lightweight and accessible JavaScript/CSS implementation of Google-inspired accordion dropdowns, focused on smooth animations and user experience. Try Googling something like [how to grow an avocado stone in water](https://www.google.com/search?q=how+to+grow+an+avocado+stone+in+water) and you'll see a 'People also ask' section.

<a href="https://danedwardsdeveloper.github.io/google-style-accordion-dropdowns/" target="_blank">Live demo</a>

![Google-style accordion GIF demo](https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExNzdncms1MGpuaDluNW5uY21oY2Z4OXN0cmVsY2Y4enVlZDlqbzltNiZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/6kBytkO0LDrbh2vCYC/giphy.gif)

### Features

- Smooth, CSS-driven opening/closing animations
- Keyboard navigation support
- ARIA attributes for enhanced accessibility

---

### Notes

- The icons are from [Google Material Symbols](https://fonts.google.com/icons). If anyone knows how to change the colour of these SVGs please let me know! (They should be `#757878`)
- `:focus-visible` is for accessibility. An orange border is added to indicate focus only when using the keyboard. It isn't supported by all browsers. [Can I Use: :focus-visible](https://caniuse.com/css-focus-visible)

---

## Getting started

```html
<!-- index.html -->

<button class="accordion" role="button" aria-label="Expand Details">
  <div class="question">In the olden days, when knights wore armor, how did they go to the toilet?</div>
  <div class="toggle-icon-background">
    <img class="toggle-icon" src="./assets/icons/expand-icon.svg" alt="" />
  </div>
</button>
<div class="panel">
  <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
</div>
```

```css
/*accordion.css*/

.accordion {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: white;
  color: #1f1f1f;
  margin: 0;
  padding: 0.8rem 0px;
  cursor: pointer;
  width: 100%;
  border: none;
  text-align: left;
  outline: none;
  font-size: 1rem;
  transition: 0.4s;
  border-top: 1px solid #dadce0;
}
.accordion:focus-visible {
  border: 2px solid orange;
  border-radius: 4px;
}

.question {
  max-width: 80%;
}

.panel {
  max-height: 0;
  padding: 0px;
  color: #474747;
  transition: height 0.2s ease-in;
  background-color: white;
  font-size: 1rem;
  overflow: hidden;
}
.panel:last-of-type {
  border-bottom: 1px solid #dadce0;
}

.toggle-icon-background {
  padding: 0.4rem;
  background-color: #f7f8f9;
  height: 2rem;
  width: 2rem;
  border-radius: 100%;
  text-align: center;
}

.toggle-icon {
  height: 2rem;
  margin: 0;
  padding: 0;
  vertical-align: middle;
  transition: transform 0.2s ease-in-out;
}

.upside-down {
  transform: rotate(-180deg);
}
```
