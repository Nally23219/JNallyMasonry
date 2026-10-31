# J. Nally & Company: jnallymasonry.com

Website for J. Nally & Company: preservation masonry and lighthouse restoration by
Martin J. Nally, Manchester-by-the-Sea, MA.

## Structure
It's a static site with no framework and no build step.

- `index.html` is the whole site: markup, styles and script
- `images/dad.avif` is Marty's portrait
- `images/illustrative/` holds temporary placeholder photos (see the README there)
- `robots.txt` and `sitemap.xml` are for search engines

## Preview locally
```
python3 -m http.server 8000
```
Then open http://localhost:8000.

## Deploy
Hosted on Cloudflare Pages, connected to this GitHub repo.
- A push to `main` deploys to production (jnallymasonry.com).
- A push to any other branch creates a preview at `<branch>.<project>.pages.dev`.

## Forms
The estimate and job-application forms are configured at the top of the `<script>` in `index.html`:
- `FORM_ENDPOINT`: set this to a form-service URL (e.g. Formspree) and submissions get emailed directly.
- When it's empty, the forms open the visitor's email app addressed to `FORM_EMAIL`.
