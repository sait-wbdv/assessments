# Assignment 2 - Raster Image Optimization
In this assignment, you will: 
- create three `small`, `medium` and `large` image sets;
- place the images in a responsive web page;
- optimize the images with `srcset`, `width`, `height` and `loading` image attributes.

---

## Directory Structure
The following directory structure is expected for this assignment:

```
/assets
  /css
    /main.css
  /images
    /full
      /img-1.jpg
      /img-2.jpg
      /img-3.jpg
    /lg
      /img-1.webp
      /img-2.webp
      /img-3.webp
    /md
      /img-1.webp
      /img-2.webp
      /img-3.webp
    /sm
      /img-1.webp
      /img-2.webp
      /img-3.webp
/index.html
```

- Change the image filenames and extensions to suit your needs, but they should be easily recognized within an image set.
- `main.css` may be changed to `style.css` or similar.

---

## Instructions
### 1. Processed Images
1. Choose 3 openly licensed (or your own) **high-frequency** images (**that weren't images given to you in class**) to use in this project. Source images should be at least 2000px wide.
2. For each image, create the following image set with a _2:1 aspect ratio_ and _max `100k` file size_:
    - small: `500px` wide;
    - medium: `1024px` wide;
    - large: `1920px` wide;
3. Images should be organized according to the Directory Structure listed above. Place your original source image in `assets/images/full`.
4. You may use WebP, JPEG or PNG encoders to reach the required file size limit.
5. Each size of a given image should have the same aspect ratio.
6. For testing and marking, each image set (`sm`/`md`/`lg`) should be visually distinct across sizes. You may use an image editing method of your choice to accomplish this. For example, you may use different colour correction, filters, etc. 

## 2. HTML/CSS Implementation 
1. Using the following HTML template (optional), display `img-1`, `img-2` and `img-3` in a valid html page:

    ```html
    <div class="container">
      <img src="assets/images/md/img-1.webp" alt="Image 1">
      <img src="assets/images/md/img-2.webp" alt="Image 2">
      <img src="assets/images/md/img-3.webp" alt="Image 3">
    </div>
    ```

    - Change the alt text to something more descriptive based on the content of the image.

2. Make the container and images responsive by linking the following CSS in an external file:

    ```css
    .container {
      width: 90vw;
      max-width: 1920px;
      margin: auto;
    }

    img {
      display: block;
      width: 100%;
      margin: 3rem auto;
    }
    ```

    - You may add your own CSS for aesthetics but the page and images must remain responsive and `90vw` width until the maximum is reached.
    - Images should be hosted locally in the directory structure listed above. Follow file and directory naming convensions.
3. Add appropriate `srcset` image attributes to each `img` element (note that the fallback will be the `md` image). Images should visually change as the browser chooses the optimum image as the viewport width changes.
4. Add `width` and `height` _attributes_ to each `img` element, corresponding to `src` image. Use CSS to preserve aspect ratio.
5. Add the appropriate `loading` attribute to the `img` element to allow for lazy loading.

### 3. Documentation and code quality
- Include a `README.md` in your project that contains the following information:
  - Course title;
  - Author name;
  - Links to:
    - GH repo;
    - GH Pages site
  - Attributions for any code or assets that are not your own.
- The above directory structure and naming conventions should be followed.
- All code must validate and be properly indented, organized and commented.

---

## Marking Rubric
This assignment will be marked out of 25 points for the following, based on the requirements above:
1. Processed Images: 5 points for each image set (**15 points** total), focusing on:
    - 2 points: file size (and whether or not they are high-frequency);
    - 2 points: image size and aspect ratio;
    - 1 point: visual distinctiveness across image sizes.
2. HTML/CSS Implementation: **5 points**:
    - 3 points: images change at the proper breakpoints;
    - 2 points: `width`, `height`, and `loading` attributes are properly implemented.
3. Documentation and code quality: **5 points**.

---

## Submission Requirements
- Push this assignment to a repo named `cpnt201-a2`.
- ZIP all files required for the site to operate and upload to Brightspace. 
- Leave a link to the following as a comment in your Brightspace submission (this is duplicated in your readme but comes in handy sometimes):
  - GH repo
  - GH Pages site
