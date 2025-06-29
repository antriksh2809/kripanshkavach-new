# Kripansh Kavach – Personal Website

This repository contains the source code for **Kripansh Kavach's** personal portfolio website.  The site is built with plain **HTML, CSS and JavaScript** (no frontend framework) and can be served as static files or via a very small Node.js server that is included in the repo.

---

## 📂 Project structure

```
kripansh-kavach-site/
├── assets/               # CSS, JS and third-party libraries
│   ├── css/
│   └── js/
├── images/               # Optimised image assets used on the site
├── index.html            # Landing / Home page (light-weight)
├── final-website.html    # Full length single-page version of the site
├── direct-link.html      # Convenience page for a specific section/link
├── server.js             # Tiny Node static file server (no dependencies)
├── package.json          # NPM script (live-server)
├── netlify.toml          # Netlify deployment configuration
├── start-*.{bat,ps1,py}  # Helper scripts for different OSes
└── README.md             # You are here ✅
```

> Feel free to remove any files or scripts you do not need – they exist only for convenience.

---

## 🚀 Running the site locally

### Prerequisites

* [Node.js](https://nodejs.org) ≥ 14 (only needed if you wish to use the helper servers)
* Alternatively, **no tooling at all** – you can simply double-click any of the `.html` files and they will open in your browser.  However, running a local server avoids CORS issues and enables relative paths to work correctly.

### Option 1 – Live-reload dev server (recommended)

```bash
# install dependencies (only required once)
npm install

# start the server with live reload
npm start
```

`live-server` will open the site in your default browser and reload automatically whenever you save a file.

### Option 2 – Minimal Node static server

```bash
node server.js
```

Open `http://localhost:3000` in your browser.

### Option 3 – Python (already installed on many machines)

```bash
python -m http.server 3000
```

---

## 🌐 Deployment

The repository is pre-configured for **Netlify**.  Push the code to your Git provider (GitHub, GitLab, Bitbucket) and then:

1. Create a new site on Netlify and link it to the repository.
2. Set **Build Command** to `npm run build` (leave empty because the site is static).
3. Set **Publish Directory** to `/` (root of the repo).
4. Click **Deploy Site**.

`netlify.toml` can be adjusted if you need redirects or custom headers later.

You can, of course, host the site on **GitHub Pages**, **Vercel**, **Cloudflare Pages** or any S3-compatible bucket – it is just static content.

---

## ✍️ Editing content

All visual content lives in the HTML files and in the `assets/` folder:

* `assets/css/styles.css` – Global styles
* `assets/js/script.js`  – Behaviour / interactivity

Feel free to modify or remove anything to make the website your own.

---

## 🛂 License

This project is released under the MIT License – do whatever you like, just keep the license file.

---

## 🙌 Acknowledgements

* [live-server](https://github.com/tapio/live-server) – instant reload for static pages.
* Everyone whose open-source work made this project possible.
