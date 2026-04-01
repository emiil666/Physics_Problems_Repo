# Problem Set 3 — Mechanics II: Dynamics and Energy
## Complete Solutions

> **VS Code tip:** Install the *Markdown+Math* extension (or *Markdown Preview Enhanced*) to render LaTeX equations. Open interactive HTML visualizations by right-clicking any linked `.html` file → *Open with Live Server* (or just double-click to open in browser).

---

## Table of Contents

1. [Problem 1 – Newton's Second Law (Constant Force)](#problem-1--newtons-second-law-constant-force)
2. [Problem 2 – Inclined Plane with Friction](#problem-2--inclined-plane-with-friction)
3. [Problem 3 – Work of a Variable Force](#problem-3--work-of-a-variable-force)
4. [Problem 4 – Conservation of Energy](#problem-4--conservation-of-energy)
5. [Problem 5 – Momentum and Elastic Collision](#problem-5--momentum-and-one-dimensional-elastic-collision)
6. [Problem 6 – Motion with Linear Drag](#problem-6--motion-with-linear-drag)
7. [Problem 7 – Vertical Throw with Drag](#problem-7--vertical-throw-with-drag)
8. [Problem 8 – Harmonic Oscillator](#problem-8--harmonic-oscillator)
9. [Problem 9 – Potential and Conservative Field](#problem-9--potential-and-conservative-field)
10. [Problem 10 – Numerical Model of a Dynamical System](#problem-10--numerical-model-of-a-dynamical-system)

---

## Problem 1 – Newton's Second Law (Constant Force)

**Given:** $m = 2\ \mathrm{kg}$, $\vec{F} = (6,\ 2)\ \mathrm{N}$, $\vec{v}(0) = (1,\ -1)\ \mathrm{m/s}$, $\vec{r}(0) = (0,0)\ \mathrm{m}$

---

### 1.1 Acceleration $\vec{a}(t)$

From Newton's second law $\vec{F} = m\vec{a}$:

$$
\vec{a} = \frac{\vec{F}}{m} = \frac{(6,\ 2)}{2} = (3,\ 1)\ \mathrm{m/s^2}
$$

Since the force is constant, the acceleration is **constant** and independent of time.

---

### 1.2 Velocity $\vec{v}(t)$

Integrating acceleration with initial condition $\vec{v}(0) = (1,\ -1)$:

$$
\vec{v}(t) = \vec{v}(0) + \vec{a}\,t = (1 + 3t,\quad -1 + t)\ \mathrm{m/s}
$$

---

### 1.3 Position $\vec{r}(t)$

Integrating velocity with initial condition $\vec{r}(0) = (0, 0)$:

$$
\vec{r}(t) = \vec{r}(0) + \vec{v}(0)\,t + \tfrac{1}{2}\vec{a}\,t^2 = \left(\frac{3}{2}t^2 + t,\quad \frac{1}{2}t^2 - t\right)\ \mathrm{m}
$$

Explicitly:

$$
x(t) = \tfrac{3}{2}t^2 + t, \qquad y(t) = \tfrac{1}{2}t^2 - t
$$

---

### 1.4 Trajectory (Parametric)

Eliminating $t$: from $y(t) = \tfrac{1}{2}t^2 - t$ and $x(t) = \tfrac{3}{2}t^2 + t$, we find $t$ from the system. The trajectory is a **parabola** in the $xy$-plane (uniformly accelerated motion in 2D always produces a parabolic path).

➡️ **[Open interactive trajectory animation → vis_p1_trajectory.html](vis_p1_trajectory.html)**

---

### 1.5 Work Done by the Force at $t = 3\ \mathrm{s}$

**Method 1 — Direct calculation:**

$$
W = \vec{F} \cdot \Delta\vec{r} = \vec{F} \cdot [\vec{r}(3) - \vec{r}(0)]
$$

$$
\vec{r}(3) = \left(\tfrac{3}{2}\cdot 9 + 3,\quad \tfrac{1}{2}\cdot 9 - 3\right) = (13.5 + 3,\; 4.5 - 3) = (16.5,\; 1.5)\ \mathrm{m}
$$

$$
W = (6,2)\cdot(16.5, 1.5) = 6 \times 16.5 + 2 \times 1.5 = 99 + 3 = \boxed{102\ \mathrm{J}}
$$

---

### 1.6 Verification with the Work-Energy Theorem

The work-energy theorem states: $W = \Delta KE = \tfrac{1}{2}m v^2(3) - \tfrac{1}{2}m v^2(0)$

$$
\vec{v}(3) = (1 + 9,\; -1 + 3) = (10,\; 2)\ \mathrm{m/s}
$$

$$
KE(3) = \tfrac{1}{2} \times 2 \times (10^2 + 2^2) = 1 \times 104 = 104\ \mathrm{J}
$$

$$
KE(0) = \tfrac{1}{2} \times 2 \times (1^2 + 1^2) = 2\ \mathrm{J}
$$

$$
\Delta KE = 104 - 2 = 102\ \mathrm{J} \quad \checkmark
$$

**Result is consistent with the work-energy theorem.** ✅

---

## Problem 2 – Inclined Plane with Friction

**Given:** Mass $m$, angle $\alpha$, kinetic friction coefficient $\mu$

---

### 2.1 Forces Acting on the Body

Using axes along (x) and perpendicular to (y) the incline:

| Force | Along incline | Perpendicular to incline |
|---|---|---|
| Gravity component | $mg\sin\alpha$ (down the slope) | $-mg\cos\alpha$ |
| Normal force $N$ | $0$ | $+N$ |
| Friction $f = \mu N$ | $-\mu mg\cos\alpha$ (opposing motion, up slope) | $0$ |

Equilibrium perpendicular to incline: $N = mg\cos\alpha$

---

### 2.2 Acceleration

Newton's second law along the incline (taking down the slope as positive):

$$
ma = mg\sin\alpha - \mu mg\cos\alpha
$$

$$
\boxed{a = g(\sin\alpha - \mu\cos\alpha)}
$$

For motion to occur (body slides): $\tan\alpha > \mu$

---

### 2.3 Time of Descent from Height $h$

The length of the slope is $L = h/\sin\alpha$. Starting from rest ($v_0 = 0$):

$$
L = \tfrac{1}{2}a t^2 \implies t = \sqrt{\frac{2L}{a}} = \sqrt{\frac{2h}{a\sin\alpha}}
$$

$$
\boxed{t = \sqrt{\frac{2h}{g\sin\alpha(\sin\alpha - \mu\cos\alpha)}}}
$$

---

### 2.4 Final Velocity

$$
v = at = \sqrt{2aL} = \sqrt{2g(\sin\alpha - \mu\cos\alpha)\cdot\frac{h}{\sin\alpha}}
$$

$$
\boxed{v = \sqrt{\frac{2gh(\sin\alpha - \mu\cos\alpha)}{\sin\alpha}}}
$$

---

### 2.5 Energy Balance Check

Energy lost to friction: $W_f = \mu mg\cos\alpha \cdot L = \mu mg\cos\alpha \cdot \frac{h}{\sin\alpha} = \mu mgh\cot\alpha$

By energy conservation:
$$
mgh = \tfrac{1}{2}mv^2 + W_f
$$

$$
\tfrac{1}{2}mv^2 = mgh - \mu mgh\cot\alpha = mgh\left(1 - \frac{\mu\cos\alpha}{\sin\alpha}\right) = mgh\cdot\frac{\sin\alpha - \mu\cos\alpha}{\sin\alpha}
$$

$$
v^2 = \frac{2gh(\sin\alpha - \mu\cos\alpha)}{\sin\alpha} \quad \checkmark
$$

**Consistent with direct kinematic result.** ✅

---

## Problem 3 – Work of a Variable Force

**Given:** $F(x) = -kx$ (Hooke's Law / spring force)

---

### 3.1 Equation of Motion and Solution

Newton's second law:

$$
m\ddot{x} = -kx \implies \ddot{x} + \omega_0^2 x = 0, \quad \omega_0 = \sqrt{\frac{k}{m}}
$$

General solution (simple harmonic motion):

$$
\boxed{x(t) = A\cos(\omega_0 t) + B\sin(\omega_0 t)}
$$

where $A$ and $B$ are determined by initial conditions.

---

### 3.2 Work Done from $0$ to $x_0$

$$
W = \int_0^{x_0} F(x)\,dx = \int_0^{x_0} (-kx)\,dx = \left[-\frac{k}{2}x^2\right]_0^{x_0} = -\frac{1}{2}kx_0^2
$$

$$
\boxed{W = -\frac{1}{2}kx_0^2}
$$

The negative sign means the spring force does **negative work** when the body moves away from equilibrium (force opposes displacement).

---

### 3.3 Interpretation as Potential Energy

The work done by the spring force equals the negative change in potential energy:

$$
W = -\Delta U \implies U(x_0) - U(0) = \frac{1}{2}kx_0^2
$$

Taking $U(0) = 0$:

$$
\boxed{U(x) = \frac{1}{2}kx^2}
$$

This is the **elastic potential energy** stored in the spring.

---

### 3.4 Verification: $F = -\dfrac{dU}{dx}$

$$
-\frac{dU}{dx} = -\frac{d}{dx}\left(\frac{1}{2}kx^2\right) = -kx = F(x) \quad \checkmark
$$

---

### 3.5 Graphs of $F(x)$ and $U(x)$

➡️ **[Open interactive graph → vis_p3_spring.html](vis_p3_spring.html)**

Key features:
- $F(x) = -kx$: linear, passes through origin, negative slope $-k$
- $U(x) = \tfrac{1}{2}kx^2$: upward parabola, minimum at $x=0$
- The force always points toward the minimum of potential energy (restoring force)

---

## Problem 4 – Conservation of Energy (Free Fall)

**Given:** Body falls from height $h$, no air resistance, $g = 9.81\ \mathrm{m/s^2}$

---

### 4.1 Total Energy

Taking ground as reference level ($U = 0$ at $y = 0$):

$$
U(y) = mgy, \qquad T(y) = \tfrac{1}{2}mv^2(y)
$$

$$
\boxed{E = T + U = \tfrac{1}{2}mv^2 + mgy = mgh = \text{const}}
$$

At height $h$: $v = 0$, so $E = mgh$. Energy is conserved throughout the fall.

---

### 4.2 Velocity as a Function of Height

From $E = mgh$:

$$
\tfrac{1}{2}mv^2 + mgy = mgh \implies v^2 = 2g(h - y)
$$

$$
\boxed{v(y) = \sqrt{2g(h-y)}}
$$

At ground ($y = 0$): $v = \sqrt{2gh}$ (classical result).

---

### 4.3 Comparison with Newton's Second Law

From kinematics with constant acceleration $g$, falling from rest over distance $h$:

$$
v^2 = 2gh \quad \checkmark
$$

Both approaches give the same result — as expected since energy conservation is derived from Newton's second law for conservative forces.

---

### 4.4 Height Where $T = 0.75\,E$

$$
T = 0.75\,E \implies mgy = 0.25\,E = 0.25\,mgh
$$

$$
\boxed{y^* = 0.25\,h}
$$

At one quarter of the initial height, kinetic energy accounts for 75% of total energy, and potential energy for 25%.

➡️ **[Open interactive energy visualization → vis_p4_energy.html](vis_p4_energy.html)**

---

## Problem 5 – Momentum and One-Dimensional Elastic Collision

**Given:** Masses $m_1$, $m_2$ with initial velocities $u_1$, $u_2$; elastic collision

---

### 5.1 Conservation Laws

**Conservation of momentum:**
$$
m_1 u_1 + m_2 u_2 = m_1 v_1 + m_2 v_2 \tag{1}
$$

**Conservation of kinetic energy (elastic):**
$$
\tfrac{1}{2}m_1 u_1^2 + \tfrac{1}{2}m_2 u_2^2 = \tfrac{1}{2}m_1 v_1^2 + \tfrac{1}{2}m_2 v_2^2 \tag{2}
$$

---

### 5.2 Velocities After Collision

Solving the system (1) & (2):

$$
\boxed{v_1 = \frac{m_1 - m_2}{m_1 + m_2}u_1 + \frac{2m_2}{m_1 + m_2}u_2}
$$

$$
\boxed{v_2 = \frac{2m_1}{m_1 + m_2}u_1 + \frac{m_2 - m_1}{m_1 + m_2}u_2}
$$

**Derivation hint:** Rewrite energy conservation as $(u_1 - u_2) = -(v_1 - v_2)$ — the relative velocity reverses sign in an elastic collision.

---

### 5.3 Special Case: $m_1 = m_2 = m$

$$
v_1 = \frac{0}{2m}u_1 + \frac{2m}{2m}u_2 = u_2
$$

$$
v_2 = \frac{2m}{2m}u_1 + \frac{0}{2m}u_2 = u_1
$$

$$
\boxed{v_1 = u_2, \quad v_2 = u_1}
$$

**The two bodies exchange velocities** — the classic billiard-ball behavior. If $u_2 = 0$, body 1 stops and body 2 moves off with $u_1$.

---

### 5.4 Limit $m_2 \gg m_1$

When $m_2 \to \infty$ (massive wall):

$$
v_1 \approx \frac{-m_2}{m_2}u_1 + \frac{2m_2}{m_2}u_2 = -u_1 + 2u_2
$$

$$
v_2 \approx u_2
$$

If $u_2 = 0$ (wall at rest): $v_1 = -u_1$, $v_2 = 0$.

$$
\boxed{v_1 = -u_1 + 2u_2, \quad v_2 \approx u_2}
$$

**The light body bounces off with reversed velocity in the wall's frame.**

---

### 5.5 Physical Interpretation

| Scenario | Result | Intuition |
|---|---|---|
| Equal masses | Velocities exchange | Maximum momentum transfer |
| $m_2 \gg m_1$ | Light body reverses, heavy barely moves | Wall reflection |
| $m_1 \gg m_2$ | Heavy body barely slows, light body launched at $\approx 2u_1$ | Slingshot effect |

---

## Problem 6 – Motion with Linear Drag

**Given:** $F = -kv$, $v(0) = v_0$, $x(0) = 0$

---

### 6.1 Equation of Motion and Solution

$$
m\dot{v} = -kv \implies \frac{dv}{v} = -\frac{k}{m}dt
$$

Integrating:

$$
\ln v = -\frac{k}{m}t + C \implies \boxed{v(t) = v_0\,e^{-t/\tau}}, \quad \tau = \frac{m}{k}
$$

Integrating again for position:

$$
x(t) = \int_0^t v_0 e^{-s/\tau}ds = v_0\tau\left(1 - e^{-t/\tau}\right) = \frac{mv_0}{k}\left(1 - e^{-kt/m}\right)
$$

$$
\boxed{x(t) = \frac{mv_0}{k}\left(1 - e^{-kt/m}\right)}
$$

---

### 6.2 Limiting Behaviour as $t \to \infty$

$$
\lim_{t\to\infty} v(t) = v_0 \cdot 0 = \boxed{0}
$$

$$
\lim_{t\to\infty} x(t) = \frac{mv_0}{k}
$$

The body **asymptotically comes to rest** after traveling a total distance $x_\infty = mv_0/k$.

---

### 6.3 Comparison with Drag-Free Motion

| Quantity | No drag | With drag ($F = -kv$) |
|---|---|---|
| $v(t)$ | $v_0$ (constant) | $v_0 e^{-kt/m}$ (decays) |
| $x(t)$ | $v_0 t$ (unbounded) | $\frac{mv_0}{k}(1 - e^{-kt/m})$ (bounded) |
| $x(\infty)$ | $\infty$ | $\frac{mv_0}{k}$ (finite) |

For small $t$: drag solution $\approx v_0 t - \frac{k v_0}{2m}t^2 + \ldots$ — the quadratic term represents the effect of drag.

➡️ **[Open interactive graph → vis_p6_drag.html](vis_p6_drag.html)**

---

## Problem 7 – Vertical Throw with Drag

**Given:** $m\dfrac{dv}{dt} = -mg - kv$, $v(0) = v_0 > 0$, $x(0) = 0$ (upward positive)

---

### 7.1 Solution of the ODE

Rearranging:

$$
\frac{dv}{v + mg/k} = -\frac{k}{m}dt
$$

Let $v_t = mg/k$ (terminal velocity magnitude):

$$
\ln\left(v + v_t\right) = -\frac{k}{m}t + C
$$

Applying $v(0) = v_0$:

$$
\boxed{v(t) = \left(v_0 + v_t\right)e^{-t/\tau} - v_t}, \quad \tau = \frac{m}{k},\quad v_t = \frac{mg}{k}
$$

Position (integrating):

$$
\boxed{x(t) = \left(v_0 + v_t\right)\tau\left(1 - e^{-t/\tau}\right) - v_t\,t}
$$

---

### 7.2 Maximum Height

At maximum height, $v(t^*) = 0$:

$$
\left(v_0 + v_t\right)e^{-t^*/\tau} = v_t \implies t^* = \tau\ln\left(1 + \frac{v_0}{v_t}\right)
$$

$$
\boxed{h_{max} = \left(v_0 + v_t\right)\tau\left(1 - e^{-t^*/\tau}\right) - v_t\,t^*}
$$

Substituting $e^{-t^*/\tau} = v_t/(v_0 + v_t)$:

$$
h_{max} = v_0\tau - v_t\tau\ln\left(1 + \frac{v_0}{v_t}\right)
$$

---

### 7.3 Comparison with No-Drag Case

Without drag: $h_{max}^{(0)} = \dfrac{v_0^2}{2g}$

For small drag ($v_0 \ll v_t$), using $\ln(1+\varepsilon) \approx \varepsilon - \varepsilon^2/2$:

$$
h_{max} \approx v_0\tau - v_t\tau\left(\frac{v_0}{v_t} - \frac{v_0^2}{2v_t^2}\right) = \frac{v_0^2}{2g}\cdot\frac{1}{1 + v_0/(3v_t) + \ldots} < h_{max}^{(0)}
$$

**Drag always reduces the maximum height.**

---

### 7.4 Numerical Simulation

The numerical simulation uses Euler's method with step $\Delta t = 0.01\ \mathrm{s}$:

$$
v_{n+1} = v_n + \Delta t\cdot\frac{-mg - kv_n}{m}, \qquad x_{n+1} = x_n + v_n\Delta t
$$

➡️ **[Open interactive simulation → vis_p7_throw.html](vis_p7_throw.html)**

---

### 7.5 Analytical vs. Numerical Comparison

The Euler method introduces first-order errors of $O(\Delta t)$. For the exponential solution, the numerical result tracks the analytical closely for small $\Delta t$. The interactive visualization demonstrates this convergence.

---

## Problem 8 – Harmonic Oscillator

**Given:** $m\ddot{x} + kx = 0$

---

### 8.1 Solution

The characteristic equation $m\lambda^2 + k = 0$ gives $\lambda = \pm i\omega_0$:

$$
\boxed{x(t) = A\cos(\omega_0 t) + B\sin(\omega_0 t)}
$$

Equivalently: $x(t) = C\cos(\omega_0 t + \phi)$, where $C = \sqrt{A^2 + B^2}$, $\tan\phi = -B/A$.

---

### 8.2 Natural Frequency

$$
\boxed{\omega_0 = \sqrt{\frac{k}{m}}\ \mathrm{[rad/s]}}, \qquad f_0 = \frac{\omega_0}{2\pi}\ \mathrm{[Hz]}, \qquad T = \frac{2\pi}{\omega_0}\ \mathrm{[s]}
$$

The period $T$ is **independent of amplitude** (isochronous oscillation).

---

### 8.3 Energy as a Function of Time

$$
T(t) = \tfrac{1}{2}m\dot{x}^2 = \tfrac{1}{2}m\omega_0^2 C^2\sin^2(\omega_0 t + \phi) = \tfrac{1}{2}kC^2\sin^2(\omega_0 t + \phi)
$$

$$
U(t) = \tfrac{1}{2}kx^2 = \tfrac{1}{2}kC^2\cos^2(\omega_0 t + \phi)
$$

$$
\boxed{E = T + U = \tfrac{1}{2}kC^2 = \text{const}}
$$

Using $\sin^2\theta + \cos^2\theta = 1$.

---

### 8.4 Energy Conservation

$$
\frac{dE}{dt} = m\dot{x}\ddot{x} + kx\dot{x} = \dot{x}(m\ddot{x} + kx) = \dot{x}\cdot 0 = 0 \quad \checkmark
$$

Energy is conserved because the restoring force is conservative.

---

### 8.5 Phase Space Interpretation

In the phase plane $(x, p)$ with $p = m\dot{x}$:

$$
\frac{x^2}{C^2} + \frac{p^2}{(m\omega_0 C)^2} = 1
$$

This is an **ellipse** in phase space. Each orbit corresponds to a different energy $E = \tfrac{1}{2}kC^2$. The motion is periodic and the trajectory is closed (no dissipation).

➡️ **[Open phase space animation → vis_p8_oscillator.html](vis_p8_oscillator.html)**

---

## Problem 9 – Potential and Conservative Field

**Given:** $U(x,y) = \dfrac{k}{2}(x^2 + y^2)$

---

### 9.1 Force as the Gradient of the Potential

$$
\vec{F} = -\nabla U = -\left(\frac{\partial U}{\partial x},\ \frac{\partial U}{\partial y}\right) = -(kx,\ ky) = -k(x, y)
$$

$$
\boxed{\vec{F}(x,y) = -k\vec{r}}
$$

This is an **isotropic 2D harmonic restoring force** (2D spring), always pointing toward the origin.

---

### 9.2 Equations of Motion

$$
m\ddot{x} = -kx, \qquad m\ddot{y} = -ky
$$

Both equations are independent and have the same natural frequency $\omega_0 = \sqrt{k/m}$.

---

### 9.3 Type of Motion

General solutions:

$$
x(t) = A_x\cos(\omega_0 t + \phi_x), \qquad y(t) = A_y\cos(\omega_0 t + \phi_y)
$$

Since both oscillations share the **same frequency**, the trajectory is a **Lissajous figure with ratio 1:1**, which in general is an **ellipse** (or a circle if $A_x = A_y$ and $\phi_y - \phi_x = \pi/2$, or a straight line if $\phi_x = \phi_y$).

---

### 9.4 Total Energy

$$
E = \tfrac{1}{2}m(\dot{x}^2 + \dot{y}^2) + \tfrac{k}{2}(x^2 + y^2) = \tfrac{1}{2}kA_x^2 + \tfrac{1}{2}kA_y^2 = \text{const}
$$

---

### 9.5 Geometric Interpretation — Interactive Application

➡️ **[Open 2D potential field app → vis_p9_field.html](vis_p9_field.html)**

The equipotential surfaces are **concentric circles** $x^2 + y^2 = \text{const}$ (level sets of the paraboloid $U$). Force vectors are perpendicular to these circles, pointing inward. Trajectories are ellipses inscribed within the equipotential curves.

---

## Problem 10 – Numerical Model of a Dynamical System

**Given:** $U(x) = \dfrac{k}{2}x^2 + \lambda x^4$

---

### 10.1 Force

$$
F(x) = -\frac{dU}{dx} = -kx - 4\lambda x^3
$$

$$
\boxed{F(x) = -kx - 4\lambda x^3}
$$

For $\lambda > 0$: force is always restoring (anharmonic oscillator). For $\lambda < 0$, $k > 0$: double-well potential (bistable system).

---

### 10.2 Equation of Motion

$$
m\ddot{x} = -kx - 4\lambda x^3
$$

This is a **nonlinear ODE** — no closed-form solution in general. Numerical methods are required.

---

### 10.3 Numerical Solution — Runge-Kutta 4

Rewrite as a first-order system with $v = \dot{x}$:

$$
\dot{x} = v, \qquad \dot{v} = \frac{-kx - 4\lambda x^3}{m}
$$

RK4 step:
$$
k_1 = f(t_n, y_n)\Delta t, \quad k_2 = f\!\left(t_n + \tfrac{\Delta t}{2}, y_n + \tfrac{k_1}{2}\right)\Delta t, \ldots
$$

$$
y_{n+1} = y_n + \tfrac{1}{6}(k_1 + 2k_2 + 2k_3 + k_4)
$$

---

### 10.4 Effect of Initial Energy on Motion

| $E$ vs. $U_{max}$* | Motion type | Phase portrait |
|---|---|---|
| Low $E$ | Bounded oscillation near origin | Closed loop |
| $E = 0$, $\lambda < 0$ | Trapped in one well | Two separate loops |
| High $E$ | Wide oscillation (anharmonic) | Larger closed loop |

*$U_{max}$ applies to double-well case ($\lambda < 0$): $U_{max} = k^2/(16\lambda)$ at $x = \pm\sqrt{-k/(4\lambda)}$

---

### 10.5 Interactive Visualization

➡️ **[Open full simulation → vis_p10_nonlinear.html](vis_p10_nonlinear.html)**

The simulation includes:
- Adjustable parameters $k$, $\lambda$, $m$, and initial conditions $x_0$, $v_0$
- Real-time plot of $x(t)$
- Phase portrait $(x, v)$ with energy level curves
- Comparison between harmonic ($\lambda = 0$) and anharmonic regimes

---

*End of Problem Set 3 Solutions*

---

> **GitHub:** See `README.md` for repository setup instructions and how to render this document with math support.
