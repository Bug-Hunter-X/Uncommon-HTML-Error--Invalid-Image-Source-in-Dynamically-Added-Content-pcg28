# Uncommon HTML Error: Invalid Image Source in Dynamically Added Content

This repository demonstrates an uncommon HTML error related to dynamically adding content using `innerHTML` and an invalid image source.  The error may not always be immediately obvious since the surrounding content renders correctly.

## Bug Description

A paragraph and an image are dynamically added to a div using `innerHTML`. The image uses an invalid source, which is a relatively subtle issue.  Browsers handle this by not rendering the image, sometimes producing empty space in place of the expected image, or causing errors in certain cases.

## How to Reproduce

1. Clone this repository.
2. Open `bug.html` in your web browser.
3. Observe that while the paragraph renders correctly, the image does not appear due to the invalid source `invalid-image.jpg`.

## Solution

The solution involves proper error handling.  Check if the image source is valid before attempting to render it. You can do this by using the `onerror` event of the image element or, in this case, using a more robust method of updating the DOM content that can handle error scenarios more gracefully.

Open `solution.html` to see a corrected version.

This highlights the importance of carefully managing dynamically generated HTML content to prevent unexpected behavior and subtle errors.