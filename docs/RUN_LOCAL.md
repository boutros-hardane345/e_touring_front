# Run Locally

## Frontend
- This is a static site. Serve the folder with any static file server.
- If you open files directly from disk, some browsers may restrict `fetch()` or behave differently than on HTTP.

## Backend URL
- Edit `config.js` to point to your backend.
- For local backend, use the documented option:
  - `http://localhost:5000`

## What To Verify
- Pages load:
  - `index.html`, `about.html`, `events_page.html`, `plans_pages.html`, `contact_us_page.html`
- API calls succeed:
  - Events, plans, feedback
