# Crystal Prism Praxis

**CRYSTAL PRISM v45** SPARC validation + **Mars Mission** triple-engine hub.

| Live (after deploy) | Repo |
|---------------------|------|
| [crystal-prism-praxis.vercel.app](https://crystal-prism-praxis.vercel.app) | [github.com/Rosary-mom/Crystal-Prism-Praxis-](https://github.com/Rosary-mom/Crystal-Prism-Praxis-) |

## Triple-Engine Stack

| Engine | Physics | Game role |
|--------|---------|-----------|
| **DWARF** | Newtonian thrust + gravity | Mars lander (↑ thrust) |
| **CRYSTAL PRISM** | \(V_{\text{vortex}} = \alpha V_{\text{flat}}(1 - e^{-r/r_{\text{scale}}})\) | Mid-tier transit (SPARC α≈1) |
| **Alcubierre** | Shaping \(f(r)\), York time \(\theta\), \(\rho < 0\) | Endgame warp bubble |

## Repository layout

| File | Description |
|------|-------------|
| [`index.html`](index.html) | **Production** — full Mars Mission cockpit (deploy this) |
| [`crystal-prism-praxis-editor.html`](crystal-prism-praxis-editor.html) | **Editor copy** — identical HTML for IDE / offline edit |
| [`mars-mission-classic.html`](mars-mission-classic.html) | Original [blizzwar.vercel.app](https://blizzwar.vercel.app/) mirror |
| [`blitzkrieg.html`](blitzkrieg.html) | BLIZZWAR v2.6 dashboard (Aether, YRAZOR II) |
| [`crystal_prism_v45.py`](crystal_prism_v45.py) | 175-galaxy SPARC catalog validator |
| [`vercel.json`](vercel.json) | Routes `/` → `index.html` |

## Quick start (local)

```bash
git clone https://github.com/Rosary-mom/Crystal-Prism-Praxis-.git
cd Crystal-Prism-Praxis-
python -m http.server 8080
```

Open [http://localhost:8080](http://localhost:8080) or edit `crystal-prism-praxis-editor.html` in your IDE.

## SPARC validation (Python)

```bash
pip install -r requirements.txt
python crystal_prism_v45.py
```

Downloads SPARC `Rotmod_LTG.zip` from Zenodo on first run into `sparc_data/`.

## Deploy to Vercel

### Option A — GitHub import (recommended)

1. Go to [vercel.com/new](https://vercel.com/new)
2. Import `Rosary-mom/Crystal-Prism-Praxis-`
3. Framework: **Other** (static)
4. Root directory: `/` (default)
5. Deploy — `vercel.json` handles routing

### Option B — CLI

```bash
npm i -g vercel
cd Crystal-Prism-Praxis-
vercel --prod
```

### Option C — GitHub Pages

Settings → Pages → Source: **GitHub Actions** (workflow included) or branch `main` / root.

Site URL: `https://rosary-mom.github.io/Crystal-Prism-Praxis-/`

## Edit the HTML

Open **`crystal-prism-praxis-editor.html`** in VS Code, Cursor, or any editor. It is a byte-identical copy of `index.html` intended for local editing. After changes, copy back to `index.html` and push.

Key sections in the file:

- **Lines 1–114** — CSS (warp, prism, cockpit)
- **Lines 116–427** — HTML structure (cockpit, warp, prism, manhunt, quiz)
- **Lines 429–1060** — JavaScript game engine

## Theory & references

- [Spacetime Vortex Solves Dark Matter (Zenodo)](https://zenodo.org/doi/10.5281/zenodo.21047009)
- [SPARC rotation curves (Zenodo)](https://zenodo.org/records/16284118)
- [blizzwar.vercel.app](https://blizzwar.vercel.app/) — legacy Mars Mission mirror

## License & credit

© ROSARY 2026 ff · PROJEKT CHIMERA · Be a SuperHero — "CHIMMY" 🦸‍♂️