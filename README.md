# Ethiopia Urban Advisory and Building Group

Corporate landing page for **Ethiopia Urban Advisory and Building Group**, the Addis Ababa consultancy led by Heinock Balemual Adane. The site presents the practice's work on land entitlements, urban planning, municipal permitting, and architectural building delivery across Ethiopia in a single, responsive page.

**Live focus:** Land entitlements · Urban planning · Architectural design and CAD · GIS spatial analysis · Construction oversight

**Location:** Bole Sub-City, Addis Ababa, Ethiopia

## Project overview

This repository contains the complete public website for Ethiopia Urban Advisory and Building Group. It is built as one self-contained `index.html` file with no build step, no backend, and no database, so it can be hosted on any static hosting service and reviewed locally in a browser.

The page is written for private developers, institutional investors, public agencies, and remote clients who need a clear view of the consultancy's services before making an inquiry. It explains what the practice does, how an entitlement moves from a parcel audit to a building permit, which past projects illustrate that work, and how to request a consultation.

Principal consultant: Heinock Balemual Adane — specialist in urban land administration and management, architectural and landscape design, and GIS spatial analysis, with 15+ years of design and regulatory experience stated on the site. His working tools named on the site are AutoCAD, ArchiCAD, and QGIS.

## Tech stack

| Layer | Technology | Notes |
| --- | --- | --- |
| Markup | HTML5 | Semantic sections with in-page anchor navigation |
| Styling | Tailwind CSS via CDN | Configured inline in `index.html`; no compiled CSS file |
| Typography | Playfair Display and Inter | Loaded from Google Fonts |
| Icons | Font Awesome 6.5.1 | Loaded from CDN |
| Behaviour | Vanilla JavaScript | No framework; all scripts are at the end of `index.html` |
| Images | Unsplash, with placeholder fallback | No local image files in the current build |
| Hosting | Any static host | GitHub Pages, Netlify, Vercel, or a web server |

### Design system

- **Slate charcoal** `#16202A` — header, hero, and dark panels
- **Deep slate** `#0F171F` — top utility bar and footer
- **Sandstone** `#F7F6F2` — page background
- **Sand dark** `#ECEAE2` — subtle section contrast
- **Architectural gold** `#B38B59` — accents, labels, and calls to action
- **Gold light** `#C9A576` — hover and secondary accents
- **Headings:** Playfair Display, serif
- **Body text:** Inter, sans-serif
- **Texture:** A faint architectural blueprint grid is used on the hero, dark workflow panel, and quote banner

## Features

- Sticky navigation with a mobile menu, covering Expertise, Public Hearings, Past Projects, Community Stewardship, About Us, and Contact Us

- Hero section with the practice headline, an introduction to permitting, planning, design, and GIS work in Ethiopia, and calls to action to explore past projects or schedule a consultation

- A four-part focus strip in the hero covering land entitlements, urban planning, design and CAD, and project delivery

- Client and project portal Login modal, as included in the approved template — it explains that portal access is provisioned for active project sponsors

- Project consultation form with fields for name, email, advisory service, project location or sub-city, and project scope, with an on-page confirmation message after submission in the browser

- Privacy Policy and Terms & Conditions modals linked from the footer

- Fully responsive layout for phone, tablet, and desktop, with smooth scrolling to each section

## Page sections

### Expertise

Six capability cards covering the development lifecycle:

1. Land Development Entitlements & Permitting
2. Urban Planning & Master Plans
3. Environmental & Social Impact Assessment
4. Architectural & Landscape Design
5. Construction Management & On-Time Delivery
6. Feasibility, Due Diligence & Land Valuation

### Public Hearings & Regulatory Navigation

An explanation of representation through sub-city technical committees, municipal planning boards, and neighbourhood consultations, paired with a four-step Entitlement & Approval Workflow:

1. Cadastral & Zoning Diagnostic
2. Technical Dossier & ESIA Preparation
3. Public Consultation & Board Hearing
4. Permit Issuance & Site Mobilization

### Past Projects

A filterable portfolio with category tabs and a case-study modal for each project. Selecting a project opens its location, summary, and key deliverables.

| Project | Location | Category |
| --- | --- | --- |
| Bole Residential & Mixed-Use Development | Bole Sub-City, Addis Ababa | Project Management |
| Entoto & Municipal Public Park Master Plan | Gulele Sub-City, Addis Ababa | Building & Landscape |
| Mekele Youth & Community Center | Mekele, Tigray | Building & Landscape |
| CMC / Ayat Residential Villa & Estate | Yeka Sub-City, Addis Ababa | Building & Landscape |
| Kirkos Urban Redevelopment Corridor | Kirkos Sub-City, Addis Ababa | Acquisition & Due Diligence |
| Rift Valley Eco-Lodge & Hospitality Site | Oromia Region, Ethiopia | Entitlement |

Filter categories: All Projects, Entitlement, Project Management, Acquisition & Due Diligence, and Building & Landscape.

### Community Stewardship, About Us, and Contact

Community Stewardship covers urban green and park integration and participatory neighbourhood planning. About Us summarises the practice, its 15+ years of experience, its full-lifecycle scope from entitlement to construction, and its CAD and GIS tools, alongside three advisory standards: regulatory precision, spatial and technical rigour, and transparent client advocacy. The page closes with a quote banner and a Contact Us section with the consultation form.

## Repository structure

```text
ethiopia-urban-advisory/
├── index.html    # The entire website: markup, Tailwind config, styles, and scripts
├── README.md     # This file
└── assets/       # Optional. Empty in the current build — photos, fonts, and icons load from external services
```

There is no `package.json`, build script, or environment file. Editing `index.html` edits the live site.

## Local preview instructions

No installation is required. An internet connection is needed for the Tailwind CDN, Google Fonts, Font Awesome, and Unsplash images to load as designed.

### Option 1 — Open the file directly

Download or clone the repository, then open `index.html` in a browser.

### Option 2 — Serve the folder locally (recommended)

Serving the folder avoids browser restrictions that can affect a file opened directly.

With Python 3, from the repository folder:

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000 in a browser. Stop the server with `Ctrl+C`.

With Node.js:

```bash
npx serve .
```

Then open the local address the command prints.

### Option 3 — VS Code Live Server

Open the repository folder in VS Code, install the Live Server extension, right-click `index.html`, and choose **Open with Live Server**.

### Checking the preview

- Resize the browser or use device emulation to check the mobile menu and the project grid at phone width.
- Use the portfolio filter tabs and open each **View Details** modal.
- Submit the consultation form with test details to see the on-page confirmation.
- Open the Login, Privacy Policy, and Terms & Conditions modals from the header and footer.

## Editing content

All content lives in `index.html`.

- **Text and sections:** Edit the HTML directly in the section you want to change. Section comments in the file mark the hero, expertise, public hearings, past projects, stewardship, about, quote, and contact blocks.

- **Projects:** Edit the `projectsData` array in the script at the end of the file. Each entry has an `id`, `title`, `location`, `category`, `image`, `tags`, `summary`, and `deliverables`. The grid and the case-study modal are generated from this array, so a new entry appears automatically. Use one of the existing category names if the project should appear under a filter tab.

- **Colours and fonts:** Edit the `tailwind.config` block in the document head. Colour names such as `slatecharcoal`, `sandstone`, and `archgold`, and the `serif` and `sans` font families, are defined there.

- **Contact details:** The current Get In Touch details are Bole Sub-City, Addis Ababa, Ethiopia, 1000, etuabg@gmail.com, +251 91 178 0344, and +251 90 080 3030. The same details also appear in the top utility bar and the footer, so update all three places together.

- **Images:** Project and stewardship images are remote Unsplash URLs with an automatic placeholder fallback if an image fails to load. To use a local image instead, place it in `assets/` and reference it with a relative path such as `assets/project-name.jpg`.

> [!NOTE]
> The consultation form and the Login modal run in the browser only. The form shows a confirmation on the page and the login modal explains how portal access is provisioned; neither sends data to a server in this static build. Connect the form to an email or form service before relying on it to receive inquiries.

## Deployment

Because the site is a single static file, deployment is a file upload — there is nothing to compile.

### GitHub Pages

1. Create the repository and add `index.html` and this `README.md`, after review and approval.
2. In the repository, open **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, select the main branch and the root folder, and save.
4. GitHub Pages will publish the site and show its URL in the same settings panel.

Suggested first commit message:

```text
feat: initialize Ethiopia Urban Advisory and Building Group corporate landing page with interactive modals and filters
```

The same folder can also be dragged into Netlify or Vercel, or copied to any web server, with no configuration changes.

## Contact

**Ethiopia Urban Advisory and Building Group**
Bole Sub-City, Addis Ababa, Ethiopia, 1000

- Email: etuabg@gmail.com
- Phone: +251 91 178 0344 / +251 90 080 3030
- Principal Consultant: Heinock Balemual Adane

## Licence and content

Copyright © 2026 Ethiopia Urban Advisory and Building Group — Heinock Balemual Adane. All rights reserved.

Project summaries on the site are provided for informational purposes. Formal advisory engagements, permit representations, and design deliverables are governed by an executed Statement of Work.
