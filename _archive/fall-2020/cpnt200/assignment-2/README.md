# Assignment 2: Customer admin
For this assignment you will create a mock Administration panel with the following pages:
- `index.php`: shows a list of customers from the `aviano-db`.
- `customer.php?id=3`: shows a single customer that corresponse to `id`.
- `error.php`: static error page if there is a database connection error.

For the purposes of this assignment, you do not need to create template partials for these pages.

## Sample Database
This assignment will assume the use of the following database, named `aviano-db`:

[aviano import](import-db.sql)

## Example directory structure:

    ```
    - assets
    --- css
    --- js
    --- images
    - includes
    --- config.php
    - index.php
    - customers.php
    ```

## Instructions
### 1. Documentation and code quality
- Include a `README.md` in your project that contains the following information:
  - Course title;
  - Author name;
  - Links to:
    - your GH repo;
  - Any comments that may help squeeze marks out of your instructor (maybe give him hints on where to look for the requirements above);
  - Attributions for any code or assets that are not your own.
- Use best practices with file/directory names, commenting and indentation.

### 2. Project setup and `error.php`
1. Create a connection to the database using `mysqli_connect()` and store it in a `includes/config.php` file. For the purposes of this assigment, please use the following connection details:
    - Host: `localhost`
    - Username: `root`
    - Password: `''` (empty string)
    - Database: `aviano-db` 
2. If there is an error connecting to the database, redirect the user to `error.php` using `header()`;
    - Note: `error.php` should not include `config.php` or you will have an infinite redirect.

### 3. `index.php`
1. Include `config.php` above the `<!DOCTYPE html>`.
2. Retrieve a customers array from the database using SQL and `mysqli_query()`.
3. Using `mysqli_fetch_all()` and a `foreach()` loop, list the following customer information using a table or CSS Grid:
    - Full name, in `last_name, first_name` format;
    - Phone number;
    - Email address.
4. Link the name to the following page:

    ```html
    customer.php?id=[customer_id]
    ```

### 4. `customer.php`
1. Include `config.php` above the `<!DOCTYPE html>`;
2. Using `$_GET`, SQL and `mysqli_query()`, retrieve the customer data that corresponds to the `id` that was passed as a URL parameter.
3. Display the following information on the page:
    - A link back to `index.php`;
    - First name;
    - Last name;
    - Date of birth;
    - Driver license number;
    - Phone number;
    - Email address.
4. If a customer was not found, display an error on the page with a link back to `index.php`.

## Submitting Your Assignment
In order to receive a grade, you must:
1. Zip your project and submit them to Brightspace.
2. Include links to the following as a comment with your Brightspace submission:
    - GH Repo

## Marking Rubric
This assignment will be marked out of 30 points. Points will be given for each of the following, based on the requirements above:
1. **5 points**: Documentation and code quality
2. **5 points**: Project setup
3. **10 points**: `index.php`
4. **10 points**: `customer.php` 