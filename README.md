# iron-code-site

Standalone, publish-ready download/landing website for the Iron Code
desktop app. Static — one `index.html`, no build step, no app source.

GitHub account: **ironcodepeps**

## ⚠️ Fill placeholders BEFORE publishing

Open `index.html`, search for `TBD__`, and replace:

| Placeholder | Replace with | Status |
|---|---|---|
| ~~`TBD__FREE_DOWNLOAD_URL`~~ | GitHub Releases "latest" URL — **done** (points to `iron-code-releases`) | ✅ |
| ~~`TBD__VERSION`~~ | `1.0.0` — **done** | ✅ |
| `TBD__BUY_URL` | Paid checkout link (Lemon Squeezy / Gumroad / Stripe) | ⏳ pending payment decision |
| `price TBD__` (in the Pro tier) | Your chosen price, or remove | ⏳ pending |

The free download URL works as soon as you publish the first GitHub
Release (see `RELEASES.md`). It is version-less on purpose, so it keeps
working for every future release with no site edit.

The Free vs Pro feature lists are the recommended default split
(Free = reference, Pro = tools). Edit the two `<ul>` lists in the
`#pricing` section if you change the split.

## Publish steps (after placeholders are filled)

### 1. Create an empty public repo
On GitHub (signed in as **ironcodepeps**): **New repository**
- Name: `iron-code-site`
- Visibility: **Public**
- Do **not** add README / .gitignore / license
- Create repository

### 2. Push (from inside this folder)

```
cd "C:\Users\KyleBeck\PeptideApp-Desktop\website"
git init
git config user.name  "Kyle Beck"
git config user.email "IronCodepeps@gmail.com"
git add .
git commit -m "Add Iron Code download site"
git branch -M main
git remote add origin https://github.com/ironcodepeps/iron-code-site.git
git push -u origin main
```

(Username `ironcodepeps`; password = a `ghp_…` Personal Access Token,
same as the privacy repo.)

### 3. Enable GitHub Pages
Repo **Settings → Pages** → Source: **Deploy from a branch** →
Branch `main`, folder `/ (root)` → **Save**. Wait ~1–2 min.

### 4. Your site URL

```
https://ironcodepeps.github.io/iron-code-site/
```

(A custom domain can be added later in Settings → Pages → Custom
domain if you buy one.)

## Updating later

Edit `index.html`, then:

```
git add index.html
git commit -m "Update site"
git push
```

Pages redeploys automatically within ~1–2 minutes.
