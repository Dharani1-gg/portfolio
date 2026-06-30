# Dharani G — Portfolio

## Files
- `index.html` — the site
- `favicon.svg` — browser tab icon (swap with your own square SVG/PNG, same filename)
- `profile-placeholder.svg` — placeholder photo. Replace with your real photo, named
  `profile-placeholder.svg` (or update the `src` in the `<img id="profile-img">` tag
  in `index.html` if you use a different filename, e.g. `profile.jpg`)
- `.env.example` — documents the Clerk key needed for optional login
- `config.js` — the file the page actually reads at runtime; paste your real
  Clerk Publishable Key into `window.CLERK_PUBLISHABLE_KEY` here

## Swapping your photo
1. Export your photo as a square image.
2. Replace `profile-placeholder.svg` with it, **keeping the same filename**
   (or rename and update the `src="..."` in `index.html`).

## Optional login (Clerk)
The site works completely without this — the "Sign in" button stays hidden
until you configure a key.
1. Create a free application at https://dashboard.clerk.com
2. Copy the **Publishable Key**.
3. Open `config.js` and paste it:
   `window.CLERK_PUBLISHABLE_KEY = "pk_test_xxxxx";`
4. Reload the page — a "Sign in" button will appear in the nav bar.

`.env.example` exists for reference/documentation if you later add a build
step or backend; plain static HTML can't read `.env` files in the browser,
so `config.js` is what actually wires the key in.
