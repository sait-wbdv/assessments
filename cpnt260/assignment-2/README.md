# CPNT 260 Assignment 2: Card content block
In this assignment, you will
- add an additional content block containing a row of 3 cards (on wide screens) to the page you created in Assignment 1;
- enhance your navigation menu to make it responsive.

The content block can reflect a topic of your choice. For example:
- Our Team Members
- Products and Services
- My Kids!

## Client User Stories
1. You're an intern at a design agency and you're the only one in the office that can code. A new client asks for a first draft of a one-page website.
2. You are an independent contractor and you just landed your first paying project: a one-page website!
3. You need a website to promote your services. You think a one-page website is the best way to go.
4. A grandparent wants a website to show off their dog?

## Marking Rubric
Each of the following will be marked out of 4 points (for a total of 20 points), based on the requirements below:

### 1. Card content block
- Responsive content block: 3 cards in a row on wide screens.
- Content block should be wrapped in a `section` element or similar with a heading describing the section (i.e. "Our Team").
- Cards must have readable text at all screen sizes (ex. minimum `20ch` line length, no overflow, etc).
- Content block should be responsive: display a row of three cards on wide screens and a single column of 3 rows on mobile. Optional: there can be middle phase of two columns (2 cards and 1card, centered).
- Media queries should not be used to achieve responsiveness.

### 2. Card design
Each card should be designed with the following specifications:
- Include an image. This can be a raster, svg or icon font.
- Include a heading with body text relating to the image.
- Card text cannot touch any boundaries, like the card edge or other visible elements.
- Card width should be narrower than it is tall. IOW, it should be about the size and dimensions of a phone screen.
- Card should be wrapped in an `article` element or similar.

### 3. Responsive navigation
- Navigation menu should be horizontal on wide screens and vertical on narrow screens.
- Menu should not wrap or overflow at any screen width.
- Any method can be used to achieve responsiveness, such as media queries, Flexbox or CSS Grid.
- Optional: A hamburger menu can be used to toggle the menu on narrow screens.

### 4. General Requirements
- Page is marked up with proper semantic structural elements: 
  - required: `header`, `nav`, `main`, `footer`.
- Accessibility best practices should be followed
  - Page text is readable at all screen widths and does _not_: 
    - overlap any other page elements;
    - exceed a maximum line length of `95ch` or be shorter than `20ch`;
    - overflow off the viewport;
    - have a contrast ratio below _AA_ for its text size.
  - Images should include proper `alt` text attributes.

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
- Push this assignment to a repo named `cpnt260-a2`.
- ZIP all files required for the site to operate and upload to Brightspace. 
- Leave a link to the following as a comment in your Brightspace submission (this is duplicated in your readme but comes in handy sometimes):
  - GH repo
  - GH Pages site

