# Problem 9 – Potential and Conservative Field

**Given:** $U(x,y) = \dfrac{k}{2}(x^2 + y^2)$

---

## 9.1 Force as the Gradient of the Potential

$$
\vec{F} = -\nabla U = -\left(\frac{\partial U}{\partial x},\ \frac{\partial U}{\partial y}\right) = -(kx,\ ky)
$$

$$
\boxed{\vec{F}(x,y) = -k\vec{r}}
$$

This is an **isotropic 2D harmonic restoring force**, always pointing toward the origin.

---

## 9.2 Equations of Motion

$$
m\ddot{x} = -kx, \qquad m\ddot{y} = -ky
$$

Both equations are independent with the same natural frequency $\omega_0 = \sqrt{k/m}$.

---

## 9.3 Type of Motion

$$
x(t) = A_x\cos(\omega_0 t + \phi_x), \qquad y(t) = A_y\cos(\omega_0 t + \phi_y)
$$

Since both oscillations share the **same frequency**, the trajectory is a **Lissajous figure (1:1)** — in general an ellipse, or a circle if $A_x = A_y$ and $\Delta\phi = \pi/2$.

---

## 9.4 Total Energy

$$
E = \tfrac{1}{2}m(\dot{x}^2 + \dot{y}^2) + \tfrac{k}{2}(x^2 + y^2) = \tfrac{1}{2}k(A_x^2 + A_y^2) = \text{const}
$$

---

## 9.5 Geometric Interpretation

Equipotential surfaces: **concentric circles** $x^2 + y^2 = \text{const}$

Force vectors are perpendicular to these circles, pointing inward. Trajectories are ellipses inscribed within equipotential curves.

➡️ [Open 2D potential field app → vis_p9_field.html](vis_p9_field.html)
