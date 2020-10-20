# Codepen `init()`
## Instructions
### Basic `index.html`
1. Find a fun/interesting/engaging Codepen that:
    - uses HTML, CSS (not SCSS) and Javascript
    - affects the DOM in some way using Javascript.
2. Create a valid `index.html` file, in a new project folder.
3. Copy the code from the HTML panel of your chosen Codepen and paste it inside the `body` element.
4. Copy the code from the CSS panel and paste it into `css/main.css` in the root of your project directory
5. Link your external style sheet (using the `link` element) in the `head` of `index.html`.
6. Copy the code from the JS panel and paste it into `js/client.js` in the root of your project directory.
7. Link your external Javascript file (using a `script` element) **inside the `head` element**.
8. Test your new page in Live Server (or just open `index.html` in your browser).

### `init()` implementation
The `index.html` as you've created it, may not work if the Javascript tries to use a DOM element before the page has loaded. In addition, your Javascript code is sitting within the global execution context.

Fix this by:
1. Wrapping the Javascript code, contained within `js/client.js`, inside a function named `init()`.
2. Using `window.addEventListener()` and the `load` event, invoke this new `init` function when the page has finished loading.

## Project README
Include a `README.md` in your project that contains the following information:
- Course title;
- Author name;
- Links to:
  - your GH repo;
  - your GH Pages demo;
  - the codepen you chose for this assignment.
- Any comments that may help squeeze marks out of your instructor;
- Attributions for any code or assets that are not your own.

## Submission Requirements
- Push this assignment to a repo named `cpnt262-a1`.
- ZIP all files required for the site to operate and upload to Brightspace. 
- Leave a link to your GitHub repo as a comment in your Brightspace submission.

## Marking Rubric
This assignment will be marked out of 10 points. Points will be awarded for the following:

### Demo functionality: 4 points
- Your GH Pages demo operates identically to the chosen codepen. 2 points will be deducted if you embed CSS and JS in your `index.html` page. 
- If you **have not** implemented your `init` function (see below) and have, instead, linked your Javascript before the closing `</body>` tag, 4 points will be given for this portion of the assignment.

### `init()` implementation: 4 points
In addition to having a working demo, your code is implemented using an `init()` function as described in the requirements above.

### Project README: 2 points
Your project has an included README file as described in the requirements above.