# Node Final - Deployed Product/Services Website
## Details
In this assignment, your group will deploy a multi-page, database-driven Product website using Express, EJS (or similar view engine) and Mongoose. It will be deployed to Heroku and MongoDB Atlas.

## Instructions
This website will sell/advertise new products/services of your choice that you have not covered in prior assignments in 262.

Note: Since this is not an HTML/CSS assignment, visual components such as hero sections, footers, logos etc may be reused from prior assignments and projects. Only the theme/product/service of the website must be unique for the purposes of Mongoose model creation. Existing images may be considered placeholders but **must be served locally** (no lorem picsum).

Design elements will be ignored for this assignment with the exception of:
- Accessible and responsive navigation
- Accessible forms
- Accessible and semantic images
- Responsive galleries and card layouts

Aside from the endpoints and features defined below, you may layout and organize your site as you feel appropriate. 

BUT, please make sure your instructor doesn't have to hunt to find your code...

### Project setup
- Initialize a new project using npm.
- Dependencies:
  - `express`
  - `ejs` (or similar)
  - `dotenv`
  - `mongoose`
- Serve static assets from a `public` directory.
- Return a custom 404 page when a file (or endpoint) cannot be found.
- Mongoose connection authenticated using `.env` file.
  - .on event for errors
  - .once event for successful connection

### EJS View Setup
All static HTML should be served with EJS (or similar) view templates. For each page of your site using either EJS or Pug:
- Repeating page elements (`head`,`header`,`nav`,`footer`, etc) moved to separate template "partials" in a `views/partials` directory.
- Root page views should be stored in a separate `views/pages` directory.

### HTML Endpoints
Create HTML endpoint handlers to render and serve the following pages using `ejs`:
- `GET /`
- `GET /subscribe`
  - Contains subscribe form:
    - Fields
      - `name`
      - `email`
      - `action="[POST endpoint]"`
      - `method="post"`
  - Returns with a custom message, repeating the name and email, confirming they are subscribed.
- `GET /gallery`
  - lists 5-10 products/services of your choice with a minimum of the following fields:
    - `id`
    - `name` or `title`
    - `description`
  - Built client-side with a `fetch()` call to a JSON endpoint (listed below)
- `GET /gallery/:id` (`:id` could be some other unique identifier)
    - Displays a single product/service from the above list. This should be rendered server-side with `ejs`.
- `GET /team`
  - Displays a list of each of your team members.
  - If you are in a group of 4, this page should be built client-side with a `fetch()` call to a JSON endpoint (listed below). If not, this may be static view rendered using EJS (no database functionality needed).
- `GET /admin`
  - Lists the subscribers who have submitted the `/subscribe` form. This does not need to be password protected (we'll pretend).

### Schema/model implementations
- Define the following Mongoose Schemas in a dedicated `/models` directory:
  - `gallery`: The product/service you are selling/advertising. This may be renamed to match your chosen theme.
  - `member`: Your group members, to be listed on your Team page.
  - `subscriber`: Subscribers to your mailing list.
- Based on the above schema, `require()` your compiled models into your app.
- Remember, the above singular noun will determine the name of your MongoDB collection. It will be the plural of the noun (i.e. `galleries`, `members` and `subscribers`).

### JSON Endpoints
Create the following JSON endpoints to serve your frontend views:
1. Products/Services gallery
  - `GET /api/v0/gallery`
  - Note: the `GET /gallery/:id` endpoint should be rendered server-side with a view.
2. Subscribers list
  - `POST /api/v0/subscribers`
  - `GET /api/v0/subscribers`
3. Team members (if in a group of 4)
  - `GET /api/v0/members`

### Frontend `fetch()` implementation
Create appropriate frontend `fetch()` requests for the following JSON endpoints defined above:
- Requests `GET /api/v0/gallery` for `GET /gallery`
- Requests `GET /api/v0/subscribers` for `GET /admin`
- Requests `GET /api/v0/members` for `GET /team`

For each `fetch()` request, build a corresponding gallery/list using `/.forEach()` or similar method. Example card design for Gallery and Team pages (Admin can be an unordered list): 

```html
<figure>
  <img src="#" alt="figure">
  <figcaption>Figure</figcaption>
</figure>
```

### DB seeds
Your instructor may need to build a local version of your database to mark this assignment.
- include a `./seeds` directory containing the objects you've defined Models for. 

## Submitting Your Assignment
In order to receive a grade, you must:
1. Deploy your Express/Mongoose app to Heroku and Atlas.
2. Zip your project (NOT including `node_modules` nor `.env`) and submit them to Brightspace.
3. In a comment with your Brightspace submission, include links to:
    - your GitHub repo (i.e: [`animals-heroku-atlas`](https://github.com/cprg210/animals-heroku-atlas));
    - deployed site (i.e. [https://animals-heroku-atlas.herokuapp.com/](https://animals-heroku-atlas.herokuapp.com/)).

### Project documentation and code quality
- Include a `README.md` in your project that contains the following information:
  - Course title;
  - Team members;
  - Links to 
    - your GH repo;
    - deployed Heroku app.
  - Any comments that may help squeeze marks out of your instructor (maybe give him hints on where to look for the requirements above);
  - Attributions for any code or assets that are not your own.
- Use best practices with file/directory names, commenting, code quality and indentation.

## Submitting Your Assignment
In order to receive a grade, you must:
1. Deploy your Express app to Heroku and MongoDB Atlas.
2. Zip your project (excluding `node_modules` and `.env` file) and submit them to Brightspace.
    - include a copy of the database seeds used for this project so your instructor can recreate your database, if needed.
3. Include links to the following as a comment with your Brightspace submission:
    - GH Repo
    - Deployed Heroku App URL

## Marking Rubric
This assignment will be marked out of a total of 25 points. 5 points will be given for the following, based on the requirements above:
- EJS View Setup
- HTML Endpoints
- Schema/model implementation
- JSON Endpoints
- Frontend `fetch()` implementation