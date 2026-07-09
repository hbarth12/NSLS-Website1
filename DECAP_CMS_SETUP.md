# Decap CMS Setup

The Publications page now reads from `content/publications.json`. Decap CMS edits that file through `/admin/`.

## Files added

- `admin/index.html` - loads Decap CMS.
- `admin/config.yml` - defines the Publications editor.
- `content/publications.json` - publication entries edited by Decap.
- `assets/uploads/` - uploaded publication images.

## Before deploying

Open `admin/config.yml` and replace:

```yml
repo: YOUR-GITHUB-USERNAME/YOUR-REPO-NAME
```

with your actual GitHub repo, for example:

```yml
repo: haddonbarth/nsls
```

## How it works

Go to `/admin/` on the deployed site. Add or reorder publications in the Publications list. The first visible featured entry becomes the large card on the Publications page. The category buttons filter by `type`:

- `analysis`
- `policy-paper`
- `institutional-note`

For uploaded images, Decap saves files into `assets/uploads/` and writes the path into `content/publications.json`.

## Authentication note

The GitHub backend also needs an OAuth flow/provider for Decap CMS to commit changes back to the repo. On Vercel, this is usually handled with a small OAuth provider service or a Decap-compatible auth integration. Once that is configured, `/admin/` can commit changes directly to GitHub.
