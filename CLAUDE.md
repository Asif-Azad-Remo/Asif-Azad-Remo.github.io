# Project: Asif Azad Remo — portfolio site

A static personal portfolio website. It is a single `index.html` plus a
downloadable CV (`Asif_Azad_Remo_CV.pdf`), published to GitHub Pages using the
GitHub Actions workflow in `.github/workflows/deploy.yml`. No build step.

## When the user says "Deploy it"

Deploy this folder to the user's GitHub Pages repository:

    https://github.com/Asif-Azad-Remo/Asif-Azad-Remo.github.io

Run these steps from the project root:

1. Initialise git if needed:

       git init
       git branch -M main

2. Stage and commit everything (including `.github/` and the PDF):

       git add -A
       git commit -m "Deploy portfolio site"

3. Set the remote (add it, or update it if it already exists):

       git remote add origin https://github.com/Asif-Azad-Remo/Asif-Azad-Remo.github.io.git
       # if it already exists:
       # git remote set-url origin https://github.com/Asif-Azad-Remo/Asif-Azad-Remo.github.io.git

4. Push to `main`:

       git push -u origin main

   - If the push is rejected because the remote already has commits (for
     example an initial `README.md`), reconcile and retry:

         git pull --rebase origin main
         git push -u origin main

   - If the histories are unrelated and the remote only holds a placeholder
     README that is safe to replace, you may instead run (ask the user first
     if there is any doubt):

         git push -u origin main --force

## What happens after the push (the user does nothing else)

- `.github/workflows/deploy.yml` runs on every push to `main`.
- `actions/configure-pages` enables GitHub Pages with the **GitHub Actions**
  source; `upload-pages-artifact` + `deploy-pages` publish the site.
- Live URL: **https://asif-azad-remo.github.io/**
- The GitHub token used by `git push` must have permission to push to this
  repo. If pushing over HTTPS prompts for credentials, the user needs to be
  logged in to GitHub (e.g. via the GitHub CLI `gh auth login` or a stored
  Personal Access Token). Tell the user if authentication is required — do not
  invent or ask for tokens.
- If the very first workflow run fails with "Pages not enabled", have the user
  open the repo's **Settings -> Pages** once and set **Source: GitHub Actions**,
  then re-run the workflow. (configure-pages usually enables this automatically.)

## Keep these at the repository root
- `index.html`
- `Asif_Azad_Remo_CV.pdf`  (the "Download CV" links are relative to it)
