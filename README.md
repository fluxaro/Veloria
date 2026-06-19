# Veloria Healthcare Group

A single-page marketing website for **Veloria Healthcare Group** — a healthcare organization delivering patient-centered medical services across Nigeria.

**Tagline:** Advancing Care, Improving Lives.

## Overview

The site presents Veloria's services, mission, values, and locations through a modern, animation-rich layout. It is built with plain HTML, CSS, and JavaScript — no frameworks or build step required.

### Features

- Full-screen hero with parallax and animated stats
- Scroll-triggered reveal animations
- Infinite services marquee
- Responsive layout (mobile, tablet, desktop)
- Contact form with AJAX submission
- Google Fonts: Fraunces (display) + DM Sans (UI)
- Local healthcare imagery in `images/`

### Sections

| Section    | Content                                      |
|------------|----------------------------------------------|
| Hero       | Tagline, intro, key stats                    |
| About      | Company overview, founded 2018, Abuja HQ       |
| Services   | 10 core medical services                     |
| Showcase   | Brand quote banner                           |
| Mission    | Mission, vision, and six core values         |
| Locations  | Abuja, Kano, Port Harcourt, Enugu            |
| Contact    | Inquiry form and contact details             |

## Project Structure

```
lifecare-master/
├── index.html          # Main page
├── contact.php         # Contact form handler (requires PHP)
├── css/
│   └── veloria.css     # All styles
├── js/
│   └── veloria.js      # Animations, navigation, form AJAX
└── images/
    ├── hero.jpg
    ├── about-main.jpg
    ├── about-float.jpg
    ├── showcase.jpg
    └── locations.jpg
```

Legacy files from the original Life Care template (`style.css`, Bootstrap, Font Awesome, etc.) may still be present in the folder but are **not used** by the current site.

## Getting Started

### Option 1 — Open directly

Double-click `index.html` or open it in any modern browser. The contact form requires a PHP server to submit.

### Option 2 — Local PHP server (recommended)

```bash
cd lifecare-master
php -S localhost:8080
```

Visit [http://localhost:8080](http://localhost:8080).

### Option 3 — Static server (no contact form)

```bash
python3 -m http.server 8080
```

Pages and images will load; form submissions will not work without PHP.

## Contact Form

The form posts to `contact.php`. Before going live:

1. Set the recipient email in `contact.php`:

   ```php
   $address = "info@veloriahealthcare.com";
   ```

2. Ensure the server has PHP `mail()` configured, or replace it with SMTP (e.g. PHPMailer).

3. Update phone and email in `index.html` to match your real contact details.

## Customization

| What to change        | Where                          |
|-----------------------|--------------------------------|
| Colors & spacing      | `css/veloria.css` (`:root` vars) |
| Copy & sections       | `index.html`                   |
| Scroll / nav behavior | `js/veloria.js`                  |
| Images                | Replace files in `images/`       |
| Fonts                 | Google Fonts link in `index.html` |

## Browser Support

Works in current versions of Chrome, Firefox, Safari, and Edge. Animations respect `prefers-reduced-motion`.

## License

Content and branding belong to Veloria Healthcare Group. Original template assets (if retained) were from the Life Care HTML template.
