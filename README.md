# Crystal Prism Praxis

**CRYSTAL PRISM v45** SPARC validation + **Mars Mission** triple-engine hub.

| Live URL (enable Pages once — see below) | Repo |
|------------------------------------------|------|
| [rosary-mom.github.io/Crystal-Prism-Praxis-](https://rosary-mom.github.io/Crystal-Prism-Praxis-/) | [github.com/Rosary-mom/Crystal-Prism-Praxis-](https://github.com/Rosary-mom/Crystal-Prism-Praxis-) |

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

## Deploy (one-time setup)

### GitHub Pages — **ready** (`gh-pages` branch pushed)

1. Open [Repo Settings → Pages](https://github.com/Rosary-mom/Crystal-Prism-Praxis-/settings/pages)
2. **Build and deployment** → Source: **Deploy from a branch**
3. Branch: **`gh-pages`** / **`/ (root)`** → Save
4. Live at: **https://rosary-mom.github.io/Crystal-Prism-Praxis-/**

> If Actions are enabled: `.github/workflows/pages.yml` auto-deploys on every `main` push.

### Vercel (optional)

1. [vercel.com/new](https://vercel.com/new) → Import `Rosary-mom/Crystal-Prism-Praxis-`
2. Framework: **Other** · Root: `/`
3. Or CLI: `vercel login` then `npx vercel --prod`

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