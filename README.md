# Inconsistent border-box rendering in CSS

This repository demonstrates a subtle CSS bug related to the `box-sizing: border-box;` property and its inconsistent application across different browsers.  The issue revolves around the unexpected behavior of a div element's width and height when a border is applied.

## Bug Description

A div element with `width: 50%;`, `height: 50%;`, and `box-sizing: border-box;` should occupy 50% of its parent's width and height, inclusive of the border. However, certain browsers may not handle this correctly, leading to unexpected rendering where the element's size exceeds 50% because the border is not factored into the calculation correctly by the browser.

## Solution

The solution involves using a more robust approach to handle the border width to ensure consistent rendering across browsers.  This may involve using a different technique like calculating the border size and subtracting it from the desired width/height. This may also involve using CSS variables to simplify the code and make it easier to maintain.

## How to reproduce

1. Clone this repository.
2. Open `bug.html` in different browsers.
3. Observe the differences in the size of the div element.
4. Compare `bug.css` and `bugSolution.css` for the solution.