# Shakti Construction - Static Website

A high-performance, mobile-responsive, SEO-optimized static website for **Shakti Construction - Ahmedabad**, ready for deployment to **GitHub Pages**, **Cloudflare Pages**, or any static hosting provider.

Converted from static PHP into clean, folder-based static HTML with modular architecture and centralized assets.

---

## Site Structure & Directory Routes

All routes follow the clean folder structure (`sitename/<category>/`):

| Route | Source Directory & File | Description |
| :--- | :--- | :--- |
| `/` | `index.html` | Homepage & brand overview with revolution slider |
| `/about/` | `about/index.html` | Company history, vision, leadership & team |
| `/services/` | `services/index.html` | Comprehensive civil, residential & commercial services |
| `/contact/` | `contact/index.html` | Office address, phone, email & map location |
| `/projects/` | `projects/index.html` | Portfolio overview showcasing all project sectors |
| `/projects/residential/` | `projects/residential/index.html` | Residential architectural projects showcase |
| `/projects/commercial/` | `projects/commercial/index.html` | Commercial towers, offices & corporate spaces |
| `/projects/government/` | `projects/government/index.html` | Government & AUDA infrastructure developments |
| `/projects/pharmaceutical/` | `projects/pharmaceutical/index.html` | Cleanroom & pharmaceutical turnkey facilities |
| `/projects/institutional/` | `projects/institutional/index.html` | Institutional & educational civil projects |
| `/projects/customized-bungalows/` | `projects/customized-bungalows/index.html` | Bespoke residential villas & bungalows |
| `/projects/interior/` | `projects/interior/index.html` | Interior architecture & spatial design |
| `/civil-work/` | `civil-work/index.html` | Civil construction engineering solutions |
| `/redevelopments/` | `redevelopments/index.html` | Urban redevelopment & revitalization projects |
| `/career/` | `career/index.html` | Careers & employment opportunities |
| `/terms/` | `terms/index.html` | Terms & Conditions |
| `/privacy-policy/` | `privacy-policy/index.html` | Privacy & data protection policy |
| `/projects/auda-bopal/` | `projects/auda-bopal/index.html` | AUDA Bopal Affordable Housing Project detail |
| `/projects/haridwar-avenue/` | `projects/haridwar-avenue/index.html` | Haridwar Avenue Project detail |
| `/projects/hitesh-shah-bungalows/` | `projects/hitesh-shah-bungalows/index.html` | Hitesh Shah Bungalow Project detail |
| `/projects/santoor-farm/` | `projects/santoor-farm/index.html` | Santoor Farm Project detail |
| `/projects/sarva-shakti/` | `projects/sarva-shakti/index.html` | Sarva Shakti Project detail |
| `/projects/satva-shakti/` | `projects/satva-shakti/index.html` | Satva Shakti Project detail |
| `/projects/shakti-enclave/` | `projects/shakti-enclave/index.html` | Shakti Enclave Project detail |
| `/projects/shakti-icon/` | `projects/shakti-icon/index.html` | Shakti Icon Commercial Project detail |
| `/projects/shashwat-bungalows/` | `projects/shashwat-bungalows/index.html` | Shashwat Bungalows Project detail |
| `/projects/shreeji-heights/` | `projects/shreeji-heights/index.html` | Shreeji Heights Project detail |

---

## Modular Sections (`modular/`)

Reusable site components are cleanly separated in `modular/`:

- `modular/header.php` / `header.html`: Top navbar with branding, mobile toggle, phone & social links.
- `modular/menu.php` / `menu.html`: Slide-out overlay navigation menu matching the category structure.
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

All static resources reside in `assets/`:

```
assets/
├── css/          # Core stylesheets, plugins, bootstrap & themes
├── fonts/        # Web fonts (FontAwesome, Ionicons, Linearicons, Revicons)
├── images/       # Theme graphics, logos, icons, client photos, partners
├── js/           # jQuery, plugins, revolution slider, main scripts
└── projects/     # Architectural portfolio imagery and project galleries
```

All references across all depths use portable relative paths (`../assets/...`, `../../assets/...`), ensuring 100% portability on any host.

---

## PHP Source Backup & Static Regeneration

All original PHP source files are safely backed up in `_php_backup/` (ignored by Git for a clean static deployment).

If you make modifications to the PHP templates and want to regenerate all folder-based static HTML pages:

```bash
cd _php_backup
php generate_static.php
```

---

## Hosting & Deployment

### GitHub Pages
1. Push this repository to GitHub.
2. Go to **Settings** > **Pages**.
3. Under **Build and deployment**:
   - Source: **Deploy from a branch**
   - Branch: **main** / folder: **/ (root)**
4. Save. GitHub Pages will serve all clean folders directly (e.g., `sitename/about/`, `sitename/projects/residential/`).

### Cloudflare Pages
- **Framework preset**: None
- **Build command**: *(leave blank)*
- **Build output directory**: `/` *(root)*
- **Security Headers**: Managed automatically via `_headers`
- **Redirects & Clean URLs**: Managed automatically via `_redirects`
