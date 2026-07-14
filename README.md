# Zhiwei Zhang — Academic Website

A lightweight, responsive English academic website based exclusively on `PD_application_CV.pdf`. It is designed for deployment at a GitHub Pages user site such as `https://<username>.github.io/`.

## Local preview

From this directory, run:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000/`. A local server is required for the Updates JSON to load.

## Structure

- `index.html` — profile, bio, research interests, updates, selected publications
- `research.html` — four CV-supported research themes
- `publications.html` — articles, in-submission manuscript, proceedings, presentations
- `experience.html` — education, research experience, technical skills
- `awards.html` — scholarships and honors
- `cv.html` — embedded CV viewer and download controls
- `data/updates.json` — maintainable updates data
- `assets/css/style.css` and `assets/js/main.js` — shared design and behavior
- `assets/images/` — portrait placeholder and favicon
- `assets/files/PD_application_CV.pdf` — public copy of the source CV

## Updating content

- **Bio and profile links:** edit the hero section in `index.html`.
- **Updates:** add a new object to the top of `data/updates.json`, using only the precision supported by the source (for example, `2026` rather than inventing a day).
- **Publications:** add the item to `publications.html`, preserve its status, and optionally add it to the selected list in `index.html`.
- **Portrait:** replace `assets/images/profile.jpg` with a web-optimized portrait, keeping the filename so the page and Open Graph image remain valid. Keep meaningful alt text.
- **CV:** replace `assets/files/PD_application_CV.pdf` with the new file, keeping the same filename so links remain valid.

## Information still needed

Google Scholar, ResearchGate, GitHub, and ORCID links are configured in `index.html`. A LinkedIn URL has not been provided, so no LinkedIn link is displayed. The public CV and website do not display an email address or phone number.

## Deploying to GitHub Pages

This site is ready for a user-site repository named `<username>.github.io`:

```bash
git branch -M main
git remote add origin https://github.com/<username>/<username>.github.io.git
git push -u origin main
```

On GitHub, open **Settings → Pages**, choose **Deploy from a branch**, select `main` and `/ (root)`, then save. The expected address is `https://<username>.github.io/`. Do not run `git remote add` if a remote already exists; inspect it first with `git remote -v`.

## Custom domain

In the repository’s **Settings → Pages**, enter the domain under **Custom domain** and follow GitHub’s displayed DNS instructions. Add the corresponding `CNAME` file only after the domain is known, and enable HTTPS after DNS validation.
