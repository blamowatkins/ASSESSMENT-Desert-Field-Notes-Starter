# Desert Field Notes — GIT 337 Repair Summary

Repository: https://github.com/blamowatkins/ASSESSMENT-Desert-Field-Notes-Starter
Published homepage: https://blamowatkins.github.io/ASSESSMENT-Desert-Field-Notes-Starter/
Published resources: https://blamowatkins.github.io/ASSESSMENT-Desert-Field-Notes-Starter/pages/resources.html

The original starter was checked against the corrected multipage site. All 12 required repair targets were addressed while preserving the supplied content and desert illustration.

| ID | Original problem | Correction |
|---|---|---|
| I1 | Missing document language | Set `<html lang="en">`. |
| I2 | Missing mobile viewport | Added `width=device-width, initial-scale=1` viewport meta element. |
| I3 | Incorrect Resources destination | Changed link to `pages/resources.html`. |
| I4 | Intro heading skipped a level | Changed introductory `h3` to `h2`. |
| I5 | Unhelpful image alt text | Described the saguaro cactus illustration. |
| R1 | Nested page stylesheet path wrong | Used `../css/styles.css`. |
| R2 | Two nested-page home links wrong | Changed both to `../index.html`. |
| C1 | `outline: none` hides focus | Added a visible `:focus-visible` outline. |
| C2 | Fixed 1100px page width | Used `min(1100px, calc(100% - 2rem))`. |
| C3 | Fixed three-column grid | Used `repeat(auto-fit, minmax(min(100%, 16rem), 1fr))`. |
| C4 | ID selector overrode reusable featured class | Removed the ID background style; retained `.featured` without `!important`. |
| C5 | Impossible min/max media query | Replaced it with `@media (max-width: 700px)`. |

## Evidence
Local screenshots captured both pages at 320 CSS pixels and 200% zoom, a visible keyboard-focus outline, working Resources/home links, and the published GitHub Pages design. The student's Nu HTML Checker screenshots report no errors or warnings for either HTML page. The W3C CSS Validator screenshot reports no errors.

The full 12-item repair log, code defense, original-to-corrected source diff, hashes, and named screenshots are included in the ZIP assignment submission.

## Primary references
- [MDN: HTML elements and attributes](https://developer.mozilla.org/en-US/docs/Web/HTML)
- [MDN: Keyboard accessible](https://developer.mozilla.org/en-US/docs/Web/Accessibility/Guides/Understanding_WCAG/Keyboard)
- [MDN: CSS grid-template-columns](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/grid-template-columns)
- [MDN: CSS specificity](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_cascade/Specificity)
- [MDN: Using media queries](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_media_queries/Using_media_queries)
