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

## Updating the CV

Upload the new PDF with the **same name** to `cv/` (Add file → Upload files → `cv/CV_Frank.pdf`).
GitHub replaces the old file, and every link stays the same.


## Small edits

On github.com, open `index.html` → pencil icon → edit → **Commit changes**. The site updates within a minute.
Remember to bump "Last updated" in the footer.
