# Tech Stack

## Frontend
- Static HTML pages (no framework/build step)
- CSS: custom `css/style.css` (CSS variables, responsive media queries)
- JavaScript: vanilla browser JS in `js/script.js` and page-inline scripts
- Browser APIs used: Fetch API, localStorage, IntersectionObserver

## Third-Party (CDN)
- AOS (Animate On Scroll): `https://unpkg.com/aos@2.3.1/dist/aos.js` and `.../aos.css`
- Font Awesome 6.5.0: `https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css`
- Google Fonts: Poppins

## Backend Dependency
- The frontend is configured to call a separate backend API via `window.API_BASE_URL`.
- Current deployed backend base URL (Render): `https://e-touring-vdye.onrender.com` (see `config.js`).
