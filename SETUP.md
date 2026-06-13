# Go-live checklist — `WillEnnis/WillEnnis`

Your GitHub **profile README**. It renders at the top of `github.com/WillEnnis` because the repo name equals your username. Total time: ~5–10 minutes.

---

## 0. (One time) capitalize your username
Settings → **Account** → **Change username** → `WillEnnis`.
> Casing is cosmetic to GitHub (`willenn24`-style uniqueness is case-insensitive), but `WillEnnis` reads better on a recruiter-facing page. Do this **before** step 1 so the repo name matches.

## 1. Create the repo
- New repo → name it **exactly** `WillEnnis` (must match your username).
- Visibility: **Public**.
- GitHub shows a special "You found a secret!" banner confirming it's your profile repo. ✅

## 2. Fill the 3 placeholder links
Open `README.md`, find-and-replace these tokens:

| Token | Replace with |
|---|---|
| `__LINKEDIN_URL__` | your LinkedIn profile URL |
| `__PORTFOLIO_URL__` | The Engineer's Desk live URL (once deployed) |
| `__RESUME_URL__` | a link to your résumé PDF (Drive share link or `/assets/resume.pdf`) |

> Don't have one yet? Either drop the badge for now, or point it at `#` and fill it later. Email is already wired (`willenn24@gmail.com`).

## 3. Push it
```bash
git init
git add .
git commit -m "Profile README"
git branch -M main
git remote add origin https://github.com/WillEnnis/WillEnnis.git
git push -u origin main
```
Refresh `github.com/WillEnnis` — the README is live. Most cards render instantly; the **snake** appears after step 4.

## 4. Turn on the snake animation
The contribution-snake needs one Actions run to generate its SVG:
1. Repo → **Settings → Actions → General** → Workflow permissions → **Read and write** → Save.
2. Repo → **Actions** tab → "Generate contribution snake" → **Run workflow**.
3. It creates an `output` branch with the SVG. The README already points there; refresh and it shows. It then auto-refreshes daily.

> Until that first run, the snake image will show as broken — totally expected.

## 5. Make your profile *complete*
The README is the storefront; recruiters still glance at the rest:
- **Pin 4–6 repos.** Profile → "Customize your pins." Pin your strongest: research write-up, AIOS, portfolio, a class project. A pinned repo with a clean README beats ten empty ones.
- **Add a profile photo + bio + location** in Settings → Profile.
- **Set status** (the emoji bubble) to something like "🔬 Researching conductive 3D printing."

---

## What's different from a generic profile README
- **Engineer-first framing.** Leads with mechanical engineering + research, not a wall of web-dev logos. That's your differentiator — most CS students can't claim additive-manufacturing research.
- **Honest, specific content.** No invented metrics ("92% accuracy / 1,000+ transactions"). Real projects, described concretely. Recruiters smell inflation; specificity reads as credible.
- **Two-track tech stack.** Engineering/CAD/sim *and* software/AI — shown as two distinct sections so neither buries the other.
- **Cohesive blueprint theme.** Every card, badge, and animation shares one navy/teal palette instead of clashing default themes.
- **Auto-maintaining.** Stats, streak, and snake update themselves. Set it once.

## Tuning knobs
- **Palette:** the colors are `0a192f` (navy bg), `64ffda` (teal accent), `8892b0` (slate text), `233554` (border). Search-replace across `README.md` to re-skin.
- **Typing lines:** edit the `lines=` param in the `readme-typing-svg` URL (use `+` for spaces, `%E2%86%92` for →).
- **Progress bars** under `> currently` are hand-set `▓`/`░` — just edit the blocks.
- **Trophy/stat themes:** swap `theme=onedark` etc. Gallery: github-profile-trophy, github-readme-stats docs.

## Third-party services used (all free, no account needed)
`capsule-render` · `readme-typing-svg` · `shields.io` · `skillicons.dev` · `komarev ghpvc` · `github-readme-stats` · `github-readme-streak-stats` · `github-readme-activity-graph` · `Platane/snk`

> Note: I deliberately left out `github-profile-trophy` — its public instance was returning HTTP 402 (over-quota) for everyone at build time. If it recovers and you want trophies back, add: `![trophies](https://github-profile-trophy.vercel.app/?username=WillEnnis&theme=onedark&no-frame=true&column=7)`

> These render images from public APIs. If one is ever down, only that image breaks — the README stays fine. All read **public** data only.
