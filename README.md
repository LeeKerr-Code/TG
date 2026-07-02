# Turner & Goldrich — Website

Professional website for Turner & Goldrich Dental Laboratory, Est. 1973.

## Pages

| File | URL | Description |
|------|-----|-------------|
| `index.html` | `/` | Homepage |
| `about.html` | `/about` | Laboratory history & team |
| `aesthetics.html` | `/aesthetics` | Aesthetic dentistry philosophy |
| `gallery.html` | `/gallery` | Case study photo slideshow |
| `services.html` | `/services` | PFM, IPS e.max & Zirconia technical guidelines |
| `specials.html` | `/specials` | Monthly special offers |
| `downloads.html` | `/downloads` | Lab sheet downloads |
| `contact.html` | `/contact` | Contact details & enquiry form |
| `tg-admin.html` | `/admin` | Content management interface |

## Deployment

This site is deployed via [Vercel](https://vercel.com) directly from this GitHub repository.

### First-time setup

1. Push this repository to GitHub
2. Go to [vercel.com](https://vercel.com) and sign in
3. Click **Add New → Project**
4. Import this GitHub repository
5. Leave all settings as default — Vercel will detect the `vercel.json` config automatically
6. Click **Deploy**

Your site will be live at `https://your-project-name.vercel.app` within ~60 seconds.

### Custom domain

1. In the Vercel dashboard, go to your project → **Settings → Domains**
2. Add your domain (e.g. `turnergoldrich.com`)
3. Follow the DNS instructions shown — typically add an `A` record and a `CNAME` record at your domain registrar

### Updating content

**Option A — Content Manager (recommended for non-technical users)**
1. Open `/admin` on the live site or open `tg-admin.html` locally
2. Edit any text field and click Save
3. Use the AI Writing Assistant for copy suggestions
4. Click **Export HTML Files** to download the updated content JSON
5. Pass the export to a developer to apply changes to the HTML files

**Option B — Edit HTML files directly**
1. Open the relevant `.html` file in any text editor
2. Find the text you want to change and update it
3. Save the file
4. Commit and push to GitHub — Vercel deploys automatically within ~30 seconds

**Important — large files:** `gallery.html` is large (~7MB) because all 55 case photos are embedded directly in the file as base64 data. When updating it on GitHub, use **"Add file → Upload files"** to replace it (drag the file in), not the inline pencil/edit button, since GitHub's text editor isn't built for files this large.

## Structure

```
tg-site/
├── index.html              # Homepage
├── about.html               # About page
├── aesthetics.html          # Aesthetics page
├── gallery.html              # Gallery page (55 embedded case photos)
├── services.html            # Services page (technical content)
├── specials.html            # Specials page
├── downloads.html           # Downloads page
├── contact.html              # Contact page
├── tg-admin.html              # CMS admin interface
├── hero-smile.jpg           # Homepage hero photo
├── about-photo.jpg          # About section photo
├── gallery-images/          # Source case photos (not referenced live — gallery.html uses embedded copies)
├── vercel.json               # Vercel routing & headers config
├── .gitignore                 # Git ignore rules
└── README.md                  # This file
```

## Forms

Both the homepage consultation form and the dedicated Contact page form submit to **hello@turnergoldrich.co.uk** via [FormSubmit.co](https://formsubmit.co), a free email-forwarding service for static sites (no backend required).

**One-time step:** the first time anyone submits either form, FormSubmit sends a confirmation email to hello@turnergoldrich.co.uk — click the link in that email once to verify ownership. After that, every submission goes through automatically, and the person submitting sees an on-page "Message Sent" confirmation popup rather than being redirected away.

## Notes

- All pages are self-contained HTML files with no external dependencies except Google Fonts
- The site uses clean URLs via `vercel.json` — `/about` instead of `/about.html`
- All fonts load from Google Fonts CDN
- No build step required — pure HTML/CSS/JS

## Contact

Turner & Goldrich Ltd  
Elite House Office 1, Unit 8 The Courtyard  
100 Villiers Road, London NW2 5PJ  
t: +44 (0)20 7625 4591  
e: hello@turnergoldrich.co.uk
