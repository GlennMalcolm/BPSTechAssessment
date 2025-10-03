# Proposed Maintenance Tasks

## Typo Fix
- **Issue**: The CSS comment labeling the year group elements refers to them as "tiles", but the implementation styles interactive `<button>` controls; the terminology mismatch can confuse future contributors.
- **Task**: Update the comment to describe the elements as "buttons" to match the actual markup and styling. (File: `index.html`, lines 59-64.)

## Bug Fix
- **Issue**: The page lacks a responsive viewport meta tag, which causes the layout to scale poorly on mobile devices because browsers render it at desktop widths by default.
- **Task**: Add `<meta name="viewport" content="width=device-width, initial-scale=1.0">` to the `<head>` so the grid resizes correctly on phones. (File: `index.html`, lines 5-88.)

## Documentation/Comment Discrepancy Fix
- **Issue**: The color variables section comment lists only "Patana Colours", yet it also defines a generic `--white` token that is not part of the referenced palette, which can mislead readers about the variable's origin.
- **Task**: Clarify the comment so that it documents `--white` as a neutral utility color separate from the Patana palette. (File: `index.html`, lines 8-14.)

## Test Improvement
- **Issue**: There are no automated checks ensuring the six year-group buttons render with accessible names, leaving regressions undetected.
- **Task**: Introduce a lightweight UI test (for example, with Playwright) that loads the page and asserts the presence of buttons labeled "Year 1" through "Year 6". (File: `index.html`, lines 69-74.)
