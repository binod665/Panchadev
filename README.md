# Binod Bhandari — Portfolio Website

A clean, bilingual (English / Nepali) personal portfolio site built with plain HTML, CSS, and JavaScript — no build tools, no frameworks. Ready to host for free on GitHub Pages.

## File structure

```
index.html        → all page content
css/style.css      → all styling (colors, type, layout are set as CSS variables at the top)
js/script.js       → mobile menu, scroll animations, footer year
images/            → placeholder photos (swap these with your real photos)
```

## 1. Replace the placeholder photos

The `images/` folder currently has generated placeholder art (warm gradient + mountain silhouette) so the site looks complete out of the box. Replace each file with your own photo **using the exact same filename**, and the site will update automatically:

| Filename | Used for |
|---|---|
| `images/hero-bg.jpg` | Background behind your name on the homepage |
| `images/family.jpg` | "Family Photo" in the Family section |
| `images/tour.jpg` | "Tour Photo" in the Off the Clock section |
| `images/captured.jpg` | "Photo Captured By Me" in the Off the Clock section |
| `images/office.jpg` | "My Office" in the Work section |

Recommended size: roughly 1000×1250px (portrait) for the polaroid photos, and at least 1600px wide for the hero background. JPG or PNG both work — just keep the filename and extension the same, or update the `src`/`style` reference in `index.html` if you rename them.

## 2. Edit the text

Open `index.html` in any text editor. Each section has the English paragraph followed by a `<p class="ne">` paragraph with the Nepali translation — edit either independently. Update:
- The email address in the footer (`mailto:hello@binodbhandari.com.np`)
- The GitHub / LinkedIn / Facebook links in the footer (`href="#"` placeholders for LinkedIn and Facebook)
- Any bio details you'd like to change

## 3. Host it on GitHub Pages (free)

1. Create a new repository on GitHub (e.g. `binodbhandari.github.io` if you want it at the root of your GitHub username, or any name like `portfolio`).
2. Upload all the files in this folder to the repository, keeping the same folder structure (`index.html` at the root, `css/`, `js/`, `images/` as subfolders).
   - Easiest way: on the repository page, click **Add file → Upload files**, drag in everything, and commit.
   - Or via git from your computer:
     ```bash
     git init
     git add .
     git commit -m "Initial portfolio site"
     git branch -M main
     git remote add origin https://github.com/<your-username>/<repo-name>.git
     git push -u origin main
     ```
3. In the repository, go to **Settings → Pages**.
4. Under "Build and deployment", set **Source** to "Deploy from a branch", choose branch `main` and folder `/ (root)`, then **Save**.
5. Wait a minute or two — GitHub will give you a live URL, usually `https://<your-username>.github.io/<repo-name>/`.

## 4. Point your domain (binodbhandari.com.np) at it — optional

If you want `binodbhandari.com.np` itself to load this GitHub Pages site instead of your current host:
1. In repository **Settings → Pages → Custom domain**, enter `binodbhandari.com.np` and save (this creates a `CNAME` file in your repo automatically).
2. At your domain's DNS provider (wherever you manage binodbhandari.com.np's DNS), add a `CNAME` record pointing to `<your-username>.github.io`, or `A` records pointing to GitHub's Pages IP addresses (GitHub's Pages documentation lists the current IPs — search "GitHub Pages custom domain A records" if needed).
3. DNS changes can take a few hours to propagate.

## Customizing the look

All colors and fonts are defined as CSS variables at the top of `css/style.css`:

```css
:root{
  --ink:        #16213A;   /* dark navy backgrounds */
  --gold:       #E2A33C;   /* accent color */
  --forest:     #2F4538;   /* dark green section */
  --parchment:  #F6F0E4;   /* light background */
  ...
}
```

Change any hex value there to shift the whole site's palette consistently.
