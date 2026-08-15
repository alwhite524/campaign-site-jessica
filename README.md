# Jessica Voigt for Beaumont Mayor — campaign site

Static HTML/CSS site, same template pattern as the Lloyd White campaign site
(`campaign-site-lloyd`). No build step — just plain files.

- `index.html` — home page (bio, priorities, track record)
- `donate.html` — donation page
- `volunteer.html` — volunteer sign-up + yard sign request forms
- `style.css` — shared stylesheet (navy/teal/ivory palette, distinct from
  Lloyd's UCLA-blue theme)
- `apps-script/` — Google Apps Script backend for the volunteer/yard-sign
  forms; see `apps-script/SETUP.md`
- `CNAME` — GitHub Pages custom domain file, set to `JessicaVoigtForBeaumont.com`

## TODO before this goes live

- [x] **Photo** — `jessica-voigt.jpg` is in place.
- [ ] **Donate link** — `donate.html` has a placeholder button
      (`#PASTE-DONATE-LINK-HERE`). Swap in the real Anedot/ActBlue/WinRed
      contribution URL.
- [ ] **Volunteer form backend** — follow `apps-script/SETUP.md` to wire up
      the Google Sheet + email notifications, then paste the deployed script
      URL into `volunteer.html`.
- [ ] **Disclaimer text** — the footer currently reads "Paid for by Jessica
      Voigt for Beaumont Mayor 2026." Confirm this matches the exact
      disclaimer text required for her official campaign committee (FPPC
      filings usually specify exact required wording).
- [ ] **Endorsements** — Lloyd's site lists Jessica as an endorser; this site
      doesn't have an endorsements section yet since we don't have names to
      list. Add one later if useful.
- [ ] **Social links / contact email** — not included yet; add to the footer
      or nav once available.
- [x] **GitHub repo** — pushed to
      [github.com/alwhite524/campaign-site-jessica](https://github.com/alwhite524/campaign-site-jessica).
- [x] **GitHub Pages + DNS** — Pages is enabled (deploying from `main`), and
      Cloudflare has 4 A records for `@` pointing at GitHub Pages
      (185.199.108/109/110/111.153, all DNS-only/unproxied). Site is live at
      http://jessicavoigtforbeaumont.com/.
- [ ] **HTTPS enforcement** — GitHub is still issuing the TLS certificate for
      the custom domain (can take anywhere from a few minutes to ~24h after
      DNS propagates). Once available, check "Enforce HTTPS" in
      [repo Pages settings](https://github.com/alwhite524/campaign-site-jessica/settings/pages)
      so the site redirects to `https://`.

## Local preview

From this folder:

```bash
python -m http.server 8935
```

Then open `http://localhost:8935`.
