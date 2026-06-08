# Wotsit Scoreboard

A live, projector-friendly score tracker. Each team is rendered as a large
transparent measuring cylinder that fills bottom-up with animated, individually
rendered orange "Wotsit" puffs as the team's score increases.

It's a single, self-contained `index.html` — no build step, no server, no
external requests. Open the file and it just works (state is saved to your
browser's `localStorage`).

## Run it locally

Just open the file in a browser:

```bash
open index.html        # macOS
# or simply double-click index.html in your file manager
```

That's it. There's nothing to install or build.

## Deploy to GitHub Pages

This repo is already set up to publish itself to GitHub Pages automatically via
GitHub Actions (see [`.github/workflows/deploy-pages.yml`](.github/workflows/deploy-pages.yml)).

One-time setup:

1. Push this repository to GitHub (it lives on `main`).
2. In your repo, go to **Settings → Pages**.
3. Under **Build and deployment → Source**, choose **GitHub Actions**.

After that, every push to `main` builds and deploys the site automatically. You
can also trigger a deploy manually from the **Actions** tab
(**Deploy to GitHub Pages → Run workflow**).

Once the first deployment finishes, your scoreboard will be live at:

```
https://<your-username>.github.io/<repository-name>/
```

For this repository that is:

```
https://tim-mccurrach.github.io/Wotsits-scoring/
```

### Prefer not to use Actions?

Because the whole app is a single `index.html` at the repo root, you can also
use the classic branch-based deploy instead:

1. **Settings → Pages → Source → Deploy from a branch**.
2. Pick the **`main`** branch and the **`/ (root)`** folder, then **Save**.

Both approaches serve the exact same `index.html`.

## Keyboard shortcuts

- `f` — toggle fullscreen
- `m` — open/close the team management panel
- `Esc` — close the team management panel
