# Uncommon HTML Error: Accessing DOM Element Before It Exists

This repository demonstrates a common yet easily missed error in HTML/JavaScript: attempting to access and modify a DOM element before it has been fully loaded by the browser. 

The `bug.html` file contains the erroneous code, and `bugSolution.html` provides the corrected version.

The error occurs because JavaScript executes before the HTML is fully parsed.  Therefore, `document.getElementById('myDiv')` returns `undefined` when it is first called, leading to the `TypeError`. 

**Solution:** The solution involves ensuring that the script that accesses the DOM element is either placed at the end of the `<body>` or wrapped within a `DOMContentLoaded` event listener.