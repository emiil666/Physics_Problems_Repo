# Problem 7 – Vertical Throw with Drag

**Given:** $m\dfrac{dv}{dt} = -mg - kv$, $v(0) = v_0 > 0$, $x(0) = 0$ (upward positive)

---

## 7.1 Solution of the ODE

Let $v_t = mg/k$ (terminal velocity magnitude) and $\tau = m/k$:

$$
\boxed{v(t) = \left(v_0 + v_t\right)e^{-t/\tau} - v_t}
$$

Position (integrating):

$$
\boxed{x(t) = \left(v_0 + v_t\right)\tau\left(1 - e^{-t/\tau}\right) - v_t\,t}
$$

---

## 7.2 Maximum Height

At maximum height $v(t^*) = 0$:

$$
t^* = \tau\ln\left(1 + \frac{v_0}{v_t}\right)
$$

$$
\boxed{h_{max} = v_0\tau - v_t\tau\ln\left(1 + \frac{v_0}{v_t}\right)}
$$

---

## 7.3 Comparison with No-Drag Case

Without drag: $h_{max}^{(0)} = \dfrac{v_0^2}{2g}$

**Drag always reduces the maximum height.**

---

## 7.4 Numerical Simulation (Euler Method)

$$
v_{n+1} = v_n + \Delta t\cdot\frac{-mg - kv_n}{m}, \qquad x_{n+1} = x_n + v_n\Delta t
$$

---

## 7.5 Analytical vs Numerical Comparison

The Euler method introduces first-order errors $O(\Delta t)$. For smaller $\Delta t$ the numerical solution converges to the analytical one.

➡️ [Open interactive simulation → vis_p7_throw.html](vis_p7_throw.html)
