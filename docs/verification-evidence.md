# Validation & Evidence Summary — Desert Field Notes

The 12 repairs are documented in [repair-summary.md](repair-summary.md) and the detailed C2 explanation in [code-defense.md](code-defense.md). The submitted ZIP also contains an annotated repair log, original-versus-corrected diff, and original screenshots.

## Validation
- Nu HTML Checker screenshots for `index.html` and `pages/resources.html` both report **no errors or warnings**.
- The W3C CSS Validator screenshot for `css/styles.css` reports **no errors**.
- The packaged corrected HTML, CSS, and SVG were checked against this repository's `main` branch by Git blob SHA-1.
- Static inspection of both HTML pages confirms all **13 relative link and asset references resolve**, including stylesheet, illustration and section fragments.
- Parsing the CSS with a local CSS parser showed no parse errors.

## Browser evidence in the ZIP
- Home and Resources layouts at **320 CSS pixels** and homepage at **375 CSS pixels**.
- Both pages at **200% browser zoom**.
- Keyboard focus screenshot with an orange outline on a navigation link.
- Green featured-card treatment driven by the reusable `.featured` class, without `!important`.
- GitHub Pages deployment settings and screenshots of both published pages.

## Limits and links
These results include student-supplied browser screenshots; a separate automated current-time live-site audit, browser `scrollWidth` measurement, and full keyboard activation test were not recorded.

- [Repository](https://github.com/blamowatkins/ASSESSMENT-Desert-Field-Notes-Starter)
- [Published home](https://blamowatkins.github.io/ASSESSMENT-Desert-Field-Notes-Starter/)
- [Published resources](https://blamowatkins.github.io/ASSESSMENT-Desert-Field-Notes-Starter/pages/resources.html)
