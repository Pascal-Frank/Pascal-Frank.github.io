# Pascal Frank – personal website

A plain static site with no build step: one page (`index.html`) plus one stylesheet (`style.css`).
GitHub Pages serves it as is.

```
index.html          all content (Home / Research / CV tabs)
style.css           look and layout
images/photo.jpg    portrait (548×600 or any roughly 1:1 crop works)
cv/CV_Frank.pdf     the CV that the site links and embeds
data/<paper>/       xlsx files offered for download under a paper
.nojekyll           tells GitHub Pages not to run Jekyll
```

## One-time setup

1. Create a GitHub repository named exactly `<your-github-username>.github.io` (public).
2. Upload everything in this folder (drag and drop on the repo page → **Add file → Upload files**).
3. Repo **Settings → Pages**: Source = *Deploy from a branch*, Branch = `main`, folder = `/ (root)`.
4. After a minute the site is live at `https://<your-github-username>.github.io`.
5. Optional: a custom domain (e.g. `pascalfrank.com`): add it under Settings → Pages → Custom domain and
   follow GitHub's DNS instructions.

## Updating the CV

Upload the new PDF with the **same name** to `cv/` (Add file → Upload files → `cv/CV_Frank.pdf`).
GitHub replaces the old file, and every link stays the same.

## Going live with the Job Market Paper (with data)

1. Upload the xlsx files to `data/jmp/` (and the paper PDF, e.g. to `papers/`).
2. In `index.html`, find the block marked `JOB MARKET PAPER`.
3. Fill in the bracketed fields, point the `href`s at your files, and delete the word `hidden`
   in `<div class="jmp" hidden>`.
4. On the Home tab, fill in the line `<p class="jmp-home" hidden>` and delete its `hidden` too.
5. Commit. The JMP appears at the top of the shaded block, above Publications, with a Data box under it.

For more papers, copy an existing `<article class="paper"> … </article>` block.
An abstract is optional; wrap it in `<details><summary>Abstract</summary><p>…</p></details>`
to make it collapsible.

## Small edits

On github.com, open `index.html` → pencil icon → edit → **Commit changes**. The site updates within a minute.
Remember to bump "Last updated" in the footer.
