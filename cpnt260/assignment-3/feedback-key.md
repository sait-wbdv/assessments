# Assignment 2: Feedback Key
## 1. Code Quality
1. Validation
    1. Broken root HTML structure. See [Anatomy of an HTML document](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Getting_started#Anatomy_of_an_HTML_document)
    2. Significant syntax errors.
    3. Minor-moderate syntax errors.
    4. External files are linked from within the `body` element. Convention is to `link` from the `head` element.
2. [File structure](https://sait-wbdv.github.io/cheatsheets/naming-conventions/#file-naming-conventionsguidelines)
    1. HTML page should be named `index.html`
    2. Embedded CSS should be in an external stylesheet located in a `css` directory.
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
1. Dropdown menu is malformed and inoperable. Menus are created with the `select` element and the items in the menu are created with `option` elements. See [`<select>: The HTML Select element`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/select).
2. The empty option in a menu (e.g. "Please choose an option") should have an empty `value` attribute.
3. `checkbox` is missing. See [`<input type="checkbox">`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/checkbox)
4. In general, form input `value` should be descriptive. For example: instead of "b" as a menu option, use "breakfast".

## 4. Form Presentation
1. Problems with form layout. Form controls should line up neatly with each other.
2. Form controls are touching each other. More spacing required in your form.
3. Fonts are not properly declared or are using defaults.
4. Form not properly reset. `fieldset` border should be removed and, if a list is used for form controls, bullets should probably be removed.

## 5. Form Accessibility
1. Redundant `fieldset` and `legend` elements. You generally only need one set of `fieldset` and `legend` for general instructions for the entire form (e.g. "Please fill out our form"). If a `label` gives adequate instructions for a screen reader, additional `fieldset` and `legend` elements are not needed.
2. Inoperable for labels. The `for` attribute should match the `id` of its companion form control. See [`<label>` form element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/label)
3. Text contrast ratio is too low.
4. Make text fields nice and big for users with alternate input devices. For example, use padding or have them stretch into a large flex item. Font-size should be increased for forms.