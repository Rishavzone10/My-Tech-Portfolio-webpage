# Deploying this static portfolio to Vercel

Quick steps to get this site live on Vercel.

1) Commit & push your repository (if not already):

```powershell
git add .
git commit -m "Prepare site for Vercel"
git push origin main
```

2) Option A — Connect GitHub (recommended):
- Go to https://vercel.com and import your GitHub repository. Vercel will build and deploy automatically. No build step required for this static site.

3) Option B — Use Vercel CLI:

```powershell
npm i -g vercel
vercel login
vercel --prod
```

Notes:
- Root URL will serve `index.html` which redirects to `page.html`. If you'd rather have the page directly at `/`, rename `page.html` to `index.html` and remove the redirect file.
- `vercel.json` contains a small header and clean URL config — customize as needed for caching or rewrites.
