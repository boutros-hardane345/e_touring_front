# API Contract (Inferred)

This is inferred from frontend usage. Treat as documentation of assumptions.

## Base URL
- Provided by `window.API_BASE_URL` from `config.js`.

## Endpoints

### `GET /api/events`
- Used by: `index.html`, `events_page.html`
- Expected response: JSON array of event objects
- Fields used:
  - `title` (string)
  - `description` (string)
  - `date` (string)
  - `time` (string)
  - `location` (string)
  - `image` (string URL)
  - `badge` (string, optional)

### `GET /api/plans`
- Used by: `plans_pages.html`
- Expected response: JSON array of plan objects
- Fields used:
  - `name` (string)
  - `category` (string)
  - `location` (string)
  - `duration` (string)
  - `features` (array of strings)

### `GET /api/feedback`
- Used by: `index.html`, `contact_us_page.html`
- Expected response: JSON array of feedback objects
- Fields used:
  - `name` (string)
  - `message` (string)
  - `rating` (number 1-5)

### `POST /api/feedback`
- Used by: `contact_us_page.html`
- Request JSON:
  - `name` (string)
  - `email` (string)
  - `rating` (number)
  - `message` (string)
- Response handling:
  - If `res.ok`: frontend alerts success and reloads list.

### `POST /api/volunteer`
- Used by: `js/script.js` (only if a `#volunteerForm` exists on the page)
- Request JSON: key/value pairs from a form (exact fields depend on form markup)
- Fallback on network failure: saved to localStorage under key `volunteers`.

### `POST /api/contact`
- Used by: `js/script.js` (only if a `#contactForm` exists on the page)
- Request JSON: key/value pairs from a form (exact fields depend on form markup)
- Fallback on network failure: saved to localStorage under key `contacts`.

## Cross-Cutting Concerns
- CORS must allow the frontend origin.
- JSON is assumed for all API responses.
