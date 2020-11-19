# Assignment 1: Static Website with PHP Includes
For this assignment, choose a static 4-5 page website of your choice. For example:
- a past assignment
- a personal project
- something new

Similar to your Express EJS assignment, you will:
1. Convert the html files to php files by changing the extension to `.php`;
2. Create a `_config.php` file to hold all site-wide variables;
3. Separate repeating elements into template partials;
4. Include your partials on each page using the `include()` function;
5. Create a dynamic copyright statement for your `footer.php` partial.

Note: If your home page has a hero section, you may choose to not include your `header.php` partial on this page (but it still must use a `$page_title` variable).

## Example directory structure:

    ```
    - assets
    --- css
    --- js
    --- images
    - includes
    --- _config.php
    --- head.php
    --- header.php
    --- footer.php
    - index.php
    - about.php
    - contact.php
    - products.php
    ```

## Instructions
### 1. Project config file
Create the following site-wide variables and store them in a `includes/_config.php` file:
- `$site_title` - string containing (you guessed it) your site title to be included in your `<title>` element.
- `$site_description` - string describing your site in 50–160 characters to be included in the `<meta name="description">` information in the `<head>` (see below).
- `$site_owner` - string containing the site owner to be included in the copyright statment in the `<footer>`.

### 2. Template Partials
Separate repeating page elements into following template partials:
1. `includes/head.php` - the meta information of each page. This partial should incorporate the following site-wide variables:
  - `<title>`: contains the `$site_title` and `$page_title` (see below), separated by a hyphen.
  - `<meta name="description" content="[description]">`: contains the `$site_description` created above.
2. `includes/header.php` - the `<header>` (and possibly `<nav>`, depending on your design) that includes `$page_title` (see below), preferrably in an `<h1>` element.
3. `includes/footer.php` - the `<footer>` that includes a dynamic copyright statement (see below).

### 3. Dynamic copyright statement
Create a dynamic copyright statement that incorporates the following format `&copy; [year] [site-owner]`:
1. `[year]`: The current year, generated using the `date()` function.
2. `[site-owner]`: The site-wide `$site_owner` variable created previously.

The final copyright statement should look similar to "&copy; 2020 Tony".

### 4. Page setup
For each page of the site:
1. Include `_config.php` above the `<!DOCTYPE html>`;
2. Define a `$page_title` variable above the `<!DOCTYPE html>`;
3. Include each of the template partials defined in the previous section.

### 5. Project documentation and code quality
- Include a `README.md` in your project that contains the following information:
  - Course title;
  - Author name;
  - Links to:
    - your GH repo;
  - Any comments that may help squeeze marks out of your instructor (maybe give him hints on where to look for the requirements above);
  - Attributions for any code or assets that are not your own.
- Use best practices with file/directory names, commenting and indentation.

## Submitting Your Assignment
In order to receive a grade, you must:
1. Zip your project and submit them to Brightspace.
2. Include links to the following as a comment with your Brightspace submission:
    - GH Repo

## Marking Rubric
This assignment will be marked out of 20 points. 4 points will be given for each of the following, based on the requirements above:
1. Project config file
2. Template Partials
3. Dynamic copyright statement
4. Page setup
5. Documentation and code quality
