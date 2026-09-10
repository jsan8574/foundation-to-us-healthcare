# Foundation to US Healthcare

A self-paced, no-build course in plain HTML, CSS and JavaScript. It can be hosted from this folder as-is.

## Preview Locally

From this folder, run a simple local web server:

```sh
python3 -m http.server 8765
```

Then open `http://127.0.0.1:8765/`. Opening `index.html` directly may restrict browser storage or downloaded files, so an HTTP preview is recommended.

## Publish To Personal GitHub Pages

The intended public address is `https://jsan8574.github.io/REPOSITORY-NAME/`.

1. Create a repository in the `jsan8574` GitHub account.
2. Add that repository as this folder's remote and push the committed files.
3. In the repository, open **Settings → Pages**.
4. Choose **Deploy from a branch**, select the published branch and the root folder, then save.

GitHub Pages is public by default, regardless of repository privacy or paid plan. Do not publish patient information, credentials or other private data. No remote repository was created and nothing was pushed as part of this delivery.

## Course Behavior

- Progress, answers, reflections, required explanations, assessment attempts, the learner name and active-learning time are stored in the current browser with `localStorage`.
- A learner name is required before the course opens. The same saved name appears on the certificate and PDF learning record.
- The timer counts only while the page is visible, focused and recently active. It excludes long gaps and pauses after 90 seconds of inactivity.
- Reflections and selected practice explanations require at least 20 characters and cannot be skipped.
- Coaching key points appear after submitted work.
- Each module contains a lesson acknowledgement checkbox, practice, a two-question check for understanding and a reflection.
- The payer module covers Medicare and Medicaid delivery, military and veteran programs, common HMO/PPO/EPO/POS patterns, coordination of benefits, liability coverage, and the distinction between insurance payers and HSA/FSA funding accounts.
- The graded knowledge check contains 20 questions and requires 80% to pass.
- The certificate downloads as a PNG. The PDF learning record includes a completion-verification summary plus every module acknowledgement, learning objective, key-concept reminder, activity response and attempt, required explanation, check-for-understanding answer and attempt, reflection, coaching reminder and graded knowledge-check attempt.
- PDF export loads jsPDF from a CDN and therefore requires an internet connection. The rest of the course uses local assets, apart from learner-selected official reference links.

To reset a learner's progress for testing, clear site data for the preview or deployed address in the browser. Progress does not sync between browsers, devices or domains.

## Claim-Form Resources

Only the first page from each supplied PDF is included:

- `assets/cms1500-page1.png`
- `assets/ub04-page1.png`

The supplied CMS-1500 is the legacy 08/05 form. It is identified as a location exercise in the course, with a link to the current CMS professional paper-claim resource. The UB-04 activity links to the official CMS institutional-claim resource. Update these assets only with blank or approved training forms.

## Fonts

The supplied Proxima Nova files include the exact Regular, Regular Italic, Semibold, Semibold Italic, Bold and Bold Italic weights. They are used locally from `assets/fonts/`; no weight substitutions are needed.

## Updating The Course

Course content and answer keys are in `course.js`. Interface behavior is in `app.js`, and visual styles are in `styles.css`.

After changing CSS or JavaScript, increment the shared `?v=N` value in `index.html`. Keeping the version values aligned prevents GitHub Pages and browsers from serving a stale mix of files.

The site has no framework, package manager, build step, backend or login.
