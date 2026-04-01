# Problem 2 – Inclined Plane with Friction

**Given:** Mass $m$, angle $\alpha$, kinetic friction coefficient $\mu$

---

## 2.1 Forces Acting on the Body

Using axes along (x) and perpendicular to (y) the incline:

| Force | Along incline | Perpendicular to incline |
|---|---|---|
| Gravity component | $mg\sin\alpha$ (down the slope) | $-mg\cos\alpha$ |
| Normal force $N$ | $0$ | $+N$ |
| Friction $f = \mu N$ | $-\mu mg\cos\alpha$ (up the slope) | $0$ |

Equilibrium perpendicular to incline: $N = mg\cos\alpha$

---

## 2.2 Acceleration

Newton's second law along the incline (down the slope = positive):

$$
ma = mg\sin\alpha - \mu mg\cos\alpha
$$

$$
\boxed{a = g(\sin\alpha - \mu\cos\alpha)}
$$

For motion to occur: $\tan\alpha > \mu$

---

## 2.3 Time of Descent from Height $h$

Length of slope: $L = h/\sin\alpha$. Starting from rest ($v_0 = 0$):

$$
L = \tfrac{1}{2}a t^2 \implies \boxed{t = \sqrt{\frac{2h}{g\sin\alpha(\sin\alpha - \mu\cos\alpha)}}}
$$

---

## 2.4 Final Velocity

$$
v = at = \sqrt{2aL} \implies \boxed{v = \sqrt{\frac{2gh(\sin\alpha - \mu\cos\alpha)}{\sin\alpha}}}
$$

---

## 2.5 Energy Balance Check

Energy lost to friction: $W_f = \mu mg\cos\alpha \cdot \dfrac{h}{\sin\alpha} = \mu mgh\cot\alpha$

By energy conservation:

$$
mgh = \tfrac{1}{2}mv^2 + W_f \implies v^2 = \frac{2gh(\sin\alpha - \mu\cos\alpha)}{\sin\alpha} \quad \checkmark
$$

**Consistent with the kinematic result.** ✅
