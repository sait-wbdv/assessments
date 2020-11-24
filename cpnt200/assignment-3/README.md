# Assignment 2: Wordpress Simple Parent Theme
## Scenario
The CG Law LLP firm has contracted your team to build a 3-page Wordpress website that they can edit themselves.

## Instructions
### Home page: Practice Areas
1. Setup
    - Create a Post for each of the 3 practice areas, using `practice-areas.txt` for content;
    - Create a Category called 'Practice Areas';
    - Assign each Practice Area Post to the 'Practice Areas' Category;
    - Do NOT allow comments on these Posts.
2. Category Page - Home Page
    - List the Posts added to the Practice Areas Category
    - Post navigation should be removed (either from the template or using CSS)
    - Display a hero image (which should be stored in the Media section) that is different than the parent theme

### About Our Firm: Lawyer Profiles 
1. Setup
    - Create a Post for each of the 3 lawyers, using `lawyer-text.txt` for content;
    - Create a Category called ‘Lawyers';
    - Assign each lawyer post to the 'Lawyers' category;
    - Do NOT allow comments on the Lawyer Posts;
    - Upload 3, openly licensed images for the lawyer profile pictures **to the Media section** and display them with their bios.
2. Category Page - About Our Firm
    - Create a Category Page called About Our Firm
    - List the Posts added to the Lawyer Category on this page
    - Post navigation should be removed (either from the template or using CSS)

### Contact Us
1. Page - Contact Us 
    - Integrate a Contact Form using Contact Form 7
    - 

### General
- Create a global navigation menu:
  - that lists the above Pages;
  - denotes the current page the user is on.
- Install WordPress plugins:
  - Contact Form 7
  - Rank Math

## Requirements
- You may use any of the following themes:
- You may adapt code from other sources but you must document and attribute code that is not yours.
- Final website must be deployed to a live server (see Submission Requirements below).

## Deliverables and Rubric
5 points will be given to each of the following deliverables:

### 1. Code Quality
Your code should be valid, well formatted/organized and easy for your instructor to find the things while marking.

### 2. Post Setup
The Lawyer and Practice Areas content has been implemented according to the instructions.

### 3. Page Setup
The Home, About and Contact content has been implemented according to the instructions. The primary navigation works as expected.

### 4. Stylesheet Injection
External stylesheets have been successfully added to the site to enhance the presentation of the website. The design can be minimal but adherence to basic UX principles is expected.

### 5. Plugin Setup
The contact form, SEO and Google Map plugins have been implemented according to the instructions.

## Submission Instructions
Upload the following project files to Brightspace
- Create an admin account in the WP Admin panel:
  - username: instructor
  - password: password
- Zipped wordpress files
- phpMyAdmin database export
and submit your repo and deployed website urls as a comment.
