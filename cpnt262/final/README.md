# Node Final Group Project - Deployed Product/Services Website
In this assignment, your group will deploy a multi-page, database-driven Product website using Express, EJS (or similar view engine) and Mongoose. It will be deployed to Heroku and MongoDB Atlas.

## Instructions
This website will sell/advertise new products/services of your choice that you have not covered in prior assignments in this program.

Note: Since this is not an HTML/CSS assignment, visual components such as hero sections, footers, logos etc may be reused from prior assignments and projects. Only the theme/product/service of the website must be unique for the purposes of this assignment. Existing images may be considered placeholders but **must be served locally** (no lorem picsum).

Design elements will be ignored for this assignment with the exception of:
- Accessible and responsive navigation
- Accessible forms
- Accessible and semantic images
- Responsive galleries and card layouts

Aside from the required endpoints and features defined, you may layout and organize your site as you feel appropriate. 

BUT, please make sure your instructor doesn't have to hunt to find your code...

### Project Setup
While not explicitly listed as assignment criteria, marks will be deducted for projects that are not properly deployed.
- Initialize a new project using npm.
- Dependencies:
  - `express`
  - `ejs` (or similar)
  - `dotenv`
  - `mongoose`
  - Fancy feature (see below) 
- Serve static assets from a `public` directory.
- Return a custom 404 page when a file (or endpoint) cannot be found.
- Mongoose connection authenticated using `.env` file.
  - .on event for errors
  - .once event for successful connection

---

## Example Directory Structure

```
project-root
  ├─ models
      ├─ image.js
      ├─ subscriber.js
      └─ team-member.js
  ├─ public
  ├─ routes
      ├─ api-v0.js
      ├─ index.js
      └─ gallery.js
  ├─ seeds
      ├─ images.js
      ├─ subscribers.js (if used)
      └─ team-members.js
  ├─ views
      ├─ admin.ejs
      ├─ gallery-item.ejs
      ├─ gallery-list.ejs
      ├─ index.ejs
      ├─ subscribe.ejs
      └─ team.ejs
  ├─ import.js
  ├─ package.json
  └─ server.js
```

- This is an example structure. You may diverge from this as long as none of your route handlers are in `server.js`.

---

## Criteria
5 points will be given for each of the following criteria, for a total of 25 points:

### 1. Rendered HTML Endpoints
Create HTML route handlers to render and serve the following pages using `ejs` (or similar):
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
  - lists 9-12 products/services/items of your choice with a minimum of the fields listed in the Model in the next section.
  - Client-side `fetch()` calls to a JSON endpoint (listed below)
- `GET /gallery/:id` (`:id` could be some other unique identifier)
    - Displays a single product/service from the above list. This should be rendered server-side with `ejs`.
- `GET /team`
  - Displays a list of each of your team members.
  - If you are in a group of 4, this page should be built client-side with a `fetch()` call to a JSON endpoint (listed below). For groups of 3, this may be static view rendered using EJS (no database functionality needed).
- `GET /admin`
  - Displays a list of your subscribers.
- All static HTML should be served with EJS (or similar) view templates. For each page of your site using either EJS or Pug:
  - Repeating page elements (`head`, `header`, `footer`, etc) moved to separate template "partials" in a `views/partials` directory.
  - Root page views should be stored in a separate `views/pages` directory.

### 2. Schema/model implementation
- Define the following Mongoose Schemas in a dedicated `/models` directory:
  - `gallery`: The product/service you are selling/advertising. This may be renamed to match your chosen theme.
    - `id`
    - `name` or `title`
    - `description`
    - `imageSrc`
    - `width`
    - `height`
  - `member`: Your group members, to be listed on your Team page.
    - `name`
    - `profilePic`
    - `title`
    - `bio`
    - `github`
  - `subscriber`: Subscribers to your mailing list.
    - `name`
    - `email`
- Based on the above schema, `require()` your compiled models into your app.
- Remember, the above singular noun will determine the name of your MongoDB collection. It will be the plural of the noun (i.e. `galleries`, `members` and `subscribers`).

#### DB seeds
Your instructor may need to build a local version of your database to mark this assignment.
- include a `./seeds` directory containing the objects you've defined Models for. 

### 3. JSON Endpoints
Create the following JSON endpoints to serve your frontend views:
1. Products/Services gallery
    - `GET /api/v0/gallery`
    - Note: the `GET /gallery/:id` endpoint should be rendered server-side with a view.
2. Subscribers list
    - `POST /subscribers`
        - Inserts subscriber to database using `subscriber` model
    - `GET /api/v0/subscribers`
3. Team members (if in a group of 4)
    - `GET /api/v0/members`
4. Frontend `fetch()` implementations: Create appropriate frontend `fetch()` requests for the following JSON endpoints defined above:
    - Requests `GET /api/v0/gallery` for `GET /gallery`
    - Requests `GET /api/v0/subscribers` for `GET /admin`
    - Requests `GET /api/v0/members` for `GET /team`
5. For each `fetch()` request, build a corresponding gallery/list using `.forEach()` or similar method. 

### 4. Fancy Feature
Implement an app feature that we haven't covered in this course. Your instructor needs to approve this feature (before the end of CPNT 262) to ensure it has a large enough scope to qualify for its 5 points of mark value.

Some examples that would qualify:
- A login session that password protects your `GET /admin` route. Your teammates and your instructor should each have login credentials (`/register` functionality to add user account would not be needed).
- Pagination routes can be added to your gallery to display them 3 at a time (for example).
- You can install a 3rd party frontend framework such as [GreenSock](https://greensock.com/) to animate SVGs in your design on page load or button click.

### 5. Individual Contribution
Assign the key roles and responsibilities for each group member in delivering the Final Project. After each entry write a short summary defining their role and what their responsibilities are in the project. 

This charter will serve as the reference for your instructor's evaluation of your individual contribution to the group project.

#### Peer Evaluation
At the end of the Final Project, all team members must evaluate their teammates on a scale of 1-10. Each member's mark for this portion will be the average score given to them by their teammates.

#### Instructor Evaluation
Your instructor will also evaluate the individual contribution of each team member, within the context of the Group Charter. This will be based largely on your commit history for the project.

Things to remember:
- You must have Git properly configured to use your GitHub email address in order for your commits to be associated with your GH account. Without this, you will not receive credit for any work you have completed.
- If you have made contributions to the project that are not reflected in your commit history, please elaborate in your Project README or as a comment when you submit your group evaluation.
- Equal(ish) division of work is required unless there are mitigating circumstances.

---

## Submitting Your Assignment
In order to receive a grade, you must:
1. Deploy your Express app to Heroku and MongoDB Atlas.
2. Include a `README.md` in your project that contains the following information:
  - Course title and Team name;
  - Team members;
  - Details on what your **Fancy Feature** is an where to find it.
  - Any comments that may help squeeze marks out of your instructor (maybe give him hints on where to look for the requirements above);
  - Attributions for any code or assets that are not your own.
3. Zip your project (excluding `node_modules` and `.env` file) and submit them to Brightspace.
    - include a copy of the database seed (the array of objects) you used for this project so your instructor can recreate your database, if needed.
4. Include links to the following as a comment with your Brightspace submission:
    - GH Repo
    - Deployed Heroku App URL
    - **Connection string for `MONGODB_URL`**
