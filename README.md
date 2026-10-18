# The Digital Stage — classical pianist discovery

A responsive, static, single-page client discovery website. No Node/npm build required.

## Run locally

Open `index.html` in a browser, or in this directory run `python3 -m http.server 8080` and visit `http://localhost:8080`.

## Deploy to Vercel

1. Push **the files in this folder** (`index.html`, `vercel.json`, `README.md`) to the root of a GitHub repository.
2. In https://vercel.com/new import that repository.
3. Framework Preset: **Other**; Root Directory: `./`; Build Command: none; Output Directory: `.`.
4. Click Deploy. Pushing to `main` will redeploy automatically once connected.

## How client answers work

The primary action **Share my answers** opens the mobile share sheet, ideally sharing a `.txt` file to WhatsApp, Messages, email, etc. If unsupported it attempts plain-text sharing, copying, or a download. **Vercel does not receive or store these submissions.** The client must send the answers to you, and should verify they sent them. Browser-local autosave is supported (same device and browser only).

For automatic inbox collection later, integrate a form service or an authenticated Vercel backend; static Vercel hosting alone does not process form POSTs.

## Mobile QA

At minimum check 320px, 375px, 390px, 430px and desktop widths; test links opening and coming back; check the share sheet on a real iPhone/Android device.
