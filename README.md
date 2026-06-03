# epitaxy-methods-visualiser

> Step-by-step interactive simulator for 7 epitaxial growth methods — built as a study tool for **EEE 4131: Device Fabrication Techniques**.

Each method is broken into 3–6 animated steps, accompanied by **chemical reaction formulas from the slides**, process parameters, pros/cons, and a **"Why this exists"** panel explaining what problem the method solves over its predecessor.

🔗 **Live demo:** _add your GitHub Pages link here_

---

## Methods Covered

Follows the exact lecture sequence of EEE 4131 slides 09–13:

| # | Method | Lecture | Key idea |
|---|--------|---------|----------|
| 1 | **CVD** — Chemical Vapor Deposition | Lec 9–10 | Sequential 6-step process; heterogeneous surface reactions; rate-limiting concepts |
| 2 | **VPE** — Vapor Phase Epitaxy | Lec 11 | Two-zone tube with T-gradient; covers both **halide** and **hydride** processes for GaAs |
| 3 | **HVPE** — Hydride VPE | Lec 11 | In-situ GaCl generation; very high growth rates for bulk GaN |
| 4 | **MOCVD / MOVPE** — Metal-Organic CVD | Lec 11 | Metal-organic precursors; thermal cracking on wafer; solves AlGaAs problem |
| 5 | **MBE** — Molecular Beam Epitaxy | Lec 12 | UHV + effusion beams + RHEED; atomic-layer precision |
| 6 | **PA-CVD / PE-CVD** — Plasma-Assisted CVD | Lec 13 | RF plasma replaces thermal energy; lower deposition temperature |
| 7 | **ALD** — Atomic Layer Deposition | Lec 13 | A/inert/B/inert pulse sequence; self-limiting; digital monolayer control |

---

## Features

**Simulator panel (center)**
- 3–6 animated SVG steps per method, each covering one discrete stage of the process
- Play / pause / step forward-back / jump to any step via pip bar
- Keyboard controls: `←` `→` to step, `Space` to play/pause

**Method info panel (left)**
- Full name, abbreviation, tagline
- **Key Reactions** — chemical equations from the slides displayed per method
- Process parameters (temperature, pressure, growth rate, precursors)
- Advantages and disadvantages

**"Why this exists" panel (right)**
- Which earlier method this evolved from
- The specific problem the earlier method had
- How this method fixes it — grounded in slide content

**Timeline bar (top)**
- Clickable evolution timeline with lecture numbers: CVD → VPE → HVPE → MOCVD → MBE → PA-CVD → ALD

---

## Chemical Reactions Included

All equations sourced directly from EEE 4131 slides.

**CVD (Lec 9–10)**
- `SiH₄ + O₂ —heat→ SiO₂ + 2H₂`
- `SiH₄(g) ⇌ SiH₂(g) + 2H(g)`
- `Kp(T) = pSiH₂ · pH² / pSiH₄`
- `Kp(T) = K₀ · e^(−ΔG/kT)` (Arrhenius form)

**VPE — Halide process (Lec 11)**
- `AsCl₃(g) + ³⁄₂ H₂(g) ⇌ ¼ As₄(g) + 3HCl(g)`
- `Ga + ¼ As₄ ⇌ GaAs` (crust on Ga source)
- `GaAs + HCl(g) ⇌ GaCl(g) + ½ H₂(g) + ¼ As₄(g)`

**VPE — Hydride process (Lec 11)**
- `Ga(g) + HCl(g) ⇌ GaCl(g) + ½ H₂(g)`
- `AsH₃(g) ⇌ ¼ As₄(g) + ³⁄₂ H₂(g)`
- `GaCl(g) + ¼ As₄ + ½ H₂ ⇌ GaAs(s) + HCl(g)`

**HVPE (Lec 11)**
- `Ga(l) + HCl(g) → GaCl(g) + ½ H₂(g)`
- `GaCl + AsH₃ → GaAs(s) + HCl + H₂`

**MOCVD (Lec 11)**
- `Ga(CH₃)₃ + NH₃ —heat→ GaN(s) + 3CH₄`
- `Ga(CH₃)₃ + AsH₃ —heat→ GaAs(s) + 3CH₄`

**MBE (Lec 12)**
- `Ga(s) —heat→ Ga(g)` · `Ga(g) + ¼As₄(g) → GaAs(s)` (physical condensation, no chemistry)

**PA-CVD (Lec 13)**
- `SiH₄ + e⁻* → SiH₃* + H* + e⁻` (electron-impact dissociation)
- `SiH₃* + surface → Si(s) + H↑`

**ALD (Lec 13)**
- Sequence: `A / inert / B / inert / ...` · 1 cycle ≈ 0.2 nm

---

## Why I Built This

Preparing for my semester exam on these topics. Building animations is unforgiving — you can't fake understanding of which gas enters where, in what order, what reacts with what, and what the product is. The chemical equations embedded in every step meant I had to internalize not just the workflow but the actual chemistry.

The tool may also help:
- Students in semiconductor device fabrication courses
- Quick visual reference for comparing deposition methods
- Anyone learning why CVD has so many variants

---

## Tech Stack

- **HTML5 + CSS3 + Vanilla JS** — single file, no build step, no dependencies
- **SVG + SMIL animations** — atoms flowing, gas streams, plasma particles, effusion beams
- **CSS variables** — full dark-mode design system

Zero npm. Zero frameworks. Just open `index.html`.

---

## Run Locally

```bash
git clone https://github.com/<your-username>/epitaxy-methods-visualiser.git
cd epitaxy-methods-visualiser
# open index.html in any browser
```

**Deploy to GitHub Pages:**
1. Push to a public repo
2. Settings → Pages → Source: `main` branch, `/root`
3. Live at `https://<your-username>.github.io/epitaxy-methods-visualiser`

---

## Controls

| Action | Control |
|--------|---------|
| Select method | Click timeline node |
| Next step | `→` / `next →` button |
| Previous step | `←` / `← prev` button |
| Auto-play | `Space` / `▶ play` |
| Jump to step | Click pip dot |
| Reset | `↺ reset` |

---

## Source Material

Content sourced **strictly** from EEE 4131 lecture slides:

| Lecture | Topics |
|---------|--------|
| 08 | Epitaxy overview, homoepitaxy vs heteroepitaxy, lattice mismatch |
| 09 | CVD fundamentals — process steps, reactions, heterogeneous vs homogeneous |
| 10 | CVD thermodynamics — equilibrium constant, Arrhenius, rate-limiting regimes |
| 11 | VPE (halide + hydride), HVPE, MOCVD/MOVPE — all reactions and reactor diagrams |
| 12 | MBE — UHV, effusion cells, shutters, RHEED, ATG instability |
| 13 | PA-CVD/PE-CVD (RF plasma), ALD (A/inert/B/inert cycle) |

Animations are pedagogical schematics — not to scale, intended for learning.

---

## Repo Structure

```
epitaxy-methods-visualiser/
├── index.html          # entire app — self-contained
└── README.md
```

---

## Roadmap

- [ ] Lec 14 content: auto-doping, junction shift, pattern distortion visualiser
- [ ] Lec 15 content: defect types — stacking fault, edge/screw/threading dislocation
- [ ] Quiz mode — auto-generated from method content
- [ ] Mobile layout polish

---

## License

MIT — fork, reuse, extend freely.

---

_Built by a student, for students. If it helped, drop a ⭐_
