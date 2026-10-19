# GIT 337 Code Defense — C2 Responsive Shared Width

**High-impact repair:** C2, the shared width rule in `css/styles.css`.

**Symptom:** The original site used a fixed desktop width, so content could overflow the browser window on narrow mobile viewports.

**Cause:** The starter rule gave `.site-header`, `main`, and `footer` a fixed `width: 1100px`, even when the CSS viewport was much smaller.

**Correction:**

```css
.site-header,
main,
footer {
  width: min(1100px, calc(100% - 2rem));
  margin-inline: auto;
}
```

CSS `min()` chooses the smaller allowed value. This preserves a maximum width of 1100 pixels on wide screens, but uses the available window width minus 2 rem on narrow screens. `margin-inline: auto` centers the container. I separately fixed the grid tracks and mobile media query to let the content inside the container adapt.

**Authority:** [MDN: `min()`](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Values/min) and [MDN: `calc()`](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Values/calc).

**Verification:** My corrected CSS screenshot shows the new width. The 320-CSS-pixel home and Resources screenshots show content wrapping into narrow columns without obvious horizontal clipping. The 200% zoom screenshots show readable content. The complete original and corrected files, HTML/CSS validator evidence, and screenshots are included in the submission ZIP.

**Decision:** Keep the desktop width maximum but replace the fixed-only size with a flexible expression. This supports smaller screens without sacrificing the visual identity.

**Verification limit:** These are screenshots and source evidence; a programmatically recorded comparison of `document.documentElement.scrollWidth` and `clientWidth` is not included.
