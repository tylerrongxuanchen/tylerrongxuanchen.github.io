# tyler-chen-website

Personal academic website for Tyler Rongxuan Chen, built with [Quarto](https://quarto.org).

## Local preview

```powershell
quarto preview          # live-reloading local server
quarto render           # one-off build into _site/
```

## First-time publish to GitHub Pages

1. Create an empty repo on GitHub named `tylerrongxuanchen.github.io` (user site → root URL).
2. From this folder:

   ```powershell
   git remote add origin https://github.com/tylerrongxuanchen/tylerrongxuanchen.github.io.git
   git push -u origin main
   quarto publish gh-pages
   ```

3. The site goes live at `https://tylerrongxuanchen.github.io/`.
   Subsequent updates: edit, commit, then `quarto publish gh-pages` again.

## Custom domain (recommended before the job market)

1. Buy a domain (Cloudflare Registrar or Porkbun, ~$10–12/yr).
2. In the repo: Settings → Pages → Custom domain → enter the domain; this creates a `CNAME` file
   on the `gh-pages` branch (add the same `CNAME` file under the project root and list it in
   `_quarto.yml` `resources:` so publishing does not remove it).
3. At the DNS provider: add a `CNAME` record pointing `www` (or the apex via ALIAS/ANAME) to
   `<username>.github.io`. Enable "Enforce HTTPS" in repo settings once DNS propagates.

## Before going live — TODO checklist

- [ ] Replace `assets/profile.png` (placeholder) with a real photo
- [ ] Replace `YOUR-USERNAME` GitHub links in `_quarto.yml` and `index.qmd`
- [ ] Add Google Scholar profile URL in `index.qmd` (create a Scholar profile if needed)
- [ ] Add article / replication / SSRN / Zenodo links in `research.qmd` and `data.qmd`
      (marked with `<!-- TODO -->` comments)
- [ ] Verify the publication years shown for the two Chinese-language articles
- [ ] Update `assets/Tyler_Rongxuan_Chen_CV.pdf` whenever the CV changes
- [ ] Add the site URL to the department profile and CV header
