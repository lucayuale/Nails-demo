# Velvet Nail Studio — Booking Concept | VYB

> **A VYB portfolio demonstration** · Fictional nail studio · Booking UI preview (not connected)

**Velvet Nail Studio** is an editorial, responsive website concept for a nail salon, created by **VYB — Web Design & Development**. It shows how manicure services, nail-art inspiration and a future online booking experience could be presented in one cohesive brand.

**Demo notice:** Velvet is **not a real nail studio**. Images are illustrative references, and the service names, durations, prices and opening hours are examples. **The booking calendar is not connected.** No appointment, payment, or customer contact is collected through this demo. In particular, **this version does not use the Obsidian/Barbería Setmore calendar**.

## Features

- Elegant one-page design with distinct **Services**, **Nail Edit / Gallery**, **Studio**, **Booking** and **Visit** sections.
- Bilingual **English / Spanish** content with an interactive language switcher.
- Responsive layout for mobile and desktop.
- Seven sample services, illustrative prices and durations.
- Five gallery looks with full-size lightbox, plus two additional local images.
- Booking-themed call-to-action buttons. Without a configured provider, they display a clear informational status instead of redirecting visitors.
- Keyboard-accessible controls, mobile menu, subtle reveal animations and reduced-motion support.
- Static frontend written in **HTML, CSS and vanilla JavaScript**; no npm dependencies, backend, user accounts or database.

## Folder layout

```text
index.html            Main website / GitHub Pages entry point
config.js             Studio content, translations, services, imagery and booking settings
app.js                Language switcher, service cards, gallery, navigation and booking actions
styles.css            Responsive styles and animations
assets/               Seven local .webp photos and favicon.svg
.nojekyll             GitHub Pages static-site hint
README.md             This document
COMO_PUBLICAR.txt     Spanish step-by-step publishing guide
```

**Important:** `index.html`, `config.js`, `app.js`, `styles.css` and the entire `assets/` directory must be uploaded together to the **repository root**. Leaving out `assets/` causes blank or broken imagery on GitHub Pages.

## Local preview

From the directory containing `index.html`, run:

```bash
python -m http.server 8080
```

Then open `http://localhost:8080/`. On Windows, `py -m http.server 8080` also works. No build step is needed for this deployable demo.

## Publish on GitHub Pages

1. Create a new repository under a GitHub account you control (for example `Nails-demo`).
2. Extract this ZIP on your computer. Use **Add file → Upload files** to upload **all extracted files and the entire `assets/` directory** directly to the repository root. Do **not** upload the ZIP as a single file or nest the website under an extra parent directory.
3. Commit the files to the `main` branch.
4. Go to **Settings → Pages** and select **Deploy from a branch → main → /(root)**, then Save.
5. In **Actions**, confirm that the Pages deployment has completed; open the real **Visit site** link in **Settings → Pages**.
6. Test images, language switcher, service cards, gallery lightbox, mobile menu and booking buttons. A booking button should display a *not connected* message.
7. If images are missing, verify exact paths such as `assets/hero.webp`, then hard-refresh after the successful deployment. You don't need to delete the Pages site.

No GitHub Pages link is hardcoded because the repository name is not known yet.

## Booking configuration

This project is the **Booking layout**, but its published demo intentionally has no live booking provider:

```js
"booking": {
  "url": "",
  "mode": "modal"
}
```

The booking modal code remains in `app.js`, ready for a real studio's supported Setmore booking URL. Until that URL is configured, the calls to action display an explanatory message and **cannot create real appointments**. For customer delivery, configure the customer's own account and test availability, service mapping, confirmations and cancellations before accepting appointments.

For this **GitHub Pages-ready package**, make presentational changes directly in `config.js` and related static files. The original development ZIP also includes a separate generator/source project, which is **not** needed for this deployment; generating again from the old source would overwrite demo-only changes unless the source configuration is updated too.

## Responsible use

- The studio, business identity, contact details, location and pricing are illustrative.
- Never add personal credentials, API keys or unpublished customer data to a public repository.
- Confirm rights and licenses for reference photography before using it for a real client.
- GitHub Pages publishes static files publicly; this demo does not store or send customer form submissions.

## Español

Esta es una **demo ficticia de salón de uñas**, creada por VYB. Incluye menú de servicios, galería de diseños, vista de reservas y cambio de idioma español/inglés. **Los turnos no están conectados** y no aparece ninguna URL de Obsidian. Los botones Booking avisan que la agenda está pendiente de configuración.

Para publicarla, descomprimí el ZIP y subí **todos los archivos junto con la carpeta `assets/`** a la raíz de tu repositorio. Activá **Settings → Pages → Deploy from a branch → main → /(root)**. Si faltan imágenes, revisá que la carpeta `assets/` esté publicada y que el último despliegue haya terminado.

---

**VYB — Web Design & Development** · Portfolio demo, no real appointments.
