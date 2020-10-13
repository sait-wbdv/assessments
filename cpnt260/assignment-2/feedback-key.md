# Assignment 2: Feedback Key
## 1. Code Quality
1. Validation
    1. Broken root HTML structure. See [Anatomy of an HTML document](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Getting_started#Anatomy_of_an_HTML_document)
    2. Significant syntax errors.
    3. Minor-moderate syntax errors.
    4. External files are linked from within the `body` element. Convention is to `link` from the `head` element.
2. [File structure](https://sait-wbdv.github.io/cheatsheets/naming-conventions/#file-naming-conventionsguidelines)
    1. HTML page should be named `index.html`
    2. External css files should be in a `css` directory.
    3. Your images should be in a dedicated `images` directory.
3. Indentation and Organization
    1. Indent should be 2 spaces. You can change this in your code editor preferences/settings.
    2. Nested code blocks should be indented.
    3. CSS declarations should be organized by category (box model, fonts, borders, flex, etc), separated by a space.
4. Improper class names
    1. Presentational wording used in class names. Avoid using terms such as `border-red` or `header-photo-shadow` for class names. If the design elements change (i.e. from red to blue) the class names will also need to be changed.
    2. `class` names should not be camel case (that's for js variables). Use lowercase names with hyphens or underscores instead of spaces.

## 2. Project Documentation
1. README file missing.
2. Suggested information for a README:
    - Course code and title
    - Assignment title
    - GH Pages link
    - Attributions
3. Code comments
    1. General reminders for yourself and hints for new developers working on your project.
    2. Description of obstacles you encountered during the project, theories on the nature of the problem and possible solutions.

## 3. General
1. `height` is set explicitly on elements of the card. This will make the vertical height of the card change with the height of the window. This means the card is too long on large screens and content overflows the card on small screens. Instead, try setting `min-height` or avoid setting height altogether. Spacing is better managed using `padding` and `margin`.
2. Fonts are not properly implemented.
3. Card container design is broken.
4. Card width is not limited to between `20ch` and `40ch`.
5. Colour scheme does not match the mockup.

## 4. Card Header
1. Card header design is broken.
2. Header design breaks at small card `width` and/or `height`.
3. Broken aspect ratio on profile/background image.
4. River image should be a CSS background image and not HTML since it's a presentational image.
5. Profile image should be an HTML image and not a CSS background image since it should be considered a content image like the profile heading and description.

## 5. Card Footer
1. Some problems with social media icon spacing.
2. Improper import of icon fonts.
3. Border created with `hr` rule (content used as presentation) when pure presentational solution was available.
4. Social media icon size does not match the mockup.
5. Separating border between description and icons is missing.