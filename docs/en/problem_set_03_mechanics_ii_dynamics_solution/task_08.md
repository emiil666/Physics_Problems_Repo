# Problem 8 – Harmonic Oscillator

**Given:** $m\ddot{x} + kx = 0$

---

## 8.1 Solution

Characteristic equation $m\lambda^2 + k = 0$ gives $\lambda = \pm i\omega_0$:

$$
\boxed{x(t) = A\cos(\omega_0 t) + B\sin(\omega_0 t)} = C\cos(\omega_0 t + \phi)
$$

where $C = \sqrt{A^2 + B^2}$ is the amplitude and $\phi$ is the phase.

---

## 8.2 Natural Frequency

$$
\boxed{\omega_0 = \sqrt{\frac{k}{m}}\ \mathrm{[rad/s]}}, \qquad T = \frac{2\pi}{\omega_0}\ \mathrm{[s]}
$$

The period $T$ is **independent of amplitude** (isochronous oscillation).

---

## 8.3 Energy as a Function of Time

$$
T(t) = \tfrac{1}{2}m\dot{x}^2 = \tfrac{1}{2}kC^2\sin^2(\omega_0 t + \phi)
$$

$$
U(t) = \tfrac{1}{2}kx^2 = \tfrac{1}{2}kC^2\cos^2(\omega_0 t + \phi)
$$

$$
\boxed{E = T + U = \tfrac{1}{2}kC^2 = \text{const}}
$$

---

## 8.4 Energy Conservation Proof

$$
\frac{dE}{dt} = \dot{x}(m\ddot{x} + kx) = \dot{x}\cdot 0 = 0 \quad \checkmark
$$

---

## 8.5 Phase Space Interpretation

In the phase plane $(x, p)$ with $p = m\dot{x}$:

$$
\frac{x^2}{C^2} + \frac{p^2}{(m\omega_0 C)^2} = 1
$$

This is an **ellipse** — the trajectory is closed and periodic (no dissipation).

➡️ [Open phase space animation → vis_p8_oscillator.html](vis_p8_oscillator.html)
