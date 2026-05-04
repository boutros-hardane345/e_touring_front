# Architecture

## High-Level
- This repo is the static frontend for the e_Touring site.
- Pages load shared assets:
  - `css/style.css`
  - `config.js` (sets `window.API_BASE_URL`)
  - `js/script.js` (shared UI + form helpers)
- Pages also include inline scripts for page-specific data fetching/rendering.

## Components (Conceptual)
- Static frontend (this repo)
- Backend REST API (separate service)
- Static assets: `images/*`
- External CDNs: AOS, Font Awesome, Google Fonts

## Data Flows
- Home `index.html`:
  - `GET ${API_BASE_URL}/api/events` (renders 3 cards)
  - `GET ${API_BASE_URL}/api/feedback` (renders 3 testimonials)
- Events `events_page.html`:
  - `GET ${API_BASE_URL}/api/events` (renders all)
- Plans `plans_pages.html`:
  - `GET ${API_BASE_URL}/api/plans` (renders all, with client-side category filter)
- Contact/Feedback `contact_us_page.html`:
  - `GET ${API_BASE_URL}/api/feedback` (renders testimonials)
  - `POST ${API_BASE_URL}/api/feedback` (submits new feedback)
- Shared `js/script.js` (conditionally active if matching elements exist):
  - `POST ${API_BASE_URL}/api/volunteer` (fallback to localStorage on failure)
  - `POST ${API_BASE_URL}/api/contact` (fallback to localStorage on failure)

## Environment Configuration
- Backend base URL is centralized in `config.js`.
