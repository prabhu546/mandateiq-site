# MandateIQ website

Single-page landing site for MandateIQ, hosted on GitHub Pages. No build step: one `index.html`.

## Publish on GitHub Pages

1. Create a new public repository on GitHub, for example `mandateiq-site`.
2. Upload `index.html` and this `README.md` to the repository root (Add file → Upload files → Commit).
3. Go to **Settings → Pages**. Under *Build and deployment*, set Source to **Deploy from a branch**, branch **main**, folder **/ (root)**, then Save.
4. After a minute the site is live at `https://<your-username>.github.io/mandateiq-site/`.

## Turn on the pilot form

GitHub Pages has no backend, so the form posts to Formspree (free tier is enough to start).

1. Sign up at formspree.io and create a form.
2. Copy the form ID (the part after `/f/` in the endpoint).
3. In `index.html`, replace `YOUR_FORM_ID` in the form's `action` with your ID and commit.

Submissions then arrive in your email and the Formspree dashboard.

## Custom domain (optional)

1. Buy a domain (e.g. `mandateiq.in`).
2. In **Settings → Pages → Custom domain**, enter it and save. GitHub creates a `CNAME` file.
3. At your domain registrar, add DNS records:
   - Apex domain: four `A` records pointing to `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - `www`: a `CNAME` record pointing to `<your-username>.github.io`
4. Tick **Enforce HTTPS** once the certificate is issued.

## Things to edit before launch

- Contact email in the footer (`hello@mandateiq.in`).
- Pilot form ID (see above).
- The UPI e-mandate volume figure in the problem section, if newer NPCI data is out.
