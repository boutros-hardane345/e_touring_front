# Deploy

## Frontend Deploy
- Deploy the repo as a static site (no build step).
- Ensure the deployed output includes:
  - `*.html`
  - `css/style.css`
  - `js/script.js`
  - `config.js`
  - `images/*`

## Set Backend Endpoint
- Set `API_BASE_URL` in `config.js` to your deployed backend URL.

## Backend Requirements
- Backend must support:
  - `GET /api/events`, `GET /api/plans`, `GET/POST /api/feedback`
- Backend must allow CORS from the frontend domain.
