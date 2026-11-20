# Shakti Construction - Static Website

A high-performance, mobile-responsive, SEO-optimized static website for **Shakti Construction - Ahmedabad**, ready for deployment to **GitHub Pages**, **Cloudflare Pages**, or any static hosting provider.

Converted from static PHP into clean static HTML with modular architecture and centralized assets.

---

## Site Structure & Routes

| Route | File | Description |
| :--- | :--- | :--- |
| `/` | `index.html` | Homepage & brand overview with revolution slider |
| `/about.html` | `about.html` | Company history, vision, leadership & team |
| `/services.html` | `services.html` | Comprehensive civil, residential & commercial services |
| `/residential.html` | `residential.html` | Residential architectural projects showcase |
| `/commercial.html` | `commercial.html` | Commercial towers, offices & corporate spaces |
| `/government.html` | `government.html` | Government & AUDA infrastructure developments |
| `/pharmaceutical-projects.html` | `pharmaceutical-projects.html` | Cleanroom & pharmaceutical turnkey facilities |
| `/institutional-projects.html` | `institutional-projects.html` | Institutional & educational civil projects |
| `/customized-bungalows.html` | `customized-bungalows.html` | Bespoke residential villas & bungalows |
| `/interior-design.html` | `interior-design.html` | Interior architecture & spatial design |
| `/civil-work.html` | `civil-work.html` | Civil construction engineering solutions |
| `/redevelopments.html` | `redevelopments.html` | Urban redevelopment & revitalization projects |
| `/contact.html` | `contact.html` | Office address, phone, email & map location |
| `/career.html` | `career.html` | Careers & employment opportunities |
| `/terms.html` | `terms.html` | Terms & Conditions |
| `/privacy-policy.html` | `privacy-policy.html` | Privacy & data protection policy |
| `/auda-bopal.html` | `auda-bopal.html` | AUDA Bopal Affordable Housing Project detail |
| `/haridwar-avenue.html` | `haridwar-avenue.html` | Haridwar Avenue Project detail |
| `/hitesh-shah-bungalows.html` | `hitesh-shah-bungalows.html` | Hitesh Shah Bungalow Project detail |
| `/santoor-farm.html` | `santoor-farm.html` | Santoor Farm Project detail |
| `/sarva-shakti.html` | `sarva-shakti.html` | Sarva Shakti Project detail |
| `/satva-shakti.html` | `satva-shakti.html` | Satva Shakti Project detail |
| `/shakti-enclave.html` | `shakti-enclave.html` | Shakti Enclave Project detail |
| `/shakti-icon.html` | `shakti-icon.html` | Shakti Icon Commercial Project detail |
| `/shashwat-bungalows.html` | `shashwat-bungalows.html` | Shashwat Bungalows Project detail |
| `/shreeji-heights.html` | `shreeji-heights.html` | Shreeji Heights Project detail |

---

## Modular Sections (`modular/`)

To make maintenance and future updates simple, reusable site components have been separated into modular sections:

- `modular/header.php` / `header.html`: Top navbar with branding, mobile toggle, phone & social links.
- `modular/menu.php` / `menu.html`: Slide-out overlay navigation menu.
- `modular/navbar.php` / `navbar.html`: Combined menu and header component.
- `modular/footer.php` / `footer.html`: Global site footer with links and company info.
- `modular/projects-thumb.php` / `projects-thumb.html`: "Other Projects" thumbnail carousel.
- `modular/latest-projects.php` / `latest-projects.html`: Homepage filterable project category carousel.
- `modular/news.php` / `news.html`: Latest news section carousel.
- `modular/testimonial.php` / `testimonial.html`: Client reviews and partner logos carousel.
- `modular/head.php` / `head.html`: Reusable HTML head metadata and style links.
- `modular/scripts.php` / `scripts.html`: Reusable JavaScript bundle scripts.

---

## Assets Organization (`assets/`)

All static resources have been moved into the consolidated `assets/` folder:

```
assets/
├── css/          # Core stylesheets, plugins, bootstrap & themes
├── fonts/        # Web fonts (FontAwesome, Ionicons, Linearicons, Revicons)
├── images/       # Theme graphics, logos, icons, client photos, partners
├── js/           # jQuery, plugins, revolution slider, main scripts
└── projects/     # Architectural portfolio imagery and project galleries
```

All references across HTML, CSS, and JS files have been updated to use relative paths (`assets/...`), ensuring 100% portability.

---

## PHP Source Backup & Static Regeneration

All original PHP source files are safely backed up in `_php_backup/` (ignored by Git for a clean static deployment).

If you make modifications to the PHP templates and want to regenerate all static HTML pages:

```bash
cd _php_backup
php generate_static.php
```

This will automatically render all pages with output buffering, resolve paths, clean characters, and write updated static HTML pages to the root directory.

---

## Hosting & Deployment

### GitHub Pages
1. Push this repository to GitHub.
2. In your GitHub repository, go to **Settings** > **Pages**.
3. Under **Build and deployment**:
   - Source: **Deploy from a branch**
   - Branch: **main** / folder: **/ (root)**
4. Save. GitHub Pages will serve your site directly.

### Cloudflare Pages
- **Framework preset**: None
- **Build command**: *(leave blank)*
- **Build output directory**: `/` *(root)*
- **Security Headers**: Managed automatically via `_headers`
- **Redirects & Clean URLs**: Managed automatically via `_redirects`
