# Problem 6 – 2D Electric Field Map
## Electrostatics: Three Charges in a Plane

---

## Step 1 – Electric Field Vector $\vec{E}(x, y)$

The electric field at point $\mathbf{r} = (x, y)$ due to a point charge $q_i$ located at $\mathbf{r}_i = (x_i, y_i)$ is:

$$\vec{E}_i(x, y) = \frac{q_i}{4\pi\varepsilon_0} \cdot \frac{\mathbf{r} - \mathbf{r}_i}{|\mathbf{r} - \mathbf{r}_i|^3}$$

By the **superposition principle**, the total field is:

$$\vec{E}(x, y) = \sum_{i=1}^{N} \vec{E}_i(x, y) = \frac{1}{4\pi\varepsilon_0} \sum_{i=1}^{N} \frac{q_i\,(x - x_i,\ y - y_i)}{\left[(x-x_i)^2 + (y-y_i)^2\right]^{3/2}}$$


## Step 2 – Vector Field Map

To visualize $\vec{E}(x,y)$, we sample the field on a regular grid $(x_j, y_k)$ and draw **arrows** whose:
- **Direction** follows $\vec{E}$
- **Length** is proportional to $\log(1 + |\vec{E}|)$ (logarithmic scaling prevents singularities from dominating)
- **Color** encodes field magnitude (blue = weak, red = strong)

Additionally, **electric field lines** are drawn by integrating the ODE:
$$\frac{d\mathbf{r}}{ds} = \frac{\vec{E}(\mathbf{r})}{|\vec{E}(\mathbf{r})|}$$

starting from points near each charge using the 4th-order Runge–Kutta method.

---

## Step 3 – Finding the Equilibrium Point Numerically

An **equilibrium point** is a location where $\vec{E}(x, y) = \vec{0}$, i.e., both components vanish simultaneously.

**Method: 2D gradient descent / Newton-Raphson**

We minimize $|\vec{E}|^2 = E_x^2 + E_y^2$ using gradient descent:

$$\mathbf{r}_{n+1} = \mathbf{r}_n - \eta \,\nabla|\vec{E}|^2$$

Or more efficiently, use the **Jacobian** (matrix of partial derivatives) and Newton's method:

$$\begin{pmatrix} \Delta x \\ \Delta y \end{pmatrix} = -\mathbf{J}^{-1} \begin{pmatrix} E_x \\ E_y \end{pmatrix}$$

where:
$$\mathbf{J} = \begin{pmatrix} \partial E_x/\partial x & \partial E_x/\partial y \\ \partial E_y/\partial x & \partial E_y/\partial y \end{pmatrix}$$

The partial derivatives for a single charge $q_i$ at $(x_i, y_i)$:

$$\frac{\partial E_x}{\partial x} = kq_i \frac{r^2 - 3(x-x_i)^2}{r^5}, \quad \frac{\partial E_x}{\partial y} = kq_i \frac{-3(x-x_i)(y-y_i)}{r^5}$$

**Practical approach:** scan the grid for sign changes in $E_x$ and $E_y$, then refine with Newton iterations.

---

## Step 4 – Stability Analysis (Small Displacement)

At an equilibrium point $\mathbf{r}_0$, linearize the field:

$$\vec{E}(\mathbf{r}_0 + \delta\mathbf{r}) \approx \mathbf{J}(\mathbf{r}_0)\,\delta\mathbf{r}$$

A test **positive** charge placed at the equilibrium experiences force $\vec{F} = q\vec{E}$. The motion satisfies:

$$m\ddot{\delta\mathbf{r}} = q\,\mathbf{J}(\mathbf{r}_0)\,\delta\mathbf{r}$$

The stability is determined by the **eigenvalues** $\lambda$ of $\mathbf{J}$:
- $\lambda < 0$ (real, negative): restoring force → **stable** in that direction
- $\lambda > 0$ (real, positive): repulsive force → **unstable** (saddle or source)
- Complex $\lambda$: oscillatory behavior

**Earnshaw's Theorem** states that a stable 3D electrostatic equilibrium is impossible for a free charge in vacuum. In 2D cross-sections, saddle points (stable in one direction, unstable in another) are the typical outcome.

Note: $\text{tr}(\mathbf{J}) = \nabla \cdot \vec{E} = \rho/\varepsilon_0 = 0$ in free space, so the eigenvalues sum to zero — confirming that if one direction is stable, the other must be unstable.

---

## Step 5 – Comparison: Two Charges vs. Three Charges

| Property | Two Charges (opposite) | Two Charges (same) | Three Charges |
|----------|------------------------|---------------------|---------------|
| Equilibrium exists? | On perpendicular bisector (saddle) | On line between them | Depends on configuration |
| Number of equilibria | 1 | 1 (unstable, on axis) | 1–3 (depends on $q_i$, positions) |
| Field line topology | Dipole pattern | Two lobes | More complex, asymmetric |
| Stability | Saddle (Earnshaw) | Unstable | Saddle (Earnshaw still applies) |

**For two equal charges $+q$:** equilibrium at the midpoint; stable perpendicular to the axis, unstable along the axis.

**For two opposite charges $\pm q$:** no equilibrium in free space (field lines go from $+$ to $-$ everywhere).

**For three charges:** additional equilibria can appear between charges depending on signs and magnitudes. The topology of field lines becomes richer, with possible **X-type saddle points** between groups of same-sign charges.

---

## Summary

| Task | Method |
|------|--------|
| Field calculation | Coulomb superposition |
| Visualization | Grid arrows + field line integration (RK4) |
| Equilibrium finding | Grid scan + Newton–Raphson refinement |
| Stability | Jacobian eigenvalue analysis |
| Field line topology | Runge–Kutta integration from source points |