# Announcements: hosting + Canvas embed

Repo for all classes: https://github.com/drsrennie-stack/announcements-2026-Summer

## Naming convention (use for every class)

`announcements-[COURSE]_[YYYY-MM-DD].html`

This file: `announcements-BIO-004_2026-06-15.html`

Examples for other classes in the same repo:
- `announcements-BIO-431_2026-06-15.html`
- `announcements-BIO-304_2026-06-15.html`

Course code first, then ISO date, so the folder sorts cleanly by class and the dates stay in order. (You wrote "BIOL 004"; I used "BIO-004" to match your course pages and palette config. If your Solano catalog code is actually BIOL, say so and I will switch the prefix everywhere.)

## Step 1: Add the file to the repo

From a terminal:

```bash
git clone https://github.com/drsrennie-stack/announcements-2026-Summer.git
cd announcements-2026-Summer
# copy announcements-BIO-004_2026-06-15.html into this folder, then:
git add announcements-BIO-004_2026-06-15.html
git commit -m "Add BIO 004 announcements, 2026-06-15"
git push
```

## Step 2: Turn on GitHub Pages (one time)

In the repo: Settings, Pages, Source = your default branch, folder `/ (root)`, Save.

Your page URL will be:

```
https://drsrennie-stack.github.io/announcements-2026-Summer/announcements-BIO-004_2026-06-15.html
```

Open it once to confirm it loads.

## Step 3: Embed in Canvas

1. Open the Canvas announcement or page.
2. Click the `</>` (HTML editor) button in the Rich Content Editor.
3. Paste the snippet, then Save.

```html
<iframe
  src="https://drsrennie-stack.github.io/announcements-2026-Summer/announcements-BIO-004_2026-06-15.html"
  title="Announcements, BIO 004, June 15, 2026"
  width="100%"
  height="2200"
  style="border:0; max-width:1080px; width:100%;"
  loading="lazy">
</iframe>
```

## Height note

Canvas does not run the page's auto-height script (it only fires when the parent listens, which GitHub Pages and Kajabi do but Canvas does not). The iframe uses a fixed height. `2200` is a good start; if you see an inner scrollbar or extra blank space, change the number by 100 to 200 and re-save.

## If the iframe gets stripped

Canvas only allows iframes from domains your institution allowlists. `github.io` is commonly allowed, not always.

- If it disappears on Save, ask your Canvas admin to allow `github.io`.
- Fallback that always works: I can rebuild this as an inline-styled, script-free body fragment you paste straight into the Canvas HTML view, no hosting or allowlist needed.
