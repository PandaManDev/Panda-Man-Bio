# Panda Man Bio

A polished, responsive personal hub for **Panda Man** — built as a lightweight static website with vanilla HTML, CSS, and JavaScript.

The site is designed to work well on desktop and mobile without a build step or framework.

## Features

- Responsive dark, neon-lime visual design
- Multi-page personal site
- Shared navigation generated with JavaScript
- Mobile navigation drawer
- Active-page navigation state
- Animated loading screen
- Reduced-motion support
- Native Web Share support with clipboard fallback
- Contact form using the visitor's email client
- Custom Panda Man avatar and banner assets
- Open Graph metadata on the homepage
- Static-host friendly and ready for Vercel

## Project structure

```text
Panda-Man-Bio-main/
├── index.html
├── about.html
├── adventures.html
├── achievements.html
├── characters.html
├── collabs.html
├── community.html
├── contact.html
├── credits.html
├── events.html
├── faq.html
├── favorites.html
├── friends.html
├── gallery.html
├── games.html
├── guestbook.html
├── guides.html
├── journal.html
├── links.html
├── lore.html
├── media.html
├── memes.html
├── missions.html
├── music.html
├── now.html
├── playlist.html
├── projects.html
├── quests.html
├── roadmap.html
├── secrets.html
├── setup.html
├── shoutouts.html
├── start.html
├── support.html
├── toolbox.html
├── updates.html
├── videos.html
├── styles.css
├── script.js
├── panda.man420-avatar-1024.gif
├── panda.man420-banner-1024.gif
├── 404.html
├── robots.txt
├── vercel.json
└── README.md
```

## Run locally

No Node.js installation is required.

### Option 1 — Open directly

Open `index.html` in a browser.

### Option 2 — Use a local server

A local server is recommended because it behaves more like production hosting.

With Python:

```bash
python -m http.server 8080
```

Then open:

```text
http://localhost:8080
```

## Deploy to Vercel

### Using the Vercel dashboard

1. Create a new Vercel project.
2. Import this project/repository.
3. Keep the project as a static site.
4. Deploy.
5. No environment variables are required for the current static version.

### Using Vercel CLI

Install the CLI:

```bash
npm install -g vercel
```

From the project folder:

```bash
vercel
```

For production:

```bash
vercel --prod
```

## Custom domain

After deploying, a custom domain can be added from the Vercel project dashboard.

Because this project uses root-relative paths such as `/about.html`, it works best when deployed at the domain root.

## Editing the site

### Navigation

The complete navigation list is stored in `script.js`:

```js
const PAGE_LINKS = [
  ['Home', '/'],
  ['About', '/about.html'],
  // ...
];
```

Add, remove, or rename pages there.

### Profile image

The shared profile image is:

```text
panda.man420-avatar-1024.gif
```

The JavaScript loader also references:

```text
/panda.man420-avatar-1024.gif
```

### Banner

The main background/banner asset is:

```text
panda.man420-banner-1024.gif
```

### Theme

The primary visual variables are defined in the CSS:

```css
--ink
--muted
--line
--panel
--lime
--deep
```

The current theme uses a dark background with a lime accent.

## Contact form

The contact page currently uses a `mailto:` flow rather than a server-side form service.

Messages are prepared for:

```text
pandamanofficial420@gmail.com
```

This means the visitor's device must have an email client capable of handling `mailto:` links.

For reliable server-side submissions, replace the current handler with a service or backend endpoint.

## Accessibility improvements

The site includes several accessibility-focused behaviors:

- Semantic navigation labels
- `aria-current` for the active page
- Keyboard-friendly navigation
- Escape-to-close mobile navigation
- Visible focus states
- Descriptive image alt text
- Reduced-motion detection
- Accessible loading status
- Form labels

## Performance notes

The two animated GIF assets are the largest files in the project.

For faster loading, consider converting them to modern formats such as:

- WebP
- AVIF
- MP4/WebM for animated backgrounds

A modern image format can significantly reduce page weight while keeping the same visual effect.

## Browser support

The site is designed for modern browsers including:

- Chrome
- Edge
- Firefox
- Safari

The native Web Share API is used when available. Browsers without it fall back to copying the current URL.

## Troubleshooting

### Navigation links do not work

Make sure the site is deployed at the domain root and that the `.html` files are present.

### Images are missing

Check that the following files are in the project root:

```text
panda.man420-avatar-1024.gif
panda.man420-banner-1024.gif
```

### The share button only copies the link

That is expected in browsers that do not support the Web Share API.

### Contact does not send automatically

The contact page opens the visitor's configured email application. It does not send email directly from the server.

## Security

This is a static front-end project. It does not contain server credentials or API keys.

Do not place private API keys, database service-role keys, webhook secrets, or passwords inside HTML, CSS, or client-side JavaScript.

If backend functionality is added later, keep secrets in server-side environment variables.

## Deployment checklist

Before publishing:

- [ ] Test every navigation link
- [ ] Test mobile navigation
- [ ] Test the contact form
- [ ] Test the share button
- [ ] Confirm avatar/banner assets load
- [ ] Test keyboard navigation
- [ ] Test on mobile
- [ ] Confirm the 404 page works
- [ ] Deploy to Vercel
- [ ] Add a custom domain if desired
- [ ] Test the production URL

## License

This project is provided for personal use. Replace this section with your preferred license if you plan to distribute the source publicly.

---

**Panda Man Bio**  
Personal website • Creator hub • Roblox • Projects • Community
