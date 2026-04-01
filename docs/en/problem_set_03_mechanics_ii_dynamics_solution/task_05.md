# Problem 5 – Momentum and One-Dimensional Elastic Collision

**Given:** Masses $m_1$, $m_2$ with initial velocities $u_1$, $u_2$; elastic collision

---

## 5.1 Conservation Laws

**Conservation of momentum:**

$$
m_1 u_1 + m_2 u_2 = m_1 v_1 + m_2 v_2 \tag{1}
$$

**Conservation of kinetic energy (elastic):**

$$
\tfrac{1}{2}m_1 u_1^2 + \tfrac{1}{2}m_2 u_2^2 = \tfrac{1}{2}m_1 v_1^2 + \tfrac{1}{2}m_2 v_2^2 \tag{2}
$$

---

## 5.2 Velocities After Collision

Solving the system (1) & (2):

$$
\boxed{v_1 = \frac{m_1 - m_2}{m_1 + m_2}u_1 + \frac{2m_2}{m_1 + m_2}u_2}
$$

$$
\boxed{v_2 = \frac{2m_1}{m_1 + m_2}u_1 + \frac{m_2 - m_1}{m_1 + m_2}u_2}
$$

**Key identity used:** In an elastic collision the relative velocity reverses sign: $(u_1 - u_2) = -(v_1 - v_2)$

---

## 5.3 Special Case: $m_1 = m_2$

$$
v_1 = u_2, \qquad v_2 = u_1
$$

**The two bodies exchange velocities.** If $u_2 = 0$, body 1 stops completely and body 2 moves off with $u_1$.

---

## 5.4 Limit $m_2 \gg m_1$ (massive wall)

$$
v_1 \approx -u_1 + 2u_2, \qquad v_2 \approx u_2
$$

If the wall is at rest ($u_2 = 0$): $v_1 = -u_1$ — the light body **bounces back** with the same speed.

---

## 5.5 Physical Interpretation

| Scenario | Result | Intuition |
|---|---|---|
| Equal masses | Velocities exchange | Maximum momentum transfer |
| $m_2 \gg m_1$ | Light body reverses, heavy barely moves | Wall reflection |
| $m_1 \gg m_2$ | Heavy barely slows, light launched at $\approx 2u_1$ | Slingshot effect |
