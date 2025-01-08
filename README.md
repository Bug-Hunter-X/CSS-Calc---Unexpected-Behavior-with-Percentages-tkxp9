# CSS Calc() Unexpected Behavior with Percentages

This repository demonstrates an uncommon error that can occur when using the CSS `calc()` function with percentages and other units.  The issue arises from the order of operations and the way percentages are calculated relative to their parent container.

## The Problem

When subtracting a percentage from a fixed unit (like pixels) within a `calc()` expression, the percentage is calculated based on the *parent container's* width, not the fixed unit. This often leads to unexpected and incorrect results.

## Reproducing the Bug

The `bug.css` file contains CSS code demonstrating this issue.  You will see that a div does not have the expected width because of an incorrect `calc()` usage.

## The Solution

The correct way to use `calc()` in such situations is to always ensure that the order of operations prioritizes the subtraction of the fixed value from the percentage, allowing for the percentage calculation to be based on the available space after the subtraction of the fixed units.  The `bugSolution.css` demonstrates the correct usage.

## How to run the example

Simply open the `index.html` file in your browser. You'll see two divs which demonstrate the incorrect and correct behaviors.