# Problem 4 – Conservation of Energy (Free Fall)

**Given:** Body falls from height $h$, no air resistance, $g = 9.81\ \mathrm{m/s^2}$

---

## 4.1 Total Energy

Taking ground as reference level ($U = 0$ at $y = 0$):

$$
U(y) = mgy, \qquad T(y) = \tfrac{1}{2}mv^2(y)
$$

$$
\boxed{E = T + U = \tfrac{1}{2}mv^2 + mgy = mgh = \text{const}}
$$

At height $h$: $v = 0$, so $E = mgh$. Energy is conserved throughout the fall.

---

## 4.2 Velocity as a Function of Height

From $E = mgh$:

$$
\tfrac{1}{2}mv^2 + mgy = mgh \implies \boxed{v(y) = \sqrt{2g(h-y)}}
$$

At ground ($y = 0$): $v = \sqrt{2gh}$.

---

## 4.3 Comparison with Newton's Second Law

From kinematics with constant acceleration $g$, falling from rest over distance $h$:

$$
v^2 = 2gh \quad \checkmark
$$

Both approaches give the same result — energy conservation is derived from Newton's second law for conservative forces.

---

## 4.4 Height Where $T = 0.75\,E$

$$
T = 0.75\,E \implies mgy = 0.25\,E = 0.25\,mgh
$$

$$
\boxed{y^* = 0.25\,h}
$$

At one quarter of the initial height, kinetic energy accounts for 75% of total energy.

➡️ [Open interactive energy visualization → vis_p4_energy.html](vis_p4_energy.html)
