# Assignment 3 Group Project: Wordpress Law Firm Website
[Team Assignments](teams.md)

## Scenario
The CG Law LLP firm has contracted your team to build a 3-page Wordpress website that they can edit themselves.

## Instructions
### 1. General
- Create a global navigation menu:
  - that lists the three Pages listed below;
  - denotes the current page the user is on.
- Install WordPress plugins:
  - Contact Form 7
  - Rank Math
- Create an admin account for each team member
- Create an admin account in the WP Admin panel:
  - username: instructor
  - password: password
- Add your instructor as a collaborator to your Flywheel site:
  - Email: acidtone@tonygrimes.com
  
### 2. Home page: Practice Areas
1. Setup
    - Create a Post for each of the 3 practice areas, using [`practice-areas.txt`](starter/practice-areas.txt) for content;
    - Create a Category called 'Practice Areas';
    - Assign each Practice Area Post to the 'Practice Areas' Category;
    - Do NOT allow comments on these Posts.
2. Category Page - Home Page
    - List the Posts added to the Practice Areas Category
    - Post navigation should be removed (either from the template or using CSS)
    - Display a hero image (which should be stored in the Media section) that is different than the parent theme
3. Each team member should be the author of one Practice Area post.

### 3. About Our Firm: Lawyer Profiles 
1. Setup
    - Create a Post for each of the 3 lawyers, using [`lawyer-text.txt`](starter/lawyer-text.txt) for content;
    - Create a Category called ‘Lawyers';
    - Assign each lawyer post to the 'Lawyers' category;
    - Do NOT allow comments on the Lawyer Posts;
    - Upload 3, openly licensed images for the lawyer profile pictures **to the Media section** and display them with their bios.
2. Category Page - About Our Firm
    - Create a Category Page called About Our Firm
    - List the Posts added to the Lawyer Category on this page
    - Post navigation should be removed (either from the template or using CSS)
3. Each team member should be the author of one Lawyer Profile.

### 4. Contact Us
1. Page - Contact Us 
    - Integrate a Contact Form using Contact Form 7
        - Full Name, email address and message.
    - Include address information with Google Map pin using a Rank Math shortcode.

### 4. Rank Math Configuration
1. Configure Rank Math
    1. Global Meta: use defaults
    2. Local SEO: 
        - Choose an address for your law firm, such as:
            - the home address of one of your members
            - an address of an empty lot in Calgary (use Google Maps to find the postal code)
            - _do not_ use a fake address, otherwise the Google Map won't display a correct location
        - FYI:
            - Locality -> City
            - Region -> Province
        - About page -> "About Our Firm"
        - Contact page -> "Contact Us"
    3. Home page: Create a home page meta description that is not lorem ipsum
2. Using a Rank Math Local SEO shortcode, include address and map information on the "Contact Us" page.

### 5. Group Evaluation
Assign the key roles and responsibilities for each group member in delivering the Project. After each entry write a short summary defining their role and what their responsibilities are in the project.

Each group member will evaluate their teammates out of 10. This will be averaged and combined with the individual contribution of their assigned Posts (Lawyer Profile and Area of Practice).

## Additional Requirements
- You may use one of the following themes:
  - [Neve](https://themeisle.com/themes/neve/)
  - [Zakra](https://zakratheme.com/)
- You may adapt code from other sources but you must document and attribute code that is not yours.
- Final website must be deployed to Flywheel (see Submission Requirements below).

## Submission Instructions
- Submit the following to Brightspace as a text submission:
  - your deployed Flywheel link
  - the username/password for the deployed demo site.
- Create an admin account in the WP Admin panel:
  - username: instructor
  - password: password
- Add your instructor as a collaborator to your Flywheel site:
  - Email: acidtone@tonygrimes.com

## Deliverables and Rubric
This assignment will be marked out of 50 points. 10 points will be given for each of the following:
1. General Requirements
2. Home Page
3. About Our Firm
4. Rank Math
5. Group Evaluation and Individual Contribution