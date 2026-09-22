# Pawni Tyagi — Portfolio

Static site. One HTML file plus a folder of screenshots. No build step, no dependencies.

    index.html
    shots/        seven screenshots used on the page

## Deploy on Vercel (the way you did FoodBridge)

1. Make a new GitHub repo, e.g. `portfolio`.
2. Put `index.html` and the `shots/` folder in the root of it and push.
3. On vercel.com: Add New -> Project -> import that repo.
4. Framework preset: **Other**. Leave build command and output directory empty.
5. Deploy. You get `portfolio-<something>.vercel.app`.
6. Project -> Settings -> Domains to rename it to something like `pawnityagi.vercel.app`.

That URL is what goes on your resume and in application forms.

## Alternative: GitHub Pages

Push the same two items, then repo Settings -> Pages -> Source: `main`, folder `/root`.
You get `pawniityagii.github.io/portfolio`.

## Editing later

Everything is in `index.html` — the CSS sits in one `<style>` block at the top,
the content is plain HTML below it. To swap a screenshot, drop a new file into
`shots/` with the same name.

## Note on the link preview image

`og:image` points at `shots/fb-landing.jpg` relative to the site. Some platforms
(LinkedIn, WhatsApp) want a full URL. Once you know your domain, change that one
line to the absolute address, e.g.
`<meta property="og:image" content="https://pawnityagi.vercel.app/shots/fb-landing.jpg">`
