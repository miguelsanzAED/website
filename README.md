# Nogara Energy — Website Source

This repository contains the full source of the [nogaraenergy.odoo.com](https://nogaraenergy.odoo.com) website: page templates (QWeb/HTML) and all media assets.

## Structure

```
pages/          QWeb HTML templates — one file per page
images/         All images and logos used across the site
```

## Pages

| File | URL | Description |
|------|-----|-------------|
| `index.html` | `/` | Homepage — hero, stats, services overview |
| `about-us.html` | `/about-us` | About Nogara Energy |
| `our-services.html` | `/our-services` | Services page |
| `grants-awards.html` | `/grants-awards` | Grants & Awards |
| `contactus.html` | `/contactus` | Contact form |
| `contactus-thank-you.html` | `/contactus-thank-you` | Post-contact confirmation |
| `blog_2.html` | `/blog/2` | R&D Services blog |
| `privacy.html` | `/privacy` | Privacy policy |
| `your-task-has-been-submitted.html` | `/your-task-has-been-submitted` | Task submission confirmation |

## Images

| File | Used in |
|------|---------|
| `nogara-logo.png` | Site header (all pages) |
| `nogara-pcb-lab.png` | Homepage hero |
| `nogara-solar-home.webp` | Homepage "What we do" section |
| `nogara-power-grid.webp` | Homepage / Services |
| `nogara-plc-panel.jpg` | Services page |
| `nogara-electronics-pcb.jpg` | Services page |
| `nogara-power-electronics.jpg` | Services page |
| `nogara-team.png` | About Us |
| `nogara-plc-hardware.png` | About Us / Services |
| `nogara-diagram.webp` | Technical diagram |
| `idea2024-event.jpg` | Grants & Awards |
| `idea2024-team.jpg` | Grants & Awards |
| `logo-iaf.jpg` | Grants & Awards — IAF logo |
| `logo-gobierno-aragon.png` | Grants & Awards — Gobierno de Aragón logo |

## How pages work

Pages are **QWeb templates** — Odoo's templating format. They extend `website.layout` and contain standard Bootstrap 5 HTML inside a `<div id="wrap">` block.

To push a modified page back to the live Odoo site, use the tooling in the [nogara-energy Claude Code project](../nogara-energy/):

```bash
cd ~/proyectos/nogara-energy
python tools/push_page.py --url / --input ../website/pages/index.html
```

## Tech stack

- **CMS:** Odoo 17 Website module
- **CSS framework:** Bootstrap 5
- **Templating:** QWeb (Odoo)
- **Hosting:** Odoo SaaS — nogaraenergy.odoo.com
