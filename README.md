# Uncommon HTML Bug: Premature DOM Manipulation

This repository demonstrates a subtle bug that can occur in HTML when JavaScript interacts with the Document Object Model (DOM) before the entire page has finished loading.  The bug is characterized by the JavaScript failing silently or producing unpredictable results.  The solution illustrates how to avoid this error using event listeners or ensuring the script runs after the DOM is ready.

## Bug Description:

The script attempts to access and modify the `myDiv` element using `document.getElementById` *before* the element is fully parsed and added to the DOM. This typically happens when the script is placed in the `<head>` section of the HTML document.

## Solution:

The solution uses the `DOMContentLoaded` event listener to ensure the script only runs after the entire HTML document has been parsed and the DOM is ready.