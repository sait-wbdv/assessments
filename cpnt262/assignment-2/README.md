# Assignment 2: Dynamic animals gallery
## Scenario
You're building a proof-of-concept gallery for a client. The gallery information will _eventually_ be served dynamically from a JSON API (which you will create later in 262). For now, you want to figure out the frontend component before dealing with the server.

## Instructions and Marking Rubric
This assignment will be marked out of a total of 10 points for the following:

### 2 points: `width` and `height` data
The included [`animals.js`](starter/js/animals.js) object lacks `width` and `height` data. 
1. Find the dimensions of each animal image located in the included [`images`](starter/images) directory, and
2. add these values as object properties to the corresponding image in [`animals.js`](starter/js/animals.js).

### 2 points: Link js as ES Modules
Two files have been provided in the [`js`](starter/js) directory.
1. `import` the `animals.js` array into `client.js`;
2. Link `client.js` as an ES Module (`type="module"`) to [`index.html`](starter/index.html).

### 4 points: Insert gallery of animal images into `.gallery` element
1. Using `Array.forEach()` (or similar), loop through the animals array and create an image card for each image that includes:
    - a `<figure class="card">` container;
    - an `<img>` element including `src`, `alt`, `width` and `height` attributes;
    - a `<figcaption>` element containing photo credit and link to Unsplash source.
2. Compile a list of these images and insert them into the `.gallery` element provided in [`index.html`](starter/index.html).

An example `figure` card has been provided in the `template` element located in [`index.html`](starter/index.html).

### 2 points: Design and esthetics
Include any CSS you need to:
- limit the max width of the gallery;
- layout the images responsively, centering the gallery on the page;
- preserve the aspect ratio of each image.

## Submission Requirements
- Push this assignment to a repo named `cpnt262-a2`. Include a README with the following:
  - Course title;
  - Author name;
  - Links to:
    - your GH repo;
    - your GH Pages demo;
    - the codepen you chose for this assignment.
  - Any comments that may help squeeze marks out of your instructor;
  - Attributions for any code or assets that are not your own.
- ZIP all files required for the site to operate and upload to Brightspace. 
- Leave a link to your GitHub repo as a comment in your Brightspace submission.

**Marks will be deducted for missing or incomplete README files.**