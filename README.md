# Uncommon HTML Bug: Accessing Non-Existent Property Before Rendering

This repository demonstrates an uncommon bug in HTML where attempting to access a non-existent property of an element that has not yet fully rendered results in an error.

## Bug Description

The bug occurs when a script tries to access a property of an HTML element before the browser has finished rendering the element.  This often happens if the script is placed in the `<head>` or at the beginning of the `<body>` before the targeted element is fully parsed and added to the DOM.

## Bug Reproduction

1. Open `bug.html` in a web browser.
2. Observe the error in your browser's console.

## Solution

The solution involves ensuring the script runs only after the document is fully loaded or the specific element is ready to be accessed.  This can be achieved using the `DOMContentLoaded` event or by wrapping the script in a function that checks for the element's existence.

See `bugSolution.html` for the corrected code.