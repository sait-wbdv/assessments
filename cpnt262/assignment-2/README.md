# Assignment 2: Dynamic Image Gallery
In this assignment you'll be refactoring your past gallery assignment into a Javascript-driven gallery:
- Gallery information will be stored in an array of objects;
- The array will be converted to HTML using a loop;
- The HTML elements will be outputted to an HTML page.

You may use the same images you used for CPNT 260 Assignment 3 or you can choose different ones. All images must be openly licensed or your own works.

## Criteria
This assignment will be marked out of 10 points according to the following requirements:

### 1. Image Array: 2 Points
- Array of 9-12 image object literals, declared as a `const` variable.
- For each image object, store the following information:
  - `id` - Unique identifier (`number`);
  - `title` - Image heading (`string`);
  - `description` - Image description (`string`: 10-25 words);
  - `width` - Image width in pixels (`number`);
  - `imgURL` - 3rd party web page that the image links to (`string`; example: wikipedia entry relating to the image);
  - `credit` - The photo credit for the image such as a person, company or website (`string`).
  - creditURL - A link to the original photo, photgrapher's home page, license details, etc (`string`).

### 2. Array Loop and Output: 4 Points
- Using `Array.prototype.forEach()` or similar method/statement, loop through the image array and output to an HTML page.
- Within each loop iteration, either:
  - output image information directly to an HTML gallery, OR
  - append to an `output` variable to be outputted at the end of the loop.
- HTML output can be achieved with either:
  - `Element.innerHTML`;
  - Direct DOM manipulation (i.e. `Document.createElement()`, etc);
  - the use of a `<template>` element.
- Gallery HTML should be valid and semantic (i.e. `figure`/`figcaption` elements or similar).
- All information contained in the object should be used. 
- Photo credit information can be displayed once on the page if it is the same for all images (but still must be included in the image objects)

### 3. Setup and Deployment: 2 points
- Images
  - Images must be locally hosted with your project.
  - Image resolution should be appropriate for the final display size in the viewport.
  - The gallery must be responsive and accessible.
- Javascript
  - Javascript must be linked in the `head` of the document and located in a dedicated `js` directory. Optional: 
  - Javascript must use _strict_ mode.
  - There must be no JS errors or warnings (except for favicon).
- CSS
  - CSS must be linked as an external stylesheet in the `head` of the document and located in a dedicated `css` directory.
  - While the goal of this assignment is not design, points will be deducted for accessibility/usability issues.

### 4. Documentation and Code Quality: 2 Points
1. Include a `README.md` in your project that contains the following information:
    - Course title;
    - Author name;
    - Links to:
      - GH repo;
      - GH Pages site
    - Some context/hints on where to look for the requirements above.
    - Attributions for any code or assets that are not your own.
2. Use best practices with [file/directory names](https://sait-wbdv.github.io/winter-2021/cheatsheets/naming-conventions/), commenting and indentation:
    - 2 spaces per indent.
    - CamelCase naming conventions followed.
    - Statements ended with semi-colons.
    - Code is well-commented.
    - See [JavaScript Style Guide](https://www.w3schools.com/js/js_conventions.asp) for full list.

---

## Submission Requirements
- Push this assignment to a repo named `cpnt262-a2`.
- ZIP all files required for the site to operate and upload to Brightspace. 
- Leave a link to the following as a comment in your Brightspace submission:
  - GH repo
  - GH Pages site
