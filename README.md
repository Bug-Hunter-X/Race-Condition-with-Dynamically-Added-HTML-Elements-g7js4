# Uncommon HTML Bug: Race Condition with Dynamically Added Elements

This repository demonstrates a subtle bug that can occur when working with dynamically added HTML elements and the `innerHTML` property.

The `bug.html` file showcases the issue.  The code creates a new div element and attempts to set its `innerHTML` property immediately after appending it to the DOM. This can fail if the browser hasn't fully added the element to the DOM before the `innerHTML` assignment is executed, leading to the new text not being rendered.

The `bugSolution.html` demonstrates the correct way to handle this by using `requestAnimationFrame` which guarantees that the code runs after the DOM updates are complete, solving the timing issue. 

This is a less common error, but important to understand for robust and reliable JavaScript/HTML interactions.