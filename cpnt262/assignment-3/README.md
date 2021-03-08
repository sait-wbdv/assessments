# Assignment 3: Deployed Static Express Website
You built a static gallery website for [Assignment 2](../assignment-2) that will _eventually_ be served dynamically from a JSON API. 

Toward that goal, in this assignment you will:
- Initialize a new `npm` project for your website;
- Install and load the `express` web framework;
- Use `express.static()` middleware to serve your static website from Assignment 2;
- Setup a custom 404 error page;
- Deploy this website to a live Heroku server.

## Criteria
2 points will be given for each of the following criteria, for a total of 10 points:

### 1. `npm` Project Setup
- Initialize a new project using npm;
  - Define the entry page as `server.js`
  - Define a `start` script that runs the command: `node server.js` (this is done by default with newer versions of `npm`).
  - Install the following modules:
    - `dotenv`
    - `express`
- Ensure that `node_modules` and `.env` is excluded from your repo using a project `.gitignore` file.

### 2. Server Setup
- Import the `express` npm package with `require()`.
- Serve static assets from a `public` directory using `express.static()` middleware.
- Server port
  - When starting the server, use a default port of `3000` when `process.env.PORT` is not found.
  - Define your development port as port `3000` in an environment variable file (i.e. a `.env` file).
  - Import this port environment variable using the `dotenv` package.

### 3. Custom 404 page
- Using a method of your choice, return a custom 404 page when a static file cannot be found.
- File must include a `404` response code.
- Page must be a valid HTML page.
- User should be redirected to a `404.html` or `/404` url or similar.

### 4. Heroku deployment
- Create a free Heroku account.
- Create an Heroku App.
- Connect your App to the Github repo of your static express app.
- Deploy your Heroku App.

### 5. Documentation and Code Quality
1. Include a `README.md` in your project that contains the following information:
    - Course title;
    - Author name;
    - Links to:
      - GH repo;
      - Deployed Heroku URL
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
- Push this assignment to a repo named `cpnt262-a3`.
- ZIP all files required for the site to operate and upload to Brightspace. 
- Leave a link to the following as a comment in your Brightspace submission:
  - GH repo
  - Deployed Heroku URL