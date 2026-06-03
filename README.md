# Epitaxy Methods Visualiser

> Interactive, step-by-step simulator of 8 epitaxial growth methods used in semiconductor manufacturing — built as a study tool for **EEE 4131: Device Fabrication Techniques**.

Each method is animated frame-by-frame, accompanied by parameters, pros/cons, and a **"Why this exists"** panel that explains what problem the method solves compared to its predecessor.

🔗 **Live demo:** _add your GitHub Pages link here_

---

## ✨ Features

- **Evolution timeline** — navigate 8 methods historically: LPE → VPE → MOCVD → HVPE → PA-CVD → MBE → CBE → ALD → SPE
- **Step-by-step animations** — every method broken into 3–5 discrete pedagogical steps (no opaque flashy motion)
- **Process narrative** — each step has a title + plain-language explanation grounded in textbook content
- **Comparative "why" panel** — for every method: previous method's limitation + how this one fixes it
- **Parameters & trade-offs** — temperature ranges, growth rates, vacuum levels, advantages, disadvantages
- **Visual legend per method** — color coding for atoms, gases, electrodes, beams
- **Keyboard controls** — `←` / `→` to step, `Space` to play/pause
- **Zero dependencies** — pure HTML + CSS + JS in a single file. No build, no install, no API keys.

---

## 🔬 Methods Covered

| # | Method | Key idea |
|---|--------|----------|
| 1 | **LPE** — Liquid Phase Epitaxy | Direct precipitation from a liquid melt |
| 2 | **VPE** — Vapor Phase Epitaxy (CVD) | Gaseous precursors react on a heated substrate |
| 3 | **MOCVD / MOVPE** — Metal-Organic CVD | Metal-organic precursors enable AlGaAs & low-vapor-pressure materials |
| 4 | **HVPE** — Hydride VPE | In-situ metal chlorides → very high growth rates for bulk GaN |
| 5 | **PA-CVD / PE-CVD** — Plasma-Assisted CVD | RF plasma breaks precursors → low-temperature deposition |
| 6 | **MBE** — Molecular Beam Epitaxy | UHV + effusion beams + RHEED → atomic-layer precision |
| 7 | **CBE** — Chemical Beam Epitaxy | Hybrid: MBE-style UHV chamber with gas-source chemistry |
| 8 | **ALD** — Atomic Layer Deposition | A/inert/B/inert pulses → digital monolayer-by-monolayer control |
| 9 | **SPE** — Solid Phase Epitaxy | Thermal recrystallisation of amorphous damaged layers |

---

## 🎯 Why I Built This

I'm preparing for my semester exam on these topics and wanted a study tool that would force me to deeply understand each method's workflow — not just memorize bullet points. Building animations is unforgiving: if you don't know which gas enters where, in what order, and what reacts with what, the SVG won't make sense.

By the end of the build, I had internalized all 8 methods well enough to explain them step-by-step.

The tool may also be useful for:

- Students taking semiconductor / device fabrication courses
- Quick visual reference for engineers comparing thin-film deposition options
- Anyone curious about how chips are physically grown

---

## 🛠️ Tech Stack

- **HTML5** — single-file structure
- **CSS3** — custom design system with CSS variables, grid layout, dark theme
- **Vanilla JS** — state-driven rendering, SVG generation, animation control
- **SVG + SMIL** — declarative animations (atoms drifting, gas flow, plasma particles, electron beams)

No frameworks. No package.json. Just open `index.html`.

---

## 🚀 Run Locally

```bash
git clone https://github.com/<your-username>/epitaxy-methods-visualiser.git
cd epitaxy-methods-visualiser
# open index.html in any browser
```

Or deploy via GitHub Pages:

1. Push to a public repo
2. Settings → Pages → Source: `main` branch
3. Done — your tool is live

---

## 🎮 Controls

| Action | Control |
|--------|---------|
| Pick a method | Click any timeline node |
| Next step | `→` arrow / `next →` button |
| Previous step | `←` arrow / `← prev` button |
| Auto-play | `Space` / `▶ play` button |
| Jump to step | Click any pip in the controls bar |
| Reset | `↺ reset` button |

---

## 📚 Source Material

All content is sourced strictly from **EEE 4131 lecture slides 08–15**:

- Lecture 08 — Epitaxy overview, heteroepitaxy, lattice mismatch
- Lecture 09 — Chemical Vapor Deposition fundamentals
- Lecture 10 — CVD reactor types and gas kinetics
- Lecture 11 — VPE, HVPE, MOVPE/MOCVD
- Lecture 12 — Molecular Beam Epitaxy
- Lecture 13 — Plasma-Assisted CVD, Atomic Layer Deposition
- Lecture 14 — Doping during epitaxy
- Lecture 15 — Defects in epitaxial layers

Animations are pedagogical schematics — not to scale, and intended for learning rather than process simulation.

---

## 🗺️ Roadmap

- [ ] Comparison mode (side-by-side two methods on one canvas)
- [ ] Defect simulation (stacking faults, threading dislocations from Lec 15)
- [ ] Doping visualisation (in-situ vs ex-situ, auto-doping)
- [ ] Mobile-responsive layout polish
- [ ] Quiz mode (auto-generated questions from method content)

---

## 📄 License

MIT — feel free to fork, extend, and reuse for your own coursework or teaching.

---

## 🙋 Author

Built by a student for students. If this helped you, drop a ⭐ — or open an issue with corrections / suggestions.
