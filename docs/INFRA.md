# Infrastructure

## What This Repo Contains
- Static frontend only.
- No Docker, no CI/CD pipeline, no IaC, no hosting config files are present in this repo.

## Backend Hosting (Implied by Config)
- `config.js` points to a Render-hosted backend:
  - `https://e-touring-vdye.onrender.com`
- Local development backend is documented in `config.js`:
  - `http://localhost:5000`

## Frontend Hosting (Not Defined Here)
- Any static hosting works (examples):
  - Render Static Site
  - Netlify
  - Vercel (static)
  - GitHub Pages
  - S3 + CloudFront
- Requirement: the hosted frontend must be able to reach the backend API and the backend must allow CORS for the frontend origin.
