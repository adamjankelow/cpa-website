# Marc Douieb & Co. — CPA Website

A single-page bilingual (Hebrew/English) website for Marc Douieb & Co., Certified Public Accountants, Ramat Gan.

## Structure

Everything lives in one self-contained file: **`index.html`** (no build step, no dependencies). Content for both languages sits side by side in the markup — each bilingual piece of text has two elements tagged `data-he` and `data-en`; the `lang-toggle` button flips `dir`/`lang` on `<html>` and CSS shows/hides accordingly. Language choice is remembered via `localStorage`.

## Editing content

Open `index.html` in any text editor and search for the section you want to change (`id="services"`, `id="team"`, `id="contact"`, etc.). Anything wrapped in square brackets, e.g. `[XX]`, `[0X-XXXXXXX]`, `[info@marcdouieb.co.il]`, is placeholder copy waiting on real details from the firm — replace both the Hebrew (`data-he`) and English (`data-en`) versions of each line.

Still-placeholder items to fill in:
- Founding year, years in practice, client count, CPA license number (hero panel)
- Second partner's bio and both partners' photos
- Address, phone, email, and business hours (footer contact section) — once real, update both the visible text **and** the `tel:`/`mailto:` link targets in the same rows
- Copyright year in the footer

## Local preview

No build tools needed — just serve the folder and open it:

```bash
python3 -m http.server 8080
# visit http://localhost:8080
```

## Deployment

Hosted via **GitHub Pages** from the `main` branch (root). Any push to `main` updates the live site automatically — usually within a minute.

Live URL: https://adamjankelow.github.io/cpa-website/
