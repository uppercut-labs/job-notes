# Job notes

Uppercut Labs browser form for a support note you can copy. The page is dark. You do not sign in, and the form has no server of its own.

What you type stays in the browser. Refreshing the page clears it. The Worker serves these files and does not receive the form.

## Live

https://job-notes.uppercut-labs.workers.dev

Open `index.html` in a browser for the same page without deploying.

## What it does

- Fields for one support interaction, with a prompt that changes by type
- A check that the required fields are filled before it writes a note
- The same headings on every note, which you review before copying
- Excel and Sheets buttons that unlock copying and leave the note on the page
- Copy to the clipboard, or select the note if the clipboard is blocked
- If you edit the form after generating, the note is marked out of date until you generate it again

## Deploy

Cloudflare Worker, static assets, Uppercut Labs account. The host is `workers.dev`. A custom domain would need a DNS decision, so this config does not attach one.

From the repository root, with Wrangler authenticated to that account:

```bash
npx wrangler@4.92.0 deploy
```

`npm run dev` serves the Worker locally after `npm install`.

## Origin

Devin Thomas published the clean-room tool at [devin-thomas/internal-notes-generator](https://github.com/devin-thomas/internal-notes-generator). Job notes is the Uppercut Labs edition of that browser form. You still fill it in locally, review the note, and copy it. This repository does not include employer code, the old host, or the workplace case write-up.

## Technology

HTML, CSS, and vanilla JavaScript. Geist is included under the SIL Open Font License (`fonts/OFL.txt`). The Uppercut Labs mark is the company logo, unchanged in shape.
