# Mind-sage

A complete, responsive, static student wellbeing website that can be published on GitHub Pages without Node.js, API keys, databases, paid hosting, or a server.

## Start locally

Open `index.html` in a modern browser. The application uses relative assets and hash-based navigation, so it also works in a GitHub Pages project subdirectory.

If you prefer a local web server, run `python -m http.server 8000` in this folder and visit `http://localhost:8000`.

## Publish on GitHub Pages

1. Sign in to GitHub and create a **public** repository named `mind-sage` (or another name).
2. Extract the `Mind-sage-GitHub-Pages.zip` archive on your computer.
3. Upload **the contents inside the `mind-sage` folder** to the root of the repository: `index.html`, `app.js`, `styles.css`, `assets/`, and the documentation. The repository root must contain `index.html`.
4. Commit the files to the `main` branch.
5. Open **Settings → Pages → Build and deployment** in the repository.
6. Under **Source**, choose **Deploy from a branch**. Choose the **main** branch and **/(root)**, then **Save**.
7. GitHub will show a public URL in the Pages section when deployment finishes. For a repository named `mind-sage`, the normal project URL format is `https://YOUR-USERNAME.github.io/mind-sage/`.

No Render deployment is required. No custom domain is required.

## Built features

- Five entry categories: Primary School, High School, UG, PG, and Ph.D.
- Date-of-birth calendar and gender selection with a "Do not want to disclose" option.
- Fresh arithmetic verification on every profile visit; an incorrect answer generates a different problem.
- Four distinct question banks (Anxious, Depressed, Stressed, Confused), with 10 mandatory questions each, one question per screen and editable previous answers.
- Transparent response-frequency index scored from 0–30, displayed as a percentage, with domain breakdown and personalised advice.
- Professionally oriented medical consultation guidance and Government of India mental-health support resources.
- A one-page PDF report generated directly in the browser, including offline without third-party PDF libraries.
- Bro-minD: guided 4–2–6 breathing, a five-senses grounding tool, three-minute meditation, sourced Bengali Vani, and original motivational reflections.
- A generated artistic illustration of Swami Vivekananda on the Vani page.
- Responsive desktop and mobile layouts; keyboard-friendly forms and buttons; reduced-motion CSS support.

## Scoring, safety and clinical use

Each questionnaire has 10 questions about experiences during the last two weeks. Response options score 0, 1, 2 and 3. The index is `round(sum(scores) / 30 × 100)`. Bands: 0–24% *Occasional*; 25–49% *Some*; 50–74% *Frequent*; 75–100% *Very frequent*. These are descriptive software bands, **not clinically validated cutoffs**. The percentage is **not a diagnosis, an individual probability of anxiety or depression, or a medication recommendation**.

The original question sets are customised educational reflection questions and have not undergone psychometric or clinical validation. Before using the site for clinical screening, research involving human subjects, or automated treatment decisions, obtain appropriate institutional ethics review, scale validation, age-appropriate safeguarding, referral protocols and clinical supervision. In particular, the primary-school workflow should be used with appropriate adult involvement.

An affirmative answer to the final depression safety question triggers an urgent-support panel. The site does not diagnose, prescribe, or replace emergency services. The application provides India's emergency number 112, the Tele-MANAS support number 14416, and child assistance via 1098 where relevant.

## Privacy and limitations

- This project is **front-end only**. It does **not** upload date of birth, gender, individual answers or reports to a backend.
- Session details stay in JavaScript memory and disappear after page reload or tab close. No browser localStorage, cookies, accounts, analytics or assessment database are used by the app.
- Generated PDF files are saved to the user's device only after clicking Download PDF. Browser printing uses the browser's own printing interface.
- Google Fonts are optional presentation resources and require connectivity; system fonts are used if unavailable.
- The **arithmetic captcha is a usability-only check**, not secure bot protection. Genuine anti-abuse protection requires a backend and a server-validated challenge.
- The same assessment questions are available in all educational categories; the category is used for context and age-appropriate signposting, not to claim different clinical norms.
- No chats, AI claims, medical predictions, or persistent tracking are included.

## Editing and ownership

- Edit page copy, questions, quotes and support programmes in `app.js`.
- Edit colours, typography, spacing and responsiveness in `styles.css`.
- Edit metadata and global resource links in `index.html`.
- Verify contact details periodically against the official sources listed in `SOURCES.md`.
- The portrait is an AI-generated **artistic depiction** and is not identified as a historical photograph.

## Quick troubleshooting

- **Blank page?** Ensure `index.html`, `app.js` and `styles.css` are uploaded in the same directory. Open your browser's developer console and inspect any 404 errors.
- **Broken portrait?** Ensure `assets/vivekananda-portrait.webp` is present at exactly that path (case sensitive).
- **No report download?** Enable file downloads for your browser/site, or use **Print** and choose **Save as PDF**.
- **404 on GitHub Pages?** Choose the correct `main` branch and `/(root)`, and ensure the repository's top level contains `index.html`.
- **Refresh while midway through an assessment?** Progress intentionally resets because responses are not stored for privacy.
