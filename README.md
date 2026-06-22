# f4rvk.github.io

Personal academic website, built with the [al-folio](https://github.com/alshedivat/al-folio) Jekyll theme.

## Local preview
```bash
bundle install
bundle exec jekyll serve
# open http://localhost:4000
```

## Deployment (GitHub Pages via GitHub Actions)
This site uses Jekyll plugins that GitHub Pages' default build does **not** support, so it
deploys through GitHub Actions (the workflow is in `.github/workflows/deploy.yml`):

1. Push these files to the **`main`** branch of the `f4rvk.github.io` repo.
2. **Settings → Actions → General → Workflow permissions** → select **"Read and write permissions"**.
3. On push, the *Deploy site* Action builds the site and pushes the result to a **`gh-pages`** branch.
4. **Settings → Pages → Build and deployment** → Source: **"Deploy from a branch"** → Branch: **`gh-pages`** / **`(root)`**.

After the first successful Action run + the Pages setting above, the site is live at
<https://f4rvk.github.io>.

## Where to edit things
| Content | File |
| --- | --- |
| Homepage / bio | `_pages/about.md` |
| Profile photo | `assets/img/prof_pic.jpg` |
| Social links, email, CV link | `_data/socials.yml` |
| Publications | `_bibliography/papers.bib` |
| CV page content | `_data/cv.yml` |
| CV PDF (download button) | `assets/pdf/FTYalcin_CV_Jun26.pdf` |
| Projects table | `_pages/projects.md` |
| Site-wide settings | `_config.yml` |
