# Jomol Jose — Portfolio (Tab-Based, Space / Purple Theme)

A single-page portfolio site — no build tools, no dependencies. HTML, CSS, and vanilla JS in one file, plus your photo and resume.

## Files
- `index.html` — the entire site
- `profile.jpg` — your headshot, used on Home and About
- `resume.pdf` — your resume, wired up to the "Download Resume" and "View in Browser" buttons on the Resume tab

## How navigation works
This is not a scrolling one-pager. The navbar (Home / About / Projects / Resume / Contact) swaps between pages with JavaScript — clicking a link hides the current page and shows the new one, no scrolling involved. The **Home page locks page scroll and fits the viewport** so your photo and intro are the entire first screen.

Routing logic is in the `<script>` at the bottom of `index.html` — look for `function showPage(id)`. Each page is a `<div class="page" id="page-xxx">`; only the one with `.active` is shown.

## Editing it
- **Typewriter roles**: search for `const roles = [` in the script, edit the array
- **Add a project**: copy a `.project-card` block inside `<div id="page-projects">`
- **Add an experience entry**: copy a `.commit` block inside `<div id="page-resume">`
- **Swap the resume file**: replace `resume.pdf` with a new file of the same name, or update the `href="resume.pdf"` references if you rename it
- **Colors/fonts**: all set once in the `:root { ... }` block near the top

To preview, double-click `index.html`, or use VS Code's "Live Server" extension for auto-refresh while editing.

## Deploying it
Keep `index.html`, `profile.jpg`, and `resume.pdf` in the same folder. Then:
- **GitHub Pages**: push this folder to a repo, enable Pages in repo settings
- **Vercel / Netlify**: drag-and-drop this folder onto their dashboard
- **Render**: deploy as a static site pointing at this folder

## Known placeholders to fill in
- Internship dates for Knovista Technologies and Infotact Solutions — search `<div class="meta">` in the Resume tab and add them
- Project card GitHub links aren't wired up yet — add a link block inside a `.project-card` if you want per-project repos linked
