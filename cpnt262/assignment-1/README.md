# Assignment 1: classList Toggle
In this assignment you'll be taking the example classList toggle shown in class and extending it into a menu or drawer toggle button.

## Use Cases
The following criteria can be used to create one of the following website features.
- Hamburger menu
- Content drawer
- Night mode
- App switch

You can create of one the above for this assignment as long as it fullfills the following requirements. The details should be documented in your README.

## Criteria
This assignment will be marked out of 10 points according to the following requirements:

### 1. Interactivity: 4 points
- A button toggles a two-state feature such as
  - open/close a menu or content drawer
  - turn night mode on/off
  - turn a configuration setting on/off
- Pressing the button switches the state of the toggle from "open" to "closed" (or "on" to "off") and vice versa.
- Interactivity is achieved with a javascript `click` (or similar) event listener using `document.addEventListener()`.
- When the toggle state changes, an obvious visual change occurs on the page using the `classList` DOM API.

### 2. Button State: 2 Points
- A `button` or checkbox element is used for the toggle button.
- The button is visible on the page and is obvously clickable.
- The button shows the current state of the toggle. For example, the button shows a hamburger icon when closed and an "X" when open.
- Precautions must be made for button state becoming "out of sync".
- The button is accompanied by a text label for accessibility and usability reasons. If an icon is used, the label may be hidden with `display: none` or similar method.

### 3. Setup and Deployment: 2 Points
- Javascript must be linked as an external script, either before the `</body>` or in the `<head>` and located in a dedicated `js` directory.
- CSS must be linked as an external stylesheet in the `<head>` and located in a dedicated `css` directory.
- Javascript must use _strict_ mode.
- There must be no JS errors or warnings (except for favicon).

### 4. Documentation and Code Quality: 2 Points
1. Include a `README.md` in your project that contains the following information:
  - Course title;
  - Author name;
  - Links to:
    - GH repo;
    - GH Pages site
  - Some context on the toggle feature (and maybe give him hints on where to look for the requirements above).
  - Attributions for any code or assets that are not your own.
2. Use best practices with [file/directory names](https://sait-wbdv.github.io/winter-2021/cheatsheets/naming-conventions/), commenting and indentation:
  - 2 spaces per indent.
  - CamelCase naming conventions followed.
  - Statements ended with semi-colons.
  - Code is well-commented.
  - See [JavaScript Style Guide](https://www.w3schools.com/js/js_conventions.asp) for full list.

---

## Submission Requirements
- Push this assignment to a repo named `cpnt262-a1`.
- ZIP all files required for the site to operate and upload to Brightspace. 
- Leave a link to the following as a comment in your Brightspace submission:
  - GH repo
  - GH Pages site
