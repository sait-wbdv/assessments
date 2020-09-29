# Assignment 3: Subscription form
Scenario: The potential client from Assignment 1 hired you based on your excellent splash page demo! They would like you to use that same design (or a new design if you desire) for a "Website Coming Soon" landing page inviting visitors to sign up for their newsletter.

They mentioned the Over 18 button isn't needed right now so you can remove it and add the Subscribe form instead.

## General
Add a valid Subscribe `form` to your hero section from Assignment 1 (or a new/different hero section). Fields to include:
- Name
  - text `input`
  - `required`
  - valid `name` attribute
- Email
  - email `input`
  - `required`
  - valid `name` attribute
- Favourite meal of the day
  - `select` menu
  - at least three `option`s to choose from
  - valid `name` and `value` attributes
- Checkbox: "I would like to recieve promotional emails" or similar.
  - chackbox `input`
  - valid `name` and `value` attributes
- Submit
  - either and `input` (type="submit") or `button` (type="submit)

The hero section should includ an `h1` heading and `p` tagline similar to Assignment 1 (you may remove the Over 18 button). The form should be visually separated from the heading and tagline.

## Form presentation
- Fieldset border should be removed (reset).
- Font face should not be default. Use your choice of Google Font.
- Use some kind of layout technique (flexbox, grid etc) to make the inputs and labels line up neatly.
- All required fields have a red asterisk next to the `label`.

## Form accessbility
- The form fields are wrapped in a `fieldset` including an accompanying `legend` element containing user instructions (i.e. "Sign-up to our newsletter"). 
- All form controls have functioning `label` elements.
- All text field inputs (name/email) have placeholder text defined.
- All text field inputs (name/email) fields should be no longer than `30ch` wide.

## Submission Requirements
- Push this assignment to a repo named `cpnt260-a3`.
- ZIP all files required for the site to operate and upload to Brightspace. 
- Leave a link to your GitHub repo as a comment in your Brightspace submission.

## Marking Rubric: 3 marks will be given for each of the following:
1. Code Quality
    - Code must be valid, organized and semantic.
2. Project Documentation
    - Code must be commented.
    - Project must include a README file containing:
        - Course title;
        - Author name;
        - Any comments that may help squeeze marks out of your instructor;
        - Attributions for any code or assets that are not your own.
3. General: See requirements above.
4. Form presentation: See requirements above.
5. Form accessibility: See requirements above.