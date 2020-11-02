# Assignment 3: Deployed Static Express Website
## Scenario
You built a proof-of-concept website for [Assignment 2](../assignment-2) that will _eventually_ be served dynamically from a JSON API. 

Toward that goal, in this assignment you will:
- install and load `express` to host a simple website;
- use the `express.static()` method to serve a static website, of your choice, that you have built in this program thus far;
- deploy this website to a live Heroku server.

## Instructions
### npm Project Setup
- Initialize a new project using npm;
- Define the entry page as `server.js`
- Define a `start` script that runs the command: `node server.js`.
- Make sure that `node_modules` is excluded from your repo using a project `.gitignore` file.

### Express setup
- Install and load the `express` npm package.
- Serve static assets from a `public` directory using the `express.static()` method.
- Return 404 errors when a static file cannot be found.

### Local port environment variable
- Define your development port as port `8080` in an environment variable file (i.e. a `.env` file).
- Import this port environment variable using the `dotenv` package.
- Make sure that files with the `.env` extension are excluded from your repo using a `.gitignore` file.
- If a port environment variable isn't found, set a default port of 8080 in `server.js`.

### Heroku server setup
- Create a free Heroku account.
- Create an Heroku App.
- Connect your App to the Github repo of your static express app.
- Deploy your Heroku App.

### Project documentation and code quality
- Include a `README.md` in your project that contains the following information:
  - Course title;
  - Author name;
  - Links to:
    - your GH repo;
    - your GH Pages demo;
    - the codepen you chose for this assignment.
  - Any comments that may help squeeze marks out of your instructor;
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
This assignment will be marked out of 10 points. 2 points will be given for each of the following, based on the requirements above:
1. npm Project Setup
2. Express setup
3. Local port environment variable setup
4. Heroku server setup
5. Project documentation and code quality