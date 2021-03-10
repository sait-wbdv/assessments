# Assignment 4: Express Gallery Website
## Scenario
In the assignment you will:
- Create a 3-page website served with rendered view engine templates.
- Fetch a list of gallery items using `fetch()`.
- Serve a JSON `GET /gallery` endpoint using `app.get()` and a custom module.

Besides the Gallery, the content of the pages will not directly be marked. You may use a third-party HTML template, a past project/assignment or create something new.

---

## Criteria
3 points will be given for each of the following criteria, for a total of 15 points:

### 1. Server setup
- Project directory structure:

    ```
    project-root
    └── assets
        ├── css
        ├── images
        └── js
    └── views
        └── partials
            ├── footer.ejs
            ├── header.ejs
            └── nav.ejs
        └── pages
            └── index.ejs
            ├── login.ejs
            └── register.ejs
    ├── package-lock.json
    ├── package.json
    └── server.js
    ```

    You may add more but they will not be marked.

- `server.js`
  - Load the following packages:
    - `express`
    - `ejs`/`pug`
    - custom module containing your Gallery data (see below);
    - one npm module of your choice, to be used in your view(s).
  - Serve static assets from a `public` directory using the `express.static()` method.
  - Return 404 errors when a static file cannot be found.

### 2. Views
- Load a view engine (`ejs`, `pug`)
- HTML Endpoints
  - Create the following HTML endpoints, served with rendered views:
    - `GET /`
    - `GET /login`
      - Login form does not need to be operable.
    - `GET /register`
      - Register form does not need to be operable.
- Each page must incorporate the following template variables:
  - Site title;
  - Page title;
- View partials:
  - Move repeating page elements to template partials;
  - Minimum requirement: `header.ejs`, `nav.ejs` and `footer.ejs` to each be used included in at least two pages.
  - At least two pages must include partial templates.
- View must incorporate one other `npm` module mentioned in "Server Setup"

### 3. Gallery JSON API
Using your gallery from Assignment 2 (modifications are welcome):
- Migrate your frontend Javascript array to a custom Node module.
  - Required object properties:
    - `id` - Unique identifier (`number`);
    - `title` - Image heading (`string`);
    - `description` - Image description (`string`: 10-25 words);
    - `width` - Image width in pixels (`number`);
    - `height` - Image height in pixels (`number`);
    - `pathURL` - a local path/filename to your image file(`string`);
    - `linkURL` - 3rd party web page that the image links to (`string`; example: wikipedia entry relating to the image);
    - `credit` - The photo credit for the image such as a person, company or website (`string`).
    - `creditURL` - A link to the original photo, photographer's home page, license details, etc (`string`).
- Create the following JSON endpoint: `GET /api/v0/gallery` (or similar)
  - Return a JSON response to the client that matches the array exported from your custom module.
- Using `fetch()` on the frontend, request your gallery array using your JSON endpoint.
  - Refactor your gallery loop to use the fetched JSON array.
  - The gallery should be:
    - responsive
    - 9-12 images
    - semantically marked up

### 4. Deployment to Heroku
- Create an Heroku App.
- Connect your App to the Github repo of your static express app.
- Deploy your Heroku App.
- Server `PORT`: If `process.env.PORT` isn't found, use port 3000.

### 5. Documentation and Code Quality
- Include a `README.md` in your project that contains the following information:
  - Course title;
  - Author name;
  - Links to:
    - your GH repo;
    - your deployed Heroku domain;
  - Any comments that may help squeeze marks out of your instructor (maybe give him hints on where to look for the requirements above);
  - Attributions for any code or assets that are not your own.
- Use best practices with file/directory names, commenting and indentation.

---

## Submitting Your Assignment
In order to receive a grade, you must:
1. Deploy your Express app to Heroku.
2. Zip your project (excluding `node_modules` and `.env` file) and submit them to Brightspace.
3. Include links to the following as a comment with your Brightspace submission:
    - GH Repo
    - Deployed Heroku App URL
