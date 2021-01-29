# CPNT 260 Assignment 1: Home Page with horizontal nav
This assignment will serve as starting project for future assignments. You have the freedom to pick the website topic to encourage creativity (and hopefully give you ammunition for the Final Presentations).

This will assume a single page site but you can optionally build a multi-page site.

## Client User Stories
1. You're an intern at a design agency and you're the only one in the office that can code. A new client asks for a first draft of a one-page website.
2. You are an independent contractor and you just landed your first paying project: a one-page website!
3. You need a website to promote your services. You think a one-page website is the best way to go.
4. A grandparent wants a website to show off their dog?

## Marking Rubric
Each of the following will be marked out of 4 points (for a total of 20 points), based on the requirements below:

### 1. Page Header and Footer
- Site name and logo.
  - `h1` heading is usually not used in the `header` for _multi-page_ sites, a `div` or `p` is preferred;
  - logo displayed using `img` element.
- Page footer
  - Copyright information centered in the footer.
    - Name
    - Date
  - Copyright symbol using either an icon font or HTML entity

### 2. Horizontal Page Navigation
Actual link text and destinations can differ from below:
- Menu links will be obviously clickable:
  - Home
    - Can be linked in the main menu or on a logo/site name.
  - Gallery
    - Link `href` to an image gallery of your choice.
  - Contact or similar
    - Link `href` to your own website, LinkedIn or social media profile of your choice. 
    - OR, use a `mailto:` link
    - OR, similar...
  - Login
    - Link `href` to `#`.
  - Register
    - Link must have a distinct look to differentiate it from the other links (e.g. make it look more like a button) since this is a main Call to Action.
  - Link `href` to `#`.
- Navigation will be a horizontal menu using Flexbox or CSS Grid.

### 3. Page Content
- `h1` and `h2` headings;
- `p`;
- `a` linked to an external site in a new tab;
- `strong` _and_ `em`;
- `img`
  - using Lorem Picsum (locally linked images will be accepted);
  - spans `100%` of its container (floated images will be accepted, as long as text is readable);
- optional: `ul`/`li` and/or `ol`/`li`;

### 4. General Requirements
- Page is marked up with proper semantic structural elements: 
  - required: `header`, `nav`, `main`, `footer`.
- Page text is readable at screen widths `400px` and does _not_: 
  - overlap any other page elements;
  - exceed a maximum line length of `95ch`;
  - overflow off the viewport;
  - have a contrast ratio below _AA_ for its text size.
- HTML images have proper `alt` text definitions/

### 5. Project documentation and code quality
- Include a `README.md` in your project that contains the following information:
  - Course title;
  - Author name;
  - Links to:
    - GH repo;
    - GH Pages site
  - Some context on the website (and maybe give him hints on where to look for the requirements above):
    - Who's the client?
    - What's the goal of the site?
  - Attributions for any code or assets that are not your own.
- Use best practices with file/directory names, commenting and indentation:
  - 2 spaces per indent
  - See: [Files and Directories - Naming Conventions](https://sait-wbdv.github.io/winter-2021/cheatsheets/naming-conventions/)

---

## Submission Requirements
- Push this assignment to a repo named `cpnt260-a1`.
- ZIP all files required for the site to operate and upload to Brightspace. 
- Leave a link to the following as a comment in your Brightspace submission (this is duplicated in your readme but comes in handy sometimes):
  - GH repo
  - GH Pages site

