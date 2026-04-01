# Problem 1 – Newton's Second Law (Constant Force)

**Given:** $m = 2\ \mathrm{kg}$, $\vec{F} = (6,\ 2)\ \mathrm{N}$, $\vec{v}(0) = (1,\ -1)\ \mathrm{m/s}$, $\vec{r}(0) = (0,0)\ \mathrm{m}$

---

## 1.1 Acceleration $\vec{a}(t)$

From Newton's second law $\vec{F} = m\vec{a}$:

$$
\vec{a} = \frac{\vec{F}}{m} = \frac{(6,\ 2)}{2} = (3,\ 1)\ \mathrm{m/s^2}
$$

Since the force is constant, the acceleration is **constant** and independent of time.

---

## 1.2 Velocity $\vec{v}(t)$

Integrating acceleration with initial condition $\vec{v}(0) = (1,\ -1)$:

$$
\vec{v}(t) = \vec{v}(0) + \vec{a}\,t = (1 + 3t,\quad -1 + t)\ \mathrm{m/s}
$$

---

## 1.3 Position $\vec{r}(t)$

Integrating velocity with initial condition $\vec{r}(0) = (0, 0)$:

$$
\vec{r}(t) = \vec{r}(0) + \vec{v}(0)\,t + \tfrac{1}{2}\vec{a}\,t^2 = \left(\frac{3}{2}t^2 + t,\quad \frac{1}{2}t^2 - t\right)\ \mathrm{m}
$$

Explicitly:

$$
x(t) = \tfrac{3}{2}t^2 + t, \qquad y(t) = \tfrac{1}{2}t^2 - t
$$

---

## 1.4 Trajectory

Eliminating $t$ from $x(t)$ and $y(t)$, the trajectory is a **parabola** in the $xy$-plane (uniformly accelerated 2D motion always produces a parabolic path).

➡️ [Open interactive trajectory animation → vis_p1_trajectory.html](vis_p1_trajectory.html)

---

## 1.5 Work Done by the Force at $t = 3\ \mathrm{s}$

$$
W = \vec{F} \cdot \Delta\vec{r} = \vec{F} \cdot [\vec{r}(3) - \vec{r}(0)]
$$

$$
\vec{r}(3) = \left(\tfrac{3}{2}\cdot 9 + 3,\quad \tfrac{1}{2}\cdot 9 - 3\right) = (16.5,\ 1.5)\ \mathrm{m}
$$

$$
W = (6,2)\cdot(16.5,\ 1.5) = 99 + 3 = \boxed{102\ \mathrm{J}}
$$

---

## 1.6 Verification with the Work-Energy Theorem

$W = \Delta KE = \tfrac{1}{2}m v^2(3) - \tfrac{1}{2}m v^2(0)$

$$
\vec{v}(3) = (10,\ 2)\ \mathrm{m/s}
$$

$$
\Delta KE = \tfrac{1}{2}\cdot 2\cdot(100+4) - \tfrac{1}{2}\cdot 2\cdot(1+1) = 104 - 2 = 102\ \mathrm{J} \quad \checkmark
$$

**Result is consistent with the work-energy theorem.** ✅
