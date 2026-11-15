PHEONIX ENTERPRISES - PUBLISHING GUIDE

Files
  index.html       the website (logo is built in, so this file works on its own)
  assets/logo.jpg  copy of your logo (optional, for other uses)
  favicon.svg      browser tab icon
  404.html         "page not found" page
  robots.txt       search engine rules
  _headers         security headers for Netlify and Cloudflare Pages
  vercel.json      security headers for Vercel

How to publish (any of these)
  Netlify / Cloudflare Pages: drag and drop this folder (or the zip) into the dashboard.
  Vercel: import the folder; vercel.json is picked up automatically.
  Other hosts (cPanel, Apache, Nginx): upload the files, then add the headers listed in _headers
  in your server settings. The page still works without them because it also has a built-in
  Content-Security-Policy tag, but the headers add clickjacking protection and HTTPS enforcement.
  Always serve the site over HTTPS (all of the hosts above do this for you).

After you have your domain
  1. Add <link rel="canonical" href="https://YOUR-DOMAIN/"> and og:url to index.html.
  2. Add a Sitemap line to robots.txt.
  3. Add an og:image (a 1200x630 image) for nicer link previews.

Before you publish
  - Replace the three "Sample" reviews (SEED list in the script) and the six "Sample concept"
    project cards with real work when you have it.
  - If you edit any <script> in index.html, the Content-Security-Policy hashes must be updated,
    otherwise the browser will block the script. Ask for the hashes to be regenerated.
