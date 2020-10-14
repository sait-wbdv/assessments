# Assignment 3 - SVG Graphic
## Summary
A client has requested a custom graphic to be used as a logo/icon for a website that has multiple colour schemes.

## Requirements
To accomplish different colour schemes with the same graphic, you realize you will need to use and inline SVG.

For the purposes of this assignment, you may create a design of your choosing and implement it on a page of your choosing. Please pay attention to your documentation so your instructor can find the design in question.

### SVG Design
If Figma, or similar vector authoring tool, build an SVG that:
- Contains three separate closed paths. For example, these paths can be a combination of:
  - a manually "drawn" closed shape using the pen tool (avoid the use of the pencil tool);
  - an icon font (imported as an SVG) that has been altered using the Pathfinder or similar tool (see the [No Bugs](https://github.com/sait-wbdv/sample-code/blob/master/frontend/svg/no-bugs/images/no-bugs.svg) graphic built in class);
  - some other openly-licensed SVG design you find online.
- Can be of a design of your choosing. You will not be marked on the aesthetics of the design itself; only the technical requirements of the closed paths.

### SVG Optimization
To ensure the best performance you will use [SVG OMG](https://jakearchibald.github.io/svgomg/) to optimize the exported design such that:
- Precision reduced to 1 (a precision of 2 is acceptable if a reduction in quality is apparent);
- Prettify Markup is turned on (for the benefit of your instructor);
- a `viewBox` is included in the file;
- `width` and `height` attributes are not included;
- no `style` element or inline `style` attributes are present within the `svg` element (presentational attributes are fine).

Note: SVG OMG may merge one or more of your paths. This is fine as long as your design has three visually distinct closed paths.

### Inline SVG 
Insert the optimized SVG graphic into a test page such that:
- the design incorporates two colours that match a non-white background;
- use class selectors and an external CSS stylesheet to achieve the colour scheme;
- at least one property other than `fill` colour is used to enhance the design (such as `stroke`, `filter`, etc);
- the size is large enough to properly differentiate between the colours of the design (e.g. don't use the graphic as a tiny social media icon). In other words, make it loud and proud.

For the purposes of this assignment, the design of the page itself doesn't matter (beyond the non-white background). You can make it simple by placing the graphic in the middle of an empty page. BUT try your best to at least make the graphic presentable for a potential client demo.

### Multiple Colour Schemes
Using a method of your choice, create a second colour scheme for the graphic. For example, you could do one of the following:
- Use a media query to change the colour of the graphic on mobile/portrait screens;
- Add the graphic to a second page with a different colour scheme;
- Use the CSS toggle technique you learned in class to manually toggle the colours of the sample page.

### Project Documentation
Please include a README with the following:
- Course code and title;
- Assignment name;
- A link to github repo;
- A link to GH Pages website;
- Attributions;
- A short summary of the location and behaviour of the graphic to direct your instructor while marking.

Include comments in the `svg` element itself to label which paths relate to the individual elements of the graphic (e.g. which path(s) makes up the bug in the [No Bugs](https://github.com/sait-wbdv/sample-code/blob/master/frontend/svg/no-bugs/images/no-bugs.svg) graphic built in class).

## Submitting Your Assignment
In order to receive a grade, you must:
1. Deploy your project to a GitHub Pages repository named "cpnt201-a3".
2. Zip your project/repo and submit them to Brightspace.
3. Include links to each GitHub repo as a comment with your Brightspace submission.

## Marking Rubric
This assignment will be marked out of 25 points.

### Criteria: 5 points will be given out for each of the following:
1. **SVG Design**: A design has been created according to the criteria above.
2. **SVG Optimization**: SVG has been optimized according to the criteria above. 
3. **Inline SVG**: SVG has been added to a sample page according to the criteria listed above. 
4. **Multiple Colour Schemes**: Multiple colour schemes have been implemented according to the criteria listed above.
5. **Project Documentation**: The project has been documented according to the criteria listed above.

