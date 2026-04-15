# Agent Instructions — DCB Horse Riding Club Website

This file tells AI coding agents how to work with this repository.

## Project Overview

A self-contained static HTML website for **DCB Horse Riding Club**, Yewalewadi, Pune. All CSS, JavaScript, and images are embedded directly in `index.html` (no build step, no dependencies).

## Architecture

- **Single file:** `index.html` holds everything — styles (`<style>`), markup, scripts (`<script>`), and base64-encoded images.
- **Fonts:** Loaded from Google Fonts (Playfair Display, Montserrat).
- **No framework, no bundler.** Plain HTML/CSS/JS only.

## CSS Variables (design tokens)

| Variable | Role |
|---|---|
| `--br` | Brand brown `#7a442a` |
| `--brd` | Dark brown `#5c3020` |
| `--gd` | Gold `#ffbd59` |
| `--gdk` | Dark gold `#e0a030` |
| `--tx` | Body text `#2a1810` |
| `--fd` | Display font (Playfair Display) |
| `--fs` | Sans font (Montserrat) |

## Key Sections & IDs

| Section | Anchor / ID |
|---|---|
| Hero | `.hero` |
| About | `#about` |
| Programs / Lessons | `#programs` |
| Our Horses | `#horses` |
| Trainers | `#trainers` |
| Gallery | `#gallery` |
| Contact / Book | `#contact` |
| Footer | `footer` |

## Common Tasks

### Update contact number
Search for the phone number — it appears in the nav CTA link and in the `sendWA()` JavaScript function.

### Add a new program card
Find the programs grid section and duplicate an existing `.prog-card` block. Update the icon, heading, and description text.

### Replace a photo
Images are base64-encoded inside `<img src="data:image/...">` tags. Replace the entire `src` value with a new base64 string, or switch to a file path if images are served separately.

### Change hero image
The hero `<img class="hero-img">` tag contains a base64 `src`. Swap it with a new image. The `object-position: center 20%` CSS keeps focus on the upper portion of the image.

### Update WhatsApp booking
The `sendWA()` function in the `<script>` block at the bottom of the file constructs the WhatsApp message and opens the `wa.me` link. Update the number or message template there.

## Do Not

- Do not introduce a build pipeline or package manager unless explicitly asked.
- Do not split the file into separate CSS/JS files unless explicitly asked.
- Do not add tracking scripts or third-party analytics without the owner's approval.

## Deployment

Push to the `main` branch. Enable GitHub Pages under **Settings → Pages → Deploy from branch (main, / root)** to publish at `https://niharikaargade.github.io/dcbhorseridingclub/`.
