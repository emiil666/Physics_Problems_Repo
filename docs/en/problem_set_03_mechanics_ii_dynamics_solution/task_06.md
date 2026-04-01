# Problem 6 – Motion with Linear Drag

**Given:** $F = -kv$, $v(0) = v_0$, $x(0) = 0$

---

## 6.1 Equation of Motion and Solution

$$
m\dot{v} = -kv \implies \frac{dv}{v} = -\frac{k}{m}dt
$$

Integrating:

$$
\boxed{v(t) = v_0\,e^{-t/\tau}}, \quad \tau = \frac{m}{k}
$$

Integrating again for position:

$$
\boxed{x(t) = \frac{mv_0}{k}\left(1 - e^{-kt/m}\right)}
$$

---

## 6.2 Limiting Behaviour as $t \to \infty$

$$
\lim_{t\to\infty} v(t) = 0, \qquad \lim_{t\to\infty} x(t) = \frac{mv_0}{k}
$$

The body **asymptotically comes to rest** after traveling a total distance $x_\infty = mv_0/k$.

---

## 6.3 Comparison with Drag-Free Motion

| Quantity | No drag | With drag |
|---|---|---|
| $v(t)$ | $v_0$ (constant) | $v_0 e^{-kt/m}$ (decays) |
| $x(t)$ | $v_0 t$ (unbounded) | $\frac{mv_0}{k}(1-e^{-kt/m})$ (bounded) |
| $x(\infty)$ | $\infty$ | $\frac{mv_0}{k}$ (finite) |

For small $t$: $x(t) \approx v_0 t - \frac{kv_0}{2m}t^2 + \ldots$ — the quadratic term represents the drag effect.

➡️ [Open interactive graph → vis_p6_drag.html](vis_p6_drag.html)
