# Assignment 4: Express Website
## Scenario
In the assignment, you'll create light-weight gallery website for a potential client of your choice (the client can be you). It will have a home page, subscribe page and gallery.

Besides the Gallery, the content of the pages will not directly be marked. You may use a third-party HTML template, a past project/assignment or create something new.

Toward that goal, in this assignment you will:
- Create a 3-page website served with rendered view engine templates.
- Fetch a list of gallery items using `fetch()`.
- Serve a JSON `GET /gallery` endpoint using `app.get()` and a custom module.

## Instructions
### Project Setup
- Initialize a new project using npm;
- Define the entry page as `server.js`
- Make sure that `node_modules` and `.env` is excluded from your repo using a `.gitignore` file.
- Install the following npm packages:
    - `express`
    - `ejs`, or other view engine

### Express setup
- Project directory structure:

    ```
    - public
    --- css
    --- js
    --- images
    - views
    --- partials7
    ----- header.ejs
    ----- nav.ejs
    ----- footer.ejs
    --- pages
    ----- index.ejs
    ----- subscribe.ejs
    ----- gallery.ejs
    - package.json
    - server.js
    ```

    You may add more but they will not be marked.

- `server.js`
  - Load the following packages:
    - npm packages above;
    - custom module containing your Gallery data (see below);
    - one npm module of your choice, to be used in a view(s).
  - Serve static assets from a `public` directory using the `express.static()` method.
  - Return 404 errors when a static file cannot be found.

### View Engine setup
- `server.js`:
  - set view engine to your chosen, loaded, package (EJS, Pug, etc)
- `view/partials`:
  - Move repeating page elements to template partials;
  - Minimum requirement: `header.ejs`, `nav.ejs` and `footer.ejs` to each be used included in at least two pages.
- `view/pages`
  - 3 root templates listed above;
  - Each page must output the following as injected template variables:
    - `title`: Page title;
    - `current`: A unique css class attached to the `body` element;
  - At least two pages must include partial templates.

### Rendered views
- Create 3 HTML (i.e. rendered) GET endpoints:
  - `index.ejs`: `GET /`
  - `subscribe.ejs`: `GET /subscribe`
  - `gallery.ejs`: `GET /gallery`
- For each endpoint:
  - Inject any needed variables;
  - Using `response.render()` send the rendered HTML to the client.
- Internal pages should highlight the current page in the navigation.

### Custom module
Create an image gallery that matches the theme of your website. You may adapt the image array used for Assignment 2, but you _cannot_ use the same images; make your own array that matches the theme of your website.
- Create a custom module that exports an array of 5-10 objects that contain the following fields:
    - `title`
    - `description`
    - `credit`
    - `image_path` (Lorem Picsum link by `id` are acceptable)
- Import this array into `server.js` using `require()`.
- For simplicity, this gallery array should closely match the one you were provided for Assignment 2.
- You _do not_ have to link to your images locally (but you can if you have the images available). You may use Lorem Picsum or some other service to use placeholder images.
- Only the text content needs to match the theme of your website. Images can be considered placeholders. The goal of this assignment is the use of an array of objects, not the processing of images.

### Gallery API
- Create the following JSON endpoint in `server.js`:
    
    ```
    GET /api/v0/gallery
    ```

- It should return a JSON response to the client that matches the array exported from your custom module.

### Asynchronous `fetch()`
- From `client.js`, request the JSON array from your new JSON endpoint using `fetch()`.
- Using the JSON response, `.forEach()` and `.innerHTML`, create an HTML gallery that matches the `figure`/`figcaption` card structure referenced in Assignment 2:

    ```html
    <figure class="card">
      <img src="[relative link to image]" alt="[image description]">
      <figcaption>[Image description with photo credit]</figcaption>
    </figure>
    ```
- The gallery should be responsive:
  - single column on mobile
  - three or more columns on desktop

### Deployment to Heroku
- Create an Heroku App.
- Connect your App to the Github repo of your static express app.
- Deploy your Heroku App.
- Server `PORT`: If `process.env.PORT` isn't found, use port 3000.

### Project documentation and code quality
- Include a `README.md` in your project that contains the following information:
  - Course title;
  - Author name;
  - Links to:
    - your GH repo;
    - your GH Pages demo;
    - the codepen you chose for this assignment.
  - Any comments that may help squeeze marks out of your instructor (maybe give him hints on where to look for the requirements above);
  - Attributions for any code or assets that are not your own.
- Use best practices with file/directory names, commenting and indentation.

## Submitting Your Assignment
In order to receive a grade, you must:
1. Deploy your Express app to Heroku.
2. Zip your project (excluding `node_modules` and `.env` file) and submit them to Brightspace.
3. Include links to the following as a comment with your Brightspace submission:
    - GH Repo
    - Deployed Heroku App URL

## Marking Rubric?
This assignment will be marked out of 20 points. Points will be given for each of the following, based on the requirements above:
- **1 point**: npm Project Setup
- **2 points**: Express setup
- **2 points**: View Engine setup
- **3 points**: Rendered views
- **3 points**: Custom gallery module
- **2 points**: Gallery JSON API
- **3 points**: Asynchronous gallery `fetch()`
- **2 points**: Deployment to Heroku
- **2 points**: Project documentation and code quality