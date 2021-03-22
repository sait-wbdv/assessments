# Assignment 5: JSON Routes with Heroku and MongoDB Atlas
## Scenario
In this assignment, you will refactor/upgrade the project you submitted for Assignment 4:
- Create a Mongoose model for your JSON gallery route
- Migrate the data in your custom gallery module to MongoDB Atlas
- Connect Heroku app to an Atlas database
- Create a single image endpoint to your app

## Setup Requirements
- Initialize a new project using npm;
- Define the entry page as `server.js`
  - Install the following npm packages (plus any other you may need):
    - `express`
    - `ejs`
    - `mongoose`
    - `dotenv`
- Make sure that `node_modules` and `.env` is excluded from your repo using a `.gitignore` file.
- `server.js` setup
  - Return a custom `404 File not found` page when an route cannot be found.
  - Server `PORT`: If `process.env.PORT` isn't found, use port 3000.

---

## Recommended Directory Structure

```
project-root
  └─ models
      └─ image.js
  └─ public
  └─ routes
      └─ image.js
  └─ seeds
      └─ images.js
  └─ views
      └─ single-item.ejs
  ├─ import.js
  ├─ package.json
  └─ server.js
```
    
- Files from Assignment 4 not included (but should be, when appropriate).
- You may add more but they will not be marked.

---

## Criteria
3 points will be given for each of the following criteria, for a total of 15 points

### 1. Gallery `mongoose` model
- Create a Mongoose model for your gallery.
  - `id` - Unique identifier (`number`);
  - `title` - Image heading (`string`);
  - `description` - Image description (`string`: 10-25 words);
  - `width` - Image width in pixels (`number`);
  - `height` - Image height in pixels (`number`);
  - `pathURL` - a local path/filename to your image file(`string`);
  - add any additional properties that apply to your project.
- `server.js` 
  - Load model using `require('./models/image.js')`
  - Connect to MongoDB Atlas using `MONGODB_URL`
      - Log connection errors to the console. 
      - Log "Connected to DB..." to the console on successful connection.
      - Respond with custom `500 Internal Server` error page if connection fails
- Migrate `GET /api/v0/images` route to use Mongoose/Atlas data instead of custom module.
- Image cards link to `GET /images/:id` route below
  - Example: `https://[app-domain].herokuapp.com/images/3`

### 2. Rendered single image route
- `GET /images/:id`
  - Returns the appropriate rendered view of the single image based on the `:id` specified in the request URL.
  - Error handling for:
    - non-existent `id`s (including malformed `id`s such as `String` when `Number` was expected)
    - custom `404 File not found` page (should be same as above) when an route cannot be found.
  - Populates data from MongoDB Atlas using Mongoose model
  - `single-item.ejs` view to be rendered
    - incorporates the following template variables
      - Site title
      - Page title
    - Incorporates the same template partials from Assignment 4 (at minimum: `head.ejs`, `header.ejs` and `footer.ejs`)
- Load route as a separate module using `require('./routes/image.js')`

### 3. Database Import
- Import your data into a MongoDB Atlas collection using a method of your choice. A sample `import.js` script will be provided.
- Create a database seed file (the array of objects) you used for this project so your instructor can recreate your database, if needed.
  - Place this file in a `seeds` directory.
  - Delete legacy `data` directory from Assignment 4

### 4. Heroku/Atlas Deployment
- Deploy your app to Heroku.
- Create DB user credentials
  - `read/write` access permissions
- Whitelist IPs 
- Set appropriate `Config Vars` with your `MONGODB_URL` connection string.
- If necessary, add appropriate CORS headers to allow for cross-domain requests.

### 5. Documentation and Code Quality
- Include a `README.md` in your project that contains the following information:
  - Course title;
  - Author name;
  - **The GET Endpoints** (with heroku domain) that your instructor will be testing.
  - Links to
      - GH repo
      - Deployed Heroku App URL
  - Any comments that may help squeeze marks out of your instructor (maybe give him hints on where to look for the requirements above);
  - Attributions for any code or assets that are not your own.
- Use best practices with file/directory names, commenting and indentation.

---

## Submitting Your Assignment
In order to receive a grade, you must:
1. Deploy your Express app to Heroku and MongoDB Atlas.
2. Zip your project (excluding `node_modules` and `.env` file) and submit them to Brightspace.
    - include a copy of the database seed (the array of objects) you used for this project so your instructor can recreate your database, if needed.
3. Include links to the following as a comment with your Brightspace submission:
    - GH Repo
    - Deployed Heroku App URL
    - **Connection string for `MONGODB_URL`**
