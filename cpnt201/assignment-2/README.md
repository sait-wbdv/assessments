# Assignment 2 - Three Deployed Git Hub Pages Templates

## Criteria
### 1. Low-frequecy image: Landscape and portrait hero images (10 points)
Create a simple hero section that:
- Fills the viewport (100vw and 100vh);
- Contains a low-frequency image as a `background-image` that takes up at least 25% of the viewport;
- Displays a different image on `landscape` vs `portrait`.

**5 points each:**
1. Image files
    - file size: 15k
    - File format: can be either WebP, JPEG or PNG.
2. Hero section with `orientation` media query
    - Text card over `background-image`.
    - Text cannot overlap a high-frequency area.

### 2. Blog excerpt with 100% image (10 points)
Below the Hero section above, place a centered image that is at least 80vw with a `max-width` of `1920px`.

**5 points each:**
1. High-fequency files (over 75% can be considered high-frequency)
    - Large file
        - width: `1920px`
        - aspect ratio: 2:1
        - size: 100k
    - Medium file
        - width: `1024px`
        - aspect ratio: 2:1
        - size: 50k
    - Small file
        - width: `500px`
        - aspect ratio: 2:1
        - size: 25k
    - File format: can be either WebP or JPEG.
2. `srcset` implementation 
    - Breakpoints based on viewport width:
        - large image: `1500px` and up
        - medium image: `750px`-`1500px`
        - small image: under `750px`
    - Images should be organized in (and linked to) a local `images` folder with coresponding `sm`, `md` and `lrg` directories. Follow file and directory naming convensions covered in this program.
    - To help your instructor mark this assignment, the images for each blog article should be visually distinct across each size. You may use a method of your choice to accomplish this. For example, you may use different colour correction, filters, etc.
    - Each size of a given blog image should have the same aspect ratio.

### 5. Documentation and code quality
- Proper directory structure
    - `/assets/images/lg...`
    - `/index.html`
- README

## Submission instructions