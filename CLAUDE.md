# Calendário UniTI

Public one-hour slot scheduler for October 2026. Anyone opens the page, types a name and marks the hours they can. The user has no developer background: explain in plain Portuguese (Portugal), one step at a time.

## How it works
- The whole site is one file: `index.html` (HTML, CSS and JS together). No build step.
- Votes are stored in Firebase Realtime Database at the `DB_URL` set near the top of the script. The page reads and writes through its REST address. Do not put passwords or tokens in any file.
- `regras-firebase.json` is a backup of the Firebase rules. It is not published to GitHub and is listed in `.gitignore`.
- Hosting: GitHub repo `anatolionobre-code/calendario-uniti`, branch `main`. Netlify is linked to it and publishes every push within seconds. Public link: https://clever-dasik-4ba9c1.netlify.app/

## Rules of the page
- Language: Portuguese (Portugal). Title: "Calendário UniTI - Para equipas desencontradas".
- Visual style inspired by wondercom.pt (deep blue, cyan, Raleway and Open Sans). Never use their logo.
- October 2026 only. Working days only, 9h–18h, one-hour slots (last slot starts at 17h).
- Excluded: weekends and Portuguese bank holidays (5 October, Implantação da República).
- One vote = one Firebase record at `votes/<slot>__<hex of lowercase name>` with `slot` and `name`.

## Working agreements
- Show the user what will be pushed and ask before every `git push`.
- Check the live page after a push.
