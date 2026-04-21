# Deployment Guide for Claude Code

This folder is ready to be pushed to GitHub and published via GitHub Pages. Hand this whole folder to Claude Code along with the prompt below.

---

## What's in this folder

```
ironman-belgrade/
├── index.html       # The app — do not modify
├── README.md        # Project description + pending-changes log
├── .gitignore       # macOS/editor noise
└── DEPLOY.md        # This file
```

## Prompt to give Claude Code

Copy everything between the lines below into Claude Code, after `cd`-ing into this folder on your MacBook.

---

I'm in a folder called `ironman-belgrade` containing a single-file
HTML app (`index.html`), a README, and a `.gitignore`. This is a
frozen artifact — **do not modify any of these files**.

Task: publish this folder as a private GitHub repo served via GitHub
Pages, so I get a live HTTPS URL I can open on my iPhone.

Please do the following:

1. Confirm `git` is available, and check whether `gh` (GitHub CLI)
   is installed and authenticated. If `gh` is not authenticated,
   stop and tell me what to run (`gh auth login`) — don't guess.

2. Initialise a git repo in this folder, add all files, commit with
   message "Initial commit — frozen v1".

3. Using `gh`, create a new **private** repo called
   `ironman-belgrade` under my account.

4. Push the local `main` branch to that new repo.

5. Enable GitHub Pages on the repo: source = `main` branch,
   directory = `/` (root). Use `gh` for this if possible
   (`gh api` with the Pages endpoint).

6. Wait 30–60 seconds, then `curl -sI` the Pages URL to verify
   it returns HTTP 200 and serves the HTML (check for the title
   `70.3 Belgrade` in the body).

7. Print the final live URL clearly.

Notes:
- Default branch must be `main`, not `master`.
- Do not add a build step, package.json, framework, or tooling.
  This is deliberately a zero-dependency static file.
- Do not minify or alter `index.html` in any way.
- If any step fails, stop and tell me which one — don't continue
  past an error.

Before you start, please confirm:
- `git --version`
- `gh --version` (and `gh auth status`)
- current directory contents with `ls -la`

---

## After deployment

Once live, open the URL in Safari on your iPhone and tap Share → Add to Home Screen. The icon will be a generic placeholder for now — the proper custom icon comes in the next iteration (tracked in README).

## Iteration workflow (for future changes)

When we come back to implement the pending changes:

1. I'll rewrite `index.html` in Claude
2. You replace the file in this folder
3. `git commit -am "describe change" && git push`
4. GitHub Pages re-publishes within ~30 seconds
5. Refresh your phone

No rebuild, no redeploy. Just edit, commit, push.
