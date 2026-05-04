# Patterns Used

## Project Shape
- Flat multi-page site with shared global CSS/JS.
- Page-specific behavior is often implemented as inline `<script>` in the HTML file.

## Shared Runtime Config
- `config.js` sets `window.API_BASE_URL`.
- Pages expect `config.js` to be loaded before scripts that call the API.

## Rendering Pattern
- Data fetched with `fetch()` then rendered via template strings and `element.innerHTML`.
- Lists render by `array.map(...).join('')`.

## Escaping / Safety
- There is an `escapeHtml()` helper (duplicated in multiple places) used for some text fields.
- Because `innerHTML` is used, any unescaped dynamic fields can introduce XSS if backend data is not trusted.

## Progressive Enhancement
- Some behaviors are conditional based on presence of elements:
  - Forms: `#volunteerForm`, `#contactForm`
- Some UI effects run unconditionally (scroll listeners, mobile detection).

## Resilience
- For volunteer/contact submissions, `js/script.js` saves to localStorage if the network request fails.
- Keys used: `volunteers`, `contacts`, `bookings`.
