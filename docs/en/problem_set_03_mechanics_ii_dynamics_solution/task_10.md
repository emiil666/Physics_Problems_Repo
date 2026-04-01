# Problem 10 – Numerical Model of a Dynamical System

**Given:** $U(x) = \dfrac{k}{2}x^2 + \lambda x^4$

---

## 10.1 Force

$$
\boxed{F(x) = -\frac{dU}{dx} = -kx - 4\lambda x^3}
$$

- $\lambda > 0$: always restoring (anharmonic oscillator)
- $\lambda < 0$, $k > 0$: double-well potential (bistable system)

---

## 10.2 Equation of Motion

$$
m\ddot{x} = -kx - 4\lambda x^3
$$

This is a **nonlinear ODE** — no closed-form solution in general.

---

## 10.3 Numerical Solution — Runge-Kutta 4 (RK4)

Rewrite as first-order system with $v = \dot{x}$:

$$
\dot{x} = v, \qquad \dot{v} = \frac{-kx - 4\lambda x^3}{m}
$$

RK4 update:

$$
y_{n+1} = y_n + \tfrac{1}{6}(k_1 + 2k_2 + 2k_3 + k_4)\Delta t
$$

RK4 is fourth-order accurate — much more precise than Euler for the same step size.

---

## 10.4 Effect of Initial Energy on Motion

| Energy vs barrier | Motion type | Phase portrait |
|---|---|---|
| Low $E$ | Bounded oscillation near origin | Closed loop |
| $E$ near barrier ($\lambda < 0$) | Trapped in one well | Two separate loops |
| High $E$ | Wide anharmonic oscillation | Larger closed loop |

Double-well barrier height: $U_{max} = \dfrac{k^2}{16|\lambda|}$ at $x = \pm\sqrt{\dfrac{k}{4|\lambda|}}$

---

## 10.5 Visualization

➡️ [Open full simulation → vis_p10_nonlinear.html](vis_p10_nonlinear.html)

The simulation includes:
- Adjustable parameters $k$, $\lambda$, $m$, initial conditions $x_0$, $v_0$
- Real-time plot of $x(t)$
- Phase portrait $(x, v)$ with energy level curves
- Preset buttons: harmonic, anharmonic, soft spring, double-well (low/high energy)
