# Pradyot Jain — Business Analytics Portfolio

Source for my personal site. Static HTML, CSS and vanilla JavaScript, deployed on Netlify.

**Live:** https://pradyot-jain-cv.netlify.app

Project write-ups, notebooks and data files live in a separate repo:
https://github.com/pradyot0921/Portfolio

## Running locally

No build step and no dependencies. Serve the folder over HTTP rather than opening
`index.html` from the filesystem, or the absolute `/assets/...` paths will not resolve:

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

## Structure

```
index.html          Home
resume.html         Experience and education
portfolio.html      Projects (cards static, detail bullets in the PROJECTS array)
skills.html         Tools and certifications
contact.html        Contact details and Netlify form
assets/css/         base.css (shared) + one stylesheet per page
assets/profile/     Portrait, WebP with JPEG fallback
assets/logos/       Employer and university logos
assets/certificates/ Employment and course certificates
assets/resumes/     Resume in PDF and DOCX
_headers            Security headers and cache policy
_redirects          .html to clean-URL canonicalisation
```

Editing content: project detail bullets are in the `PROJECTS` array near the bottom of
`portfolio.html`. Roles and qualifications are in the corresponding array in `resume.html`.
The card titles and descriptions are static HTML in the same files, so a change to a
project title needs updating in both places.

## Licensing

Code is MIT, see `LICENSE`.
Content is not, see `CONTENT-LICENSE.md`.
