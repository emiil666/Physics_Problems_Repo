# Problem 3 – Work of a Variable Force

**Given:** $F(x) = -kx$ (Hooke's Law / spring force)

---

## 3.1 Equation of Motion and Solution

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

## 3.2 Work Done from $0$ to $x_0$

$$
W = \int_0^{x_0} F(x)\,dx = \int_0^{x_0} (-kx)\,dx = \boxed{-\frac{1}{2}kx_0^2}
$$

The negative sign means the spring force does **negative work** when the body moves away from equilibrium.

---

## 3.3 Interpretation as Potential Energy

$$
W = -\Delta U \implies U(0) = 0 \implies \boxed{U(x) = \frac{1}{2}kx^2}
$$

This is the **elastic potential energy** stored in the spring.

---

## 3.4 Verification: $F = -\dfrac{dU}{dx}$

$$
-\frac{dU}{dx} = -\frac{d}{dx}\left(\frac{1}{2}kx^2\right) = -kx = F(x) \quad \checkmark
$$

---

## 3.5 Graphs of $F(x)$ and $U(x)$

➡️ [Open interactive graph → vis_p3_spring.html](vis_p3_spring.html)

Key features:
- $F(x) = -kx$: linear, negative slope $-k$, passes through origin
- $U(x) = \tfrac{1}{2}kx^2$: upward parabola, minimum at $x = 0$
- The force always points toward the minimum of potential energy (restoring force)
