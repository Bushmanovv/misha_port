# The Digital Stage — Vercel + Gmail submission

Static, phone-friendly classical pianist discovery questionnaire. No npm/build step.

## One-time Gmail connection (required)

Vercel cannot send messages to a Gmail inbox from static HTML alone. This website uses **Formspree** to securely accept and forward submissions.

1. Sign up at https://formspree.io/ using the **Gmail address that should receive the answers**.
2. Verify that address and create a form called **Pianist Discovery**.
3. Copy the form endpoint (`https://formspree.io/f/XXXXXXXX`).
4. `config.js` is already configured with `https://formspree.io/f/mvkzyoap`. To change forms later, edit this file.
5. Commit and push to GitHub. Vercel redeploys automatically.
6. Complete a **test submission** on the live site. Check the Formspree submissions dashboard AND your Gmail inbox, including Spam. Configure email notifications in Formspree if needed.

The submit button sends the complete report and displays success **only after the service accepts it**. The original copy/download options stay available as backups. If sending fails, browser autosave preserves answers for retry. Note that endpoint alone is not a secret, but enable Formspree spam protections as appropriate.

**Before configuring `config.js`, the form will not send.** No email or account credentials should be put in client-side code.

## Local testing

From the folder containing `index.html`: `python3 -m http.server 8080`, then open `http://localhost:8080`.

## Push changes to GitHub

```bash
git add index.html config.js README.md
git commit -m "Send pianist discovery submissions to Gmail via Formspree"
git push origin main
```

## Vercel deployment

Import the GitHub repo at https://vercel.com/new. Framework preset: **Other**; root `./`; no build command; output directory `.`.

## Phone acceptance test

Use a real iPhone or Android phone to submit a complete test form, verify confirmation, and verify the message reaches Gmail. Check 320–430px screens for overflow and touch target comfort.
