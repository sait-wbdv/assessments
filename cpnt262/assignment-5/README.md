# Assignment 5: JSON Server with Heroku and MongoDB Atlas
## Scenario
You are taking part in a hypothetical project with multiple developers. You've been tasked with setting up a dedicated JSON server for the project, similar in functionality to [JSON Placeholder](https://jsonplaceholder.typicode.com/). 

For the purposes of this assignment, your application will be returning JSON objects of your choice. The only restriction is they cannot be objects that have been covered in class (i.e. animals).

### Project Setup
- Initialize a new project using npm;
- Define the entry page as `server.js`
- Make sure that `node_modules` and `.env` is excluded from your repo using a `.gitignore` file.
- Project directory structure:

    ```
    - seeds
    - models
    - import.js
    - package.json
    - server.js
    ```

    You may add more but they will not be marked.

- `server.js`
  - Install the following npm packages:
    - `express`
    - `mongoose`
    - `dotenv`
  - Serve the JSON endpoints listed below;
  - Return a `404 File not found` message when an object cannot be found.

### JSON API endpoints
1. Import your data into a MongoDB Atlas collection using a method of your choice. A sample `import.js` script has been provided.
    - Create a Mongoose model for your objects.
    - `require()` a compiled model into `server.js` to request the data for the endpoints listed below.
2. Create the following JSON endpoints in `server.js`:
    - `GET /api/v0/[objects]`
        - Replace `[objects]` with an endpoint of your choice that has not been covered in class. Examples: `users`, `invoices`, `cars`, etc. The endpoint should be the plural version of the object.
        - Return a JSON array of 5-10 `[objects]` with the following properties:
            - `id`
            - `title` or `name`
            - `description`
        - add any additional properties that apply to your project.
    - `GET /api/v0/[objects]/:id`
        - Returns the appropriate JSON object based on the `:id` specified in the request URL.

### Deployment to Heroku and MongoDB Atlas
- Deploy your Heroku App.
- Server `PORT`: If `process.env.PORT` isn't found, use port 3000.
- Set appropriate `Config Vars` with your `MONGODB_URL` connection string.
- If neccessary, add appropriate CORS headers to allow for cross-domain requests.

### Project documentation and code quality
- Include a `README.md` in your project that contains the following information:
  - Course title;
  - Author name;
  - **The GET Endpoints** (with heroku domain) that your instructor will be testing.
  - Links to your GH repo;
  - Any comments that may help squeeze marks out of your instructor (maybe give him hints on where to look for the requirements above);
  - Attributions for any code or assets that are not your own.
- Use best practices with file/directory names, commenting and indentation.

## Submitting Your Assignment
In order to receive a grade, you must:
1. Deploy your Express app to Heroku and MongoDB Atlas.
2. Zip your project (excluding `node_modules` and `.env` file) and submit them to Brightspace.
    - include a copy of the database seed (the array of objects) you used for this project so your instructor can recreate your database, if needed.
3. Include links to the following as a comment with your Brightspace submission:
    - GH Repo
    - Deployed Heroku App URL

## Marking Rubric
This assignment will be marked out of 10 points. Points will be given for each of the following, based on the requirements above:
- **2 point**: Project Setup
- **3 points**: JSON API endpoints
- **3 points**: Deployment to Heroku and MongoDB Atlas
- **2 points**: Project documentation and code quality
