# learnspanishwithdaniel website

The public website for my business, Español con Daniel: Spanish lessons for Russian speakers. Live at https://learnspanishwithdaniel.xyz.

## About me (the owner)

I'm not a programmer. Explain changes in plain language, and tell me in a sentence or two what changed and how to see it. Before anything big or hard to undo, tell me the plan and wait for my OK.

## What's here

- `index.html`: the landing page. It includes the game teaser, the reviews and the booking links.
- `placement-game/index.html`: Palabra, the placement game. It ends with an email gate, then shows the player's level.
- Shared files at the root: favicons, `social-preview.jpg` (the link preview image) and `avatars/` (the reviewers' photos).

Every page is a single self-contained HTML file with its CSS and JS inline, and there is no build step. Keep it that way unless there's a clear reason not to.

## Content and language

The site is written for Russian speakers (`lang="ru"`), with Spanish words as the learning content. Write new copy in Russian, matching the tone of the existing text.

## Services the pages use

- **Brevo** collects the email from the placement game's gate. It is sent the same way Brevo's own form sends it.
- **Calendly** handles booking a lesson.
- **Google Analytics (gtag)** and the **VK pixel** (`top-fwz1.mail.ru`) handle analytics. If you add or rename a tracked event, tell me so I can update my ad campaigns.

## Publishing

GitHub Pages publishes `main` to the domain in `CNAME`. Anything committed to `main` is public, so:
- Never commit secrets, drafts or marketing material that isn't meant to be on the site.
- Make changes on a branch, preview them, then open a pull request. Merging it publishes the change.

Preview locally with the `static` launch config (`.claude/launch.json`), which serves the folder at http://localhost:8765.

## What belongs in this repo

Only static pages served on this domain: the site, small games like the placement game, and a blog later on. Anything that needs a server, secret API keys or lots of art gets its own repo. For example, the situations game lives in `~/dev/situations-game`.
