# Assignment 1: Feedback Key
## 1. Code Quality
1. Validation
    1. Broken root HTML structure. See [Anatomy of an HTML document](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Getting_started#Anatomy_of_an_HTML_document)
    2. Significant syntax errors.
    3. Minor-moderate syntax errors.
2. [File structure](https://sait-wbdv.github.io/cheatsheets/naming-conventions/#file-naming-conventionsguidelines)
    1. HTML page should be named `index.html`
    2. External css files should be in a `css` directory.
    3. Your images should be in a dedicated `images` directory.
3. Indentation and Organization
    1. Indent should be 2 spaces. You can change this in your code editor preferences/settings.
    2. Nested code blocks should be indented.
    3. CSS declarations should be organized by category (box model, fonts, borders, flex, etc), separated by a space.

## 2. Project Documentation
1. README file. Note: many of you didn't include one and I should have been more explicit. I removed a maximum of one point for missing READMEs to be fair to those that created one. Suggested information for a README:
    1. Course code and title
    2. Assignment title
    3. GH Pages link
    4. Attributions
2. Code comments
    1. General reminders for yourself and hints for new developers working on your project.
    2. Description of obstacles you encountered during the project, theories on the nature of the problem and possible solutions.

## 3. General
1. Responsive Text
    1. `font-size` should be smaller on mobile.
    2. Text cannot overflow the viewport on mobile.
2. Usability
    1. Text should be readable when overlapping an image. 
    2. Text cannot touch a visible edge. Add padding to containers that have text and a `background-color`.
3. Scrolling
    1. The page has a significant scroll bar and is no longer considered a splash/landing page.

## 4. Heading and Tagline
1. Fonts
    1. Different fonts for heading and paragraph. 
    2. System and/or generic font fallbacks in place.
    3. Convention is to assign `font-family` for body text to `body` tag.
2. Color Contrast
    1. Contrast ratio is less than 4.5:1.
3. Typography triad
    1. `font-size` should not be default.
    2. `line-height` should not be default. Recommended: define as a raw ratio with no units (i.e. 1.5 or 1.9)

## 5. Click-through link
1. Link Structure
    1. Link text should read "I am not Miner" or similar.
2. Link Presentation
    1. Padding should be added the `a` element to make it appear more clickable.
    2. Increase `font-size` to make the link more clickable.
    3. `:hover` and `:active` pseudo-selectors should be declared.
    4. Link contrast ratio should be greater than 7:1.
