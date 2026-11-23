# Signal Processing Learning Hub
### *From Signals and Systems to Intelligent Visual Perception*

[![Master Curriculum Baseline](https://img.shields.io/badge/Curriculum%20Baseline-v1.0%20(Frozen)-blue.svg)](#curriculum-architecture)
[![Authored Lessons](https://img.shields.io/badge/Authored%20Lessons-144%2F458-emerald.svg)](#current-state-census)
[![Academic Verification](https://img.shields.io/badge/QA%20Pipeline-100%25%20Passing-success.svg)](#scientific-validation)
[![Academic Homebase](https://img.shields.io/badge/Homebase-Teknik%20Telekomunikasi%20ITERA-gold.svg)](#institutional-attribution)
[![Research Umbrella](https://img.shields.io/badge/Research-ISVWS%202026--2040-purple.svg)](#institutional-attribution)

---

## 1. Overview & Institutional Attribution

**Signal Processing Learning Hub** is an open-access, rigorous academic courseware and computational laboratory system spanning from fundamental signal and systems theory to advanced intelligent sensing and computer vision.

- **Live Website**: [https://aji-nurcahyo.github.io/Signal-Processing-Learning-Hub/](https://aji-nurcahyo.github.io/Signal-Processing-Learning-Hub/)
- **Target Repository**: [https://github.com/aji-nurcahyo/Signal-Processing-Learning-Hub](https://github.com/aji-nurcahyo/Signal-Processing-Learning-Hub)
- **Repository Name**: `Signal-Processing-Learning-Hub`
- **Academic Homebase**: Program Studi Teknik Telekomunikasi, Jurusan Teknologi Produksi dan Industri, Institut Teknologi Sumatera (ITERA).
- **Research Umbrella**: Intelligent Sensing, Vision and Wireless Systems (ISVWS) 2026–2040.
- **Curriculum Baseline**: `MASTER_CURRICULUM_V1.0_BASELINE` (Strictly Frozen: 113 canonical chapters, 458 planned lessons, 284 prerequisite DAG edges).

---

## 2. Current State Census (Core Levels 1–4 Complete)

| Metric / Dimension | Core Level 1 (C01–C06) | Core Level 2 (C07–C17) | Core Level 3 (C18–C25) | Core Level 4 (C26–C35) | Entire Hub Total (Levels 1–4) |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Canonical Chapters Authored** | 6 Chapters | 11 Chapters | 8 Chapters | 10 Chapters | **35 Chapters** |
| **Authored Academic Lessons** | 24 Lessons | 46 Lessons | 33 Lessons | 41 Lessons | **144 Lessons** |
| **Formal Publication Status** | 1 Published (`c01_l01`), 23 Validated | 46 Validated | 33 Validated | 41 Validated | **1 Published, 143 Validated** |
| **Companion Python Scripts** | 24 Scripts (100% Pass) | 46 Scripts (100% Pass) | 33 Scripts (100% Pass) | 41 Scripts (100% Pass) | **144 Scripts (100% Pass)** |
| **Jupyter Notebooks (.ipynb)** | 24 Notebooks (7–10 Cells) | 46 Notebooks (7–10 Cells) | 33 Notebooks (7–10 Cells) | 41 Notebooks (7 Cells) | **144 Notebooks (100% Pass)** |
| **Reveal.js Slide Decks** | 48 Decks (Master + Public) | 92 Decks (Master + Public) | 66 Decks (Master + Public) | 82 Decks (Master + Public) | **288 Slide Decks** |
| **Academic PDF Monographs** | Complete (Internal Preview) | Complete (Internal Preview) | Complete (Internal Preview) | Complete (Internal Preview) | **183 Monographs (4 Volumes)** |

---

## 3. Curriculum Architecture

The curriculum is structured into 4 sequential Core levels:
1. **Core Level 1 — Signal Processing Fundamentals** (`C01–C06`, 24 lessons): Nature of signals, complex phasors, linear algebra foundations, discrete mathematical tools, continuous vs discrete paradigms, and scientific Python toolchains.
2. **Core Level 2 — Signals & Systems** (`C07–C17`, 46 lessons): LTI systems, convolution, difference/differential equations, state-space representations, continuous & discrete Fourier series and transforms, Laplace transforms, and Z-transforms.
3. **Core Level 3 — Sampling & Spectral Processing** (`C18–C25`, 33 lessons): Whittaker-Shannon sampling theorem, quantization ADC/DAC, DFT, FFT Radix-2/4, spectral leakage and windows, stochastic signals and autocorrelation, power spectral density (PSD), and STFT time-frequency analysis.
4. **Core Level 4 — Digital Filtering & Practical DSP** (`C26–C35`, 41 lessons): Frequency response tolerances, linear-phase FIR design, classical IIR approximations (Butterworth, Chebyshev, Elliptic), bilinear transform, signal flow graphs and Tellegen transposition, direct forms I/II, cascade SOS biquads, lattice-ladder structures, minimum-phase/all-pass decomposition, zero-phase filtering (`filtfilt`), Jury stability criterion, fixed-point Q$m.n$ arithmetic, coefficient sensitivity, roundoff noise, multirate polyphase filters, filter banks, 2D signal processing, and the dual-scope Capstone DSP Toolkit.

---

## 4. Local Development & Verification

### Prerequisites
- Node.js 18+ and npm
- Python 3.10+ with `numpy`, `scipy`, `matplotlib`
- Chromium (installed via Playwright for PDF export)

### Setup & Validation Commands
```bash
# Install Node dependencies
npm install

# Run TypeScript type-checking
npx tsc --noEmit

# Run curriculum structural validation (DAG & manifest integrity)
python scripts/validate_curriculum.py

# Run complete 16-component academic content audit (all 144 lessons)
python scripts/validate_content.py

# Run full audit across all 144 companion scripts and notebooks
python scratch/audit_all_144_core.py

# Build public distribution (isolated non-destructive staging)
python scripts/build_public_distribution.py
```

---

## 5. Deployment Policy & GitHub Pages Configuration

The learning hub uses isolated, non-destructive staging to guarantee that internal previews, unapproved lessons, and draft PDFs are never exposed to public builds:
- Only lessons with status `published` (currently strictly `c01_l01`) are packaged into public distributions.
- All 143 `validated` lessons, internal preview PDFs (`.artifacts/pdf-preview/`), and full monograph compilations remain strictly quarantined.
- Vite base path is fully configured for GitHub Pages via `VITE_BASE_PATH=/Signal-Processing-Learning-Hub/`.

---

## 6. Academic License & Attribution

&copy; 2026 Program Studi Teknik Telekomunikasi, Institut Teknologi Sumatera (ITERA).  
Under the Research Umbrella of **Intelligent Sensing, Vision and Wireless Systems (ISVWS) 2026–2040**.  
Developed for educational, scientific, and research purposes.
