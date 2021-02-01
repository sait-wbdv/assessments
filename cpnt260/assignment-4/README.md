# CPNT 260 Assignment 4: Hero section
In this assignment, you will add functionality to the page you have been building in previous exercises:
- Create a hero section for your page;
- Create a Call-to-Action for your hero section;
- Integrate third-party services to your page.

## Client User Stories
1. You're an intern at a design agency and you're the only one in the office that can code. A new client asks for a first draft of a one-page website.
2. You are an independent contractor and you just landed your first paying project: a one-page website!
3. You need a website to promote your services. You think a one-page website is the best way to go.
4. A grandparent wants a website to show off their dog?

## Marking Rubric
Each of the following will be marked out of 4 points (for a total of 20 points), based on the requirements below:

### 1. Hero section
Create a scroll-less hero section that contains:
- at least one _locally-hosted_ image (see devops section), using either HTML or CSS;
- One or more content cards:
  - a heading, wrapped in a `h1` (or other element, if appropriate)
  - a tagline, wrapped in a `p`
  - a call-to-action such as:
    - an `a` or `button` element to a website of your choice;
    - a newsletter subscription form (does not have to be active);
    - your contact form (see next section).
  - The Call to Action should look like a button and be obviously clickable;
- Display the heading and tagline with two different Google Fonts, each with fallbacks for system and generic fonts.
- Optional: use of one or more gradients;

### 2. Contact section
Note: these services have not been covered in class. This is an exercise in searching and following documentation.
- Integrate a third-party contact form (using a form submission services such as [Formspree](https://formspree.io/)). This form can be used as your Call-to-Action above.
- Integrate an interactive Google Map (ie. not a static image) into your site, using a real street address of your choice as the location pin. The can alternatively be placed in the footer instead of a dedicated contact section.

### 3. Responsiveness
- Hero section text is readable at all screen widths (i.e. text does not overlap with a busy image).
- Background images can be removed for mobile.
- `font-size` is smaller on mobile than on desktop.
- Navigation bar is usable on mobile screens. Either a vertical menu or hamburger icon (which doesn't have to be operable).
- There is a scroll-track along the side(s) on mobile.
- Text is readable at all widths.

### 4. Devops and Deployment
- See the Static Website section of [Files and Directories - Naming Conventions](https://sait-wbdv.github.io/winter-2021/cheatsheets/naming-conventions/) for a common file structure for your files.
- Your hero section image should be locally-hosted in an `images` directory.
- CSS should be linked in external CSS files named:
  - `reset.css` for your browser resets;
  - `font.css` for your Google Font declarations;
  - `main.css`, `styles.css`, etc. for your core styles.
- Deploy your project to GitHub Pages.

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
- Accessibility best practices are followed:
  - Page text is readable at all screen widths and does _not_: 
    - overlap any other page elements;
    - exceed a maximum line length of `95ch` or be shorter than `20ch`;
    - overflow off the viewport;
    - have a contrast ratio below _AA_ for its text size.
  - Images should include proper `alt` text attributes.
- Page is marked up with proper semantic elements, when needed.
- CSS declarations should be organized by category (box model, fonts, borders, flex, etc), separated by a space.

---

## Submission Requirements
- Push this assignment to a repo named `cpnt260-a4`.
- ZIP all files required for the site to operate and upload to Brightspace. 
- Leave a link to the following as a comment in your Brightspace submission (this is duplicated in your readme but comes in handy sometimes):
  - GH repo
  - GH Pages site

