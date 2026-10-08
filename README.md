# KTM INVEST — Telegram Landing Page

A fast, responsive, single-file landing page inspired by the structure of the supplied Earning Shadow reference: prominent Telegram CTA, 3 benefit statements, 3-second automatic redirect, countdown without a cancel button, and disclaimer.

## Run

Open `index.html` in your browser or upload the folder to any static hosting provider. It has no npm dependencies. Vercel Web Analytics loads automatically when deployed on Vercel with Web Analytics enabled.

## Change your details

Open `index.html` in VS Code and edit the `SITE_CONFIG` object near the bottom:

- `brand`: your brand or community name
- `titleLine`, `titleAccent`, `eyebrow`, `description`: headline and copy
- `telegramUrl`: your own Telegram invite link
- `registrationUrl`: optional website registration link; the register link appears automatically when supplied
- `redirectEnabled`: `true` for an automatic Telegram redirect, `false` to keep users on your landing page
- `redirectSeconds`: time before redirect; between 1 and 60 seconds
- `disclaimer`: your real, accurate disclosure

The page uses your supplied image URL as both its header and hero logo, and as the favicon: `https://img.remit.ee/i/wassXrMpH8Fo`. Because this image is hosted externally, it needs to remain accessible; for production reliability, download and host it locally if you have the image file.

To change the colors, look for `:root` at the top of the page's `<style>` element.

## Deploy to Vercel

1. Put this folder in a new GitHub repository.
2. Import that repository into Vercel as an **Other** (static) project.
3. Leave the build command blank and use the project root as the output directory (or use Vercel CLI from this folder).
4. Deploy and test both mobile and desktop layouts and the Telegram invite URL.

You can also use any other static host (Netlify, GitHub Pages or hosting file manager).

## Vercel Web Analytics

The page includes the official lightweight script `/_vercel/insights/script.js` in `<head>`. No `npm install` or Next.js conversion is needed for this static HTML website.

1. Open your project in the Vercel dashboard.
2. Go to **Analytics** and enable **Web Analytics** (if not yet enabled).
3. Redeploy this version and open your production URL.
4. Check Analytics after a visit; the HTML file opened locally will not serve the Vercel analytics script.

Analytics collects page views according to Vercel settings. It does not independently prove Telegram joins, particularly when visitors are redirected after 3 seconds.

## Important

- **No payment collection, registration database, custom conversion tracking, or admin dashboard** is provided in this starter.
- A static page alone cannot confirm that a user joined Telegram; this page never invents member counts or withdrawal proof.
- Ads platforms may have special rules about automatic redirects. Consider changing `redirectEnabled` to `false` for ads, and use factual claims only.
- Use only a Telegram channel you own or are authorized to promote. The included URL is a placeholder based on the channel link previously supplied for KTM INVEST. Verify it before publishing.
- The page is not affiliated with Telegram, Vercel, or Meta.
