# Mechanics II – Problem Set 3 Solutions

Complete solutions to **Problem Set 3: Dynamics and Energy**, including interactive HTML/JS visualizations for problems requiring graphs or simulations.

## Contents

| File | Description |
|---|---|
| `problem_set_03_solutions.md` | **Main solution file** — all 10 problems solved with full derivations |
| `vis_p1_trajectory.html` | Problem 1 — Animated 2D trajectory (Newton's 2nd law) |
| `vis_p3_spring.html` | Problem 3 — Interactive F(x) and U(x) graphs (Hooke's law) |
| `vis_p4_energy.html` | Problem 4 — Free fall with energy conservation animation |
| `vis_p6_drag.html` | Problem 6 — v(t) and x(t) with linear drag vs no-drag |
| `vis_p7_throw.html` | Problem 7 — Vertical throw with drag: analytical vs Euler numerical |
| `vis_p8_oscillator.html` | Problem 8 — Harmonic oscillator with phase space animation |
| `vis_p9_field.html` | Problem 9 — 2D conservative field with equipotentials and trajectories |
| `vis_p10_nonlinear.html` | Problem 10 — Nonlinear oscillator: potential, x(t), phase portrait |

## How to Use

### Viewing the Solutions (VS Code)

1. Open the project folder in VS Code
2. Install the **Markdown Preview Enhanced** extension (or **Markdown+Math**)
3. Open `problem_set_03_solutions.md`
4. Press `Ctrl+Shift+V` (or `Cmd+Shift+V`) to open the preview with rendered math

> **Alternative:** Install the **Live Preview** extension and open any `.html` file directly in the browser.

### Running the Visualizations

**Option A — Double-click** any `.html` file to open it in your default browser.

**Option B — VS Code Live Server:**
1. Install the *Live Server* extension
2. Right-click any `.html` file → *Open with Live Server*

All visualizations are **self-contained** — no internet connection or server required.

## Physics Topics Covered

1. **Newton's Second Law** — constant force, 2D kinematics, work-energy theorem
2. **Inclined Plane with Friction** — normal force, kinetic friction, energy balance
3. **Variable Force Work** — Hooke's law, potential energy, conservative force
4. **Conservation of Energy** — free fall, kinetic/potential energy exchange
5. **Elastic Collision** — momentum & energy conservation, special cases
6. **Linear Drag** — exponential decay, terminal behaviour
7. **Vertical Throw with Drag** — first-order ODE, analytical vs numerical (Euler)
8. **Harmonic Oscillator** — SHM, natural frequency, phase space
9. **Conservative Field in 2D** — gradient, equipotentials, Lissajous trajectories
10. **Anharmonic / Nonlinear Oscillator** — RK4 numerics, double-well potential, phase portrait

## Setup for GitHub

```bash
# Clone your repository
git clone https://github.com/YOUR_USERNAME/YOUR_REPO.git
cd YOUR_REPO

# Copy all solution files into the repo
cp path/to/problem_set_03_solutions.md .
cp path/to/vis_p*.html .

# Stage and commit
git add problem_set_03_solutions.md vis_p*.html README.md
git commit -m "Add Problem Set 3 solutions with interactive visualizations"
git push origin main
```

### Enable GitHub Pages (optional — live HTML demos)

1. Go to **Settings → Pages** in your repository
2. Set Source to `main` branch, `/ (root)` folder
3. Your visualizations will be live at:
   `https://YOUR_USERNAME.github.io/YOUR_REPO/vis_p1_trajectory.html`

## Math Rendering Note

GitHub's Markdown preview **does not render LaTeX** natively. To see equations:
- Use VS Code with *Markdown Preview Enhanced*
- Or view locally — all equations use standard `$...$` and `$$...$$` delimiters
- GitHub supports basic math in Markdown (between `$` signs) since 2022 — it should render in the repository view on github.com
