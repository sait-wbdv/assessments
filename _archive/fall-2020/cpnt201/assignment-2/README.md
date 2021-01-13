# Assignment 2 - Blog home page
## Summary
A client would like to start a company blog and has asked you for a proof-of-concept (PoC) blog home page listing five blog posts.

## Instructions
### Scenario documentation
Create a hypothetical company web page (it can be a real company, if applicable) with: 
- a name;
- a simple page header (`header` with `h1` and a `background-color`);
- a project README that includes:
  - Course code and title;
  - Assignment name;
  - A link to github repo;
  - A link to GH Pages website;
  - A short (50 words max) summary of the subject of the blog and how it relates to the company.

### Blog article summaries
Each blog article must have real content (not lorem ipsum) that can be taken from an openly licesed source (i.e. wikipedia), including:
- An article title and date;
- Article excerpt (10-50 words of the hypothetical article);
- an image (see requirements below);
- a "Read more..." link (or similar) pointing to a page of you choice. This can be the original article you used for the blog excerpt.

### Image processing
- Find 5 openly licensed (or your own works) **high-frequency** images (**that weren't images given to you in class**) to use in this project. Source images should be at least 2000px wide.
- For each of the 5 images, create:
  - a small version at 500px wide;
  - a medium version at 1000px wide;
  - a large version at 2000px wide.
- Images should be organized in (and linked to) a local `images` folder with coresponding `sm`, `md` and `lrg` directories. Follow file and directory naming convensions covered in this program.
- To help your instructor mark this assignment, the images for each blog article should be visually distinct across each size. You may use a method of your choice to accomplish this. For example, you may use different colour correction, filters, etc.
- Each size of a given blog image should have the same aspect ratio.

### File Size Optimization
- To mazimize network performace, optimize each image so that:
  - large images do not exceed 100K in file size;
  - medium and small images don't exceed 50K.
- Encode each **high-frequency** image as a JPEG file, not WebP.

### Responsive Optimization
In addition to the above criteria:
- Each image should be layed out so that the image is, at minumum, 75% the width of the viewport (with a max-width of 1500px).
- Each `img` element (do not use `picture` elements) should:
  - use `srcset` to ensure that the following images are displayed at their respective viewport widths:
    - 1250px and wider: large image;
    - 750-1250px: medium image;
    - less than 750px: small image.
  - use the medium image set as the `src` attribute fallback;
  - have appropriate `width` and `height` attributes matching the medium image.

## Submitting Your Assignment
In order to receive a grade, you must:
1. Deploy your project (including images) to a GitHub Pages repository named "cpnt201-a2".
2. Zip your project/repo and submit them to Brightspace.
3. Include links to each GitHub repo as a comment with your Brightspace submission.

## Marking Rubric
This assignment will be marked out of 25 points.

### Criteria: 5 points will be given out for each of the following:
1. **Scenario Documentation**: The subject of the blog articles have been implemented according to the criteria above.
2. **Blog article summaries**: Each blog excerpt has been implemented according to the criteria above. 
3. **Image processing**: Images have been processed into small, medium and large sizes according to the criteria listed above. 
4. **File size optimization**: Images have been optimized according to the criteria listed above.
5. **Responsive optimization**: The images have been implemented according to the criteria listed above.

