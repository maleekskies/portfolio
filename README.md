# maleekskies: Portfolio

Personal portfolio site for **maleekskies**, a full stack developer building AI automation across Web3, AI, and practical software.

**Live site:** [maleekskies.vercel.app](https://maleekskies.vercel.app)

## About

A static HTML portfolio with no build step or dependencies. Markup, styles, and scripts all live in `index.html`.

The site covers:

- **About**: background, current focus, and core stats
- **What I Do**: 2 core service areas (Full Stack Development, AI Automation) in a card grid
- **Featured projects**: 4 highlighted projects (VAULT 01, ChessHatch, RoleSearchHQ, OZ Handcrafted Footwear) on an interactive 3D ring carousel of compact cards; tapping a card opens a details panel with the full description, tech stack, links, a swipeable gallery of screenshots, and a case study link
- **My Work**: a hub with two in-page views:
  - **Full Stack Development**: all 9 projects with screenshots, descriptions, tech stacks, live links, repo links, and a case study
  - **AI Automation**: five case studies with pipeline diagrams: the MK customer support and lead follow-up system, the Skies Realty AI lead-management pipeline, the Skies Realty error handler, the Engineering Sites YouTube lead research pipeline, and the ChessHatch lesson publishing workflow
- **Tools I Use**: tech stack organized by category (frontend, AI automation, backend, tools & design), with logos where available. The main tools are shown first and larger.
- **What Drives Me**: 4 short values behind the work
- **Contact**: an "Email me" button with a copy-email button and a CV link, plus email, X, Telegram, and LinkedIn in a terminal-style card

## Features

- Light/dark theme toggle (preference saved locally)
- Dynamic background: a multi-column scrolling code effect in dark mode (brass/forest palette, glow, depth layering), an interactive particle network in light mode that particles gently drift toward the cursor
- 3D ring carousel for featured projects: drag, swipe, arrow buttons, or arrow keys to rotate; the front card tilts and catches a light glare following the mouse; clicking a side card brings it forward
- Project details panel: a bottom sheet on mobile and a centered window on desktop, with a screenshot gallery (swipe, arrows, or arrow keys), closing with the X, the Escape key, or a tap outside
- 3D tilt effect on skill and tool cards, following the mouse
- Five AI automation case studies, each with a pipeline diagram: MK (form, sheet, validation, local AI reply, Gmail and Telegram, follow-up), Skies Realty (form, n8n, scoring, local AI summary, CRM, Telegram alert), the Skies Realty error handler (Error Trigger to a Telegram alert with the workflow, node, time, and error), Engineering Sites (hourly YouTube research, Gemini scoring, 15-field CRM), and ChessHatch (no-repeat lesson deck, five designs, board render, voiceover, Instagram and Telegram)
- Mobile header auto-hides on scroll down, reappears on scroll up
- Hamburger menu on screens 860px and below, with About, Skills, Work, Tools, Contact, and Ask. It closes on a link tap, Escape, or a click outside.
- In-page navigation between sections and views without full page reloads
- CV download link in the header on desktop and in the contact section on all screens
- Custom favicon and social link preview image
- Scroll-triggered animations; the 3D motion and orbit animation respect the "reduce motion" accessibility setting

## Tech Stack

- HTML5, CSS3, vanilla JavaScript
- CSS 3D transforms for the project carousel, Canvas API for the particle network background
- Google Fonts (Space Grotesk, IBM Plex Mono, Inter)
- Tool icons loaded from devicon and Simple Icons via CDN, with graceful fallback if any icon fails to load
- No build tools, no package manager required

## Editing the projects

Each project is written once, as a hidden card inside the `projectStore` block near the bottom of `index.html`. The home-page ring, the details panel, and the full projects list are all built from those cards, so editing a project there updates every place it appears. The four ring projects and their order are set by the `featured` list at the top of the "Featured projects" script.

## Adding pictures to a project's gallery

Screenshots live in the project root, next to `index.html`. In the same script, find the `GALLERY` list: each project has lines like `['./rolesearchhq-board.jpg', 'Caption shown under the picture']`. Add a line for each new picture (the word `cover` means the project's existing card image). A project with no entry just shows its card image, with no arrows. For fast loading, keep screenshots around 800px wide and save them as JPEG.

## Adding screenshots to the automation case studies

Find the `SCREENSHOTS` comments inside the five case studies (the AI Automation page) in `index.html`. The MK, ChessHatch, and Skies error handler case studies already have their n8n workflow pictures (`mk-n8n-workflow.png`, `chesshatch-n8n-workflow.png`, and `skies-error-handler-n8n.png`). Each comment contains a ready-made block for any further pictures: add your images next to `index.html`, uncomment the block, and point each `src` at your file. Blur or replace any real names, phone numbers, or emails first.

## Case studies

Every full stack project has a case study. They are the `.page-view` blocks in `index.html` with these IDs: `rolesearchhq-case`, `vault01-case`, `oz-case`, `redbelly-case`, `redbelly-v2-case`, `auditlynx-case`, `chesshatch-case`, `urpassport-case`, and `travelsleek-case`. The `CASES` map in the project script connects each project key to its case study, and that link opens from the "Read case study" button in the project's details panel.

Each case study uses the same mobile-first structure: a summary, a flow, screenshots, the problem and solution, numbered steps, engineering highlights, the tech stack, and links. The images stack on small screens, and the text is written to be readable at 390px wide.

## Visitor stats

The Vercel Web Analytics script is already in `index.html`. To turn it on, open the project in Vercel, go to Analytics, press Enable, and redeploy. Page views show on the free plan. The site also sends click events (project opens, CV, email, socials), which need a paid plan to appear.

## Search

After deploying, submit `https://maleekskies.vercel.app/sitemap.xml` in Google Search Console. The structured data in `index.html` includes the name "Malik Adesiyan"; delete the `alternateName` line to use the handle only.

## Files

- `index.html`: the site itself
- `cv.pdf`: linked from the CV button in the nav
- `favicon.ico`, `favicon-32.png`, `favicon-192.png`: browser tab icon, multiple sizes
- `preview.jpg`: the image shown when the site link is shared on social platforms or messaging apps
- the `.jpg` and `.png` files in the root: screenshots shown in the project details panel
- `robots.txt`, `sitemap.xml`: search engine files
- `README.md`: this file

## Deployment

This is a static site, so it can be deployed anywhere that serves static files. Upload all the files above together, in the same folder, since `index.html` links to several of them by relative path and they'll break if separated.

- **Netlify Drop**: drag and drop the folder at [app.netlify.com/drop](https://app.netlify.com/drop)
- **Vercel**: create a project and upload the folder
- **GitHub Pages**: push the files to this repo, then enable Pages in Settings > Pages, pointing to the main branch

No build command or install step is needed. `index.html` just needs to stay named that so it's served as the homepage.

## Local Preview

Open `index.html` directly in any browser. No server required.

## Contact

- Email: maleekskies@gmail.com
- X: [@maleekskies](https://x.com/maleekskies)
- Telegram: [@maleekskies](https://t.me/maleekskies)
- LinkedIn: [maleekskies](https://www.linkedin.com/in/maleekskies/)

## AI assistant

The assistant box at the bottom of the page talks to `api/ask.js`, a Vercel serverless function that calls the Gemini API. It answers questions about the portfolio and gives practical business automation plans, preferring free or self-hosted tools. The key stays on the server. It runs on the Gemini free tier, so you pay nothing. The free tier does use your visitors' questions to improve Google's products, so do not put anything private in the assistant's facts.

1. Get a free key at [aistudio.google.com/apikey](https://aistudio.google.com/apikey). No card needed.
2. In Vercel: Project, Settings, Environment Variables, add `GEMINI_API_KEY` (all environments), then redeploy.
3. Optional: `GEMINI_MODEL` (default `gemini-3.5-flash`) and `ALLOWED_ORIGINS` (comma-separated, add a custom domain).
4. Edit what the assistant knows by changing the `SYSTEM` text at the top of `api/ask.js`.

If the key is missing, the box tells the visitor to email you instead. The function limits message length, conversation length and requests per visitor.
