# Problem Set 5 – Electromagnetism I: Field and Forces – Solutions

---

## Problem 1 – Potential and Energy

**Given:** $q = 4\ \mu\mathrm{C} = 4\times10^{-6}\ \mathrm{C}$, $k = 8.99\times10^9\ \mathrm{N\cdot m^2/C^2}$

### 1. Electric potential at $r = 0.3\ \mathrm{m}$

$$
V(r) = k\frac{q}{r} = \frac{8.99\times10^9 \cdot 4\times10^{-6}}{0.3} \approx \boxed{1.20\times10^5\ \mathrm{V}}
$$

### 2. Potential difference between $r_1 = 0.3\ \mathrm{m}$ and $r_2 = 0.6\ \mathrm{m}$

$$
\Delta V = kq\!\left(\frac{1}{r_1} - \frac{1}{r_2}\right) = 8.99\times10^9\cdot4\times10^{-6}\!\left(\frac{1}{0.3}-\frac{1}{0.6}\right)
$$

$$
= 35{,}960\cdot\frac{5}{3} \approx \boxed{5.99\times10^4\ \mathrm{V}}
$$

### 3. Work done moving $q_0 = 2\ \mu\mathrm{C}$ from $r_1$ to $r_2$

$$
W = q_0\,\Delta V = 2\times10^{-6}\cdot 59{,}933 \approx \boxed{0.120\ \mathrm{J}}
$$

The work is **positive** — the test charge moves away from the same-sign source charge, so the field does positive work.

### 4. Electric field from the derivative of the potential

$$
E(r) = -\frac{dV}{dr} = -\frac{d}{dr}\!\left(\frac{kq}{r}\right) = \frac{kq}{r^2}
$$

$$
E(0.3) = \frac{8.99\times10^9 \cdot 4\times10^{-6}}{(0.3)^2} = \frac{35{,}960}{0.09} \approx \boxed{3.99\times10^5\ \mathrm{N/C}}
$$

### 5. Comparison with Coulomb's law

Coulomb's law gives directly $E = k\,q/r^2$ — identical to step 4. $\checkmark$  
This confirms the fundamental relation $\vec{E} = -\nabla V$.

---

## Problem 2 – Coulomb's Force

**Given:**

$$
q_1 = 3\ \mu\mathrm{C},\quad q_2 = -5\ \mu\mathrm{C},\quad \vec{r}_1 = (0,0),\quad \vec{r}_2 = (0.4,\ 0.3)\ \mathrm{m}
$$

### 1. Force vector on $q_2$

Separation vector from $q_1$ to $q_2$:

$$
\vec{r}_{12} = \vec{r}_2 - \vec{r}_1 = (0.4,\ 0.3)\ \mathrm{m},\qquad r = \sqrt{0.4^2+0.3^2} = 0.5\ \mathrm{m}
$$

$$
\hat{r}_{12} = \frac{(0.4,\ 0.3)}{0.5} = (0.8,\ 0.6)
$$

$$
\vec{F} = k\frac{q_1 q_2}{r^2}\hat{r}_{12} = 8.99\times10^9\cdot\frac{(3\times10^{-6})(-5\times10^{-6})}{0.25}\cdot(0.8,\ 0.6)
$$

$$
\boxed{\vec{F} = (-0.431,\ -0.324)\ \mathrm{N}}
$$

The negative sign confirms the force is **attractive** (opposite charges), directed from $q_2$ toward $q_1$.

### 2. Magnitude

$$
|\vec{F}| = k\frac{|q_1||q_2|}{r^2} = 8.99\times10^9\cdot\frac{15\times10^{-12}}{0.25} \approx \boxed{0.539\ \mathrm{N}}
$$

### 3. Potential energy of the system

$$
U = k\frac{q_1 q_2}{r} = 8.99\times10^9\cdot\frac{-15\times10^{-12}}{0.5} \approx \boxed{-0.270\ \mathrm{J}}
$$

Negative energy confirms the charges are bound (attractive system).

### 4. Work to separate to $r_f = 2\ \mathrm{m}$

$$
W = U_f - U_i = kq_1q_2\!\left(\frac{1}{r_f}-\frac{1}{r_i}\right) = -13{,}485\!\left(\frac{1}{2}-\frac{1}{0.5}\right)
$$

$$
= -13{,}485\cdot(-1.5) \approx \boxed{+0.202\ \mathrm{J}}
$$

---

## Problem 3 – Field at a Point from a System of Charges

**Charges:** $+q$ at $(-a,0)$ and $+2q$ at $(a,0)$.

### 1. General field $\vec{E}(x,y)$

From $+q$ at $(-a,0)$:

$$
\vec{E}_1 = kq\,\frac{(x+a,\ y)}{\bigl[(x+a)^2+y^2\bigr]^{3/2}}
$$

From $+2q$ at $(a,0)$:

$$
\vec{E}_2 = 2kq\,\frac{(x-a,\ y)}{\bigl[(x-a)^2+y^2\bigr]^{3/2}}
$$

$$
\boxed{\vec{E}(x,y) = kq\left[\frac{(x+a,\,y)}{[(x+a)^2+y^2]^{3/2}}+\frac{2(x-a,\,y)}{[(x-a)^2+y^2]^{3/2}}\right]}
$$

**On the $y$-axis** ($x=0$):

$$
\vec{E}(0,y) = \frac{kq}{(a^2+y^2)^{3/2}}\bigl(-a,\ 3y\bigr)
$$

**On the $x$-axis** ($y=0$, away from singularities):

$$
E_x(x,0) = kq\left[\frac{\text{sgn}(x+a)}{(x+a)^2}+\frac{2\,\text{sgn}(x-a)}{(x-a)^2}\right],\qquad E_y = 0
$$

### 2. Condition for zero field

On the $x$-axis for $x < -a$ (both charges repel toward the left):

$$
\frac{kq}{(x+a)^2} = \frac{2kq}{(x-a)^2} \implies (x-a)^2 = 2(x+a)^2
$$

$$
x = -a\frac{\sqrt{2}+1}{\sqrt{2}-1} = -a(3+2\sqrt{2}) \approx -5.83a
$$

**On the $y$-axis:** $E_x = kq\cdot\frac{-a}{(a^2+y^2)^{3/2}} \neq 0$ for all $y\neq0$ — **no zero-field point on $y$-axis**.

### 3. Numerical evaluation

$a=0.2\ \mathrm{m}$, $y=0.3\ \mathrm{m}$, $q=2\ \mu\mathrm{C}$, at point $(0,0.3)$:

$$
(a^2+y^2)^{3/2} = (0.04+0.09)^{3/2} = (0.13)^{3/2} \approx 0.04686\ \mathrm{m^3}
$$

$$
\vec{E}(0,0.3) = \frac{8.99\times10^9\cdot2\times10^{-6}}{0.04686}(-0.2,\ 0.9) \approx \boxed{(-76{,}700,\ +345{,}300)\ \mathrm{N/C}}
$$

### 4. Limit $y \gg a$

$$
\vec{E}(0,y) \approx \frac{kq}{y^3}(-a,\ 3y)\xrightarrow{y\gg a}\frac{3kq}{y^2}\hat{j}
$$

At large distances the system looks like a single charge $3q$ — the dipole-like structure is invisible.

### 5. Zero field on $y$-axis?

**No.** The $x$-component $E_x = -kqa/(a^2+y^2)^{3/2}$ is always nonzero (both charges lie on the $x$-axis, their $x$-components do not cancel on the $y$-axis).

---

## Problem 4 – Motion of a Particle in a Uniform Field

**Given:**

$$
m=0.02\ \mathrm{kg},\quad q=10^{-3}\ \mathrm{C},\quad \vec{E}=(30,\ 100)\ \mathrm{N/C},\quad \vec{v}(0)=(20,\ 0),\quad \vec{r}(0)=(0,\ 0)
$$

### 1. Equations of motion — analytical solution

$$
\vec{a} = \frac{q\vec{E}}{m} = \frac{10^{-3}}{0.02}(30,\ 100) = (1.5,\ 5)\ \mathrm{m/s^2}
$$

$$
\boxed{x(t) = 20t + 0.75t^2}, \qquad \boxed{y(t) = 2.5t^2}
$$

$$
v_x(t) = 20+1.5t,\qquad v_y(t) = 5t
$$

### 2. Trajectory shape

Eliminating $t = \sqrt{y/2.5}$ from $x(t)$:

$$
x = 20\sqrt{0.4y} + 0.3y
$$

This is a **parabolic trajectory** — analogous to projectile motion, with acceleration in both directions.

### 3. Time to reach $v_y = 50\ \mathrm{m/s}$

$$
5t = 50 \implies \boxed{t = 10\ \mathrm{s}}
$$

### 4. Kinetic energy at $t = 0.05\ \mathrm{s}$

$$
v_x(0.05) = 20+1.5(0.05) = 20.075\ \mathrm{m/s},\qquad v_y(0.05) = 0.25\ \mathrm{m/s}
$$

$$
K = \tfrac{1}{2}mv^2 = \tfrac{1}{2}(0.02)(20.075^2+0.25^2) \approx \boxed{4.031\ \mathrm{J}}
$$

### 5. Energy balance check

$$
K_0 = \tfrac{1}{2}(0.02)(20^2) = 4.0\ \mathrm{J}
$$

$$
\vec{r}(0.05) = (1.00188,\ 0.00625)\ \mathrm{m}
$$

$$
W = q\vec{E}\cdot\vec{r} = 10^{-3}(30\cdot1.00188+100\cdot0.00625) = 0.031\ \mathrm{J}
$$

$$
K_0 + W = 4.0 + 0.031 = 4.031\ \mathrm{J} = K\;\checkmark
$$

---

## Problem 5 – Capacitor: Energy and Force

**Given:** $S=0.02\ \mathrm{m^2}$, $d=5\times10^{-3}\ \mathrm{m}$, $U=500\ \mathrm{V}$, $\varepsilon_0=8.854\times10^{-12}\ \mathrm{F/m}$

### 1. Capacitance

$$
C = \varepsilon_0\frac{S}{d} = 8.854\times10^{-12}\cdot\frac{0.02}{5\times10^{-3}} = \boxed{35.4\ \mathrm{pF}}
$$

### 2. Stored energy

$$
W = \tfrac{1}{2}CU^2 = \tfrac{1}{2}\cdot35.4\times10^{-12}\cdot(500)^2 \approx \boxed{4.43\ \mu\mathrm{J}}
$$

### 3. Electric field between the plates

$$
E = \frac{U}{d} = \frac{500}{5\times10^{-3}} = \boxed{1.0\times10^5\ \mathrm{V/m}}
$$

### 4. Energy density

$$
u = \tfrac{1}{2}\varepsilon_0 E^2 = \tfrac{1}{2}\cdot8.854\times10^{-12}\cdot10^{10} \approx \boxed{44.3\ \mathrm{mJ/m^3}}
$$

**Verification:** $W = u\cdot S\cdot d = 44.3\times10^{-3}\cdot0.02\cdot5\times10^{-3} = 4.43\ \mu\mathrm{J}\ \checkmark$

### 5. Attractive force between the plates

$$
F = u\cdot S = 44.3\times10^{-3}\cdot0.02 \approx \boxed{0.885\ \mathrm{mN}}
$$

Equivalently, from the energy method:

$$
F = -\frac{\partial W}{\partial d}\bigg|_U = \frac{\varepsilon_0 S U^2}{2d^2} = 0.885\ \mathrm{mN}\;\checkmark
$$

---

## Problem 6 – 2D Field Map

See **`problem6_field_map.html`** for the interactive visualization.

**Theory — field from $N$ charges:**

$$
\vec{E}(\vec{r}) = \sum_{i=1}^{N} k\frac{q_i(\vec{r}-\vec{r}_i)}{|\vec{r}-\vec{r}_i|^3}
$$

**Equilibrium point:** $\vec{r}^*$ where $\vec{E}(\vec{r}^*)=\vec{0}$, found by grid search minimizing $|\vec{E}|^2$.

**Stability (Earnshaw's theorem):** No stable electrostatic equilibrium exists in free space — the Laplacian of the potential satisfies $\nabla^2 V = 0$ (no charge), so no local minimum of $V$ can exist in free space.

---

## Problem 7 – Motion in a Central Field

**Equation of motion:**

$$
m\ddot{\vec{r}} = \frac{kqQ}{r^2}\hat{r},\qquad \text{let }\alpha = \frac{kqQ}{m}
$$

**Radial case** (1D, $\theta=\text{const}$):

$$
\ddot{r} = \frac{\alpha}{r^2}
$$

**Total energy:**

$$
E_{total} = \tfrac{1}{2}m(\dot{r}^2 + r^2\dot{\theta}^2) + \frac{kqQ}{r}
$$

| $E_{total}$ | Orbit type |
|---|---|
| $> 0$ | Unbound — particle escapes |
| $= 0$ | Parabolic — escape velocity |
| $< 0$ | Bound orbit (only for attractive force) |

**RK4 state vector** $\vec{u} = (x, y, v_x, v_y)$:

$$
\frac{d\vec{u}}{dt} = \left(v_x,\ v_y,\ \frac{\alpha x}{r^3},\ \frac{\alpha y}{r^3}\right)
$$

See **`problem7_central_field.html`** for the animated RK4 trajectory.

---

## Problem 8 – Energy of a Three-Charge System

### 1. Total potential energy

$$
U = k\left(\frac{q_1 q_2}{r_{12}} + \frac{q_1 q_3}{r_{13}} + \frac{q_2 q_3}{r_{23}}\right)
$$

### 2. Equilateral triangle, $q_1=q_2=q_3=q$, side $a$

All $r_{ij}=a$:

$$
\boxed{U = \frac{3kq^2}{a}}
$$

### 3. Flipping sign of $q_3 \to -q$

$$
U' = \frac{k}{a}(q^2 - q^2 - q^2) = -\frac{kq^2}{a}
$$

Energy drops from $+3kq^2/a$ to $-kq^2/a$ — the system becomes partially bound.

### 4. Minimum energy configuration

For two positive charges and one negative, the optimal configuration is an equilateral triangle. The negative charge sits equidistant from both positive ones, maximizing attractive interactions. Numerically minimize $U$ over the position of $q_3$ using gradient descent.

### 5. Stability

By **Earnshaw's theorem**, no free-space electrostatic equilibrium is stable. The minimum-energy configuration is a saddle point — stable in some directions, unstable in others. Physical confinement (e.g., crystal lattice constraints) is required for true stability.

---

## Problem 9 – Dipole in an External Field

**Setup:** charges $\pm q$ separated by $2\ell$, dipole moment $p = 2q\ell$, moment of inertia $I = 2m\ell^2$.

### 1. Torque

$$
\vec{\tau} = \vec{p}\times\vec{E}_0 \implies \boxed{\tau = pE_0\sin\theta}
$$

### 2. Potential energy

$$
\boxed{U(\theta) = -\vec{p}\cdot\vec{E}_0 = -pE_0\cos\theta}
$$

Minimum at $\theta=0$ (aligned), maximum at $\theta=\pi$ (anti-aligned).

### 3. Equation of angular motion

$$
I\ddot{\theta} = -pE_0\sin\theta \implies \boxed{2m\ell^2\ddot{\theta} = -pE_0\sin\theta}
$$

This is the **nonlinear pendulum equation**.

### 4. Linearization for small $\theta$

$$
\sin\theta \approx \theta \implies \ddot{\theta} = -\frac{pE_0}{2m\ell^2}\,\theta = -\omega_0^2\,\theta
$$

### 5. Harmonic oscillator analogy

$$
\boxed{\omega_0 = \sqrt{\frac{pE_0}{2m\ell^2}}},\qquad T = 2\pi\sqrt{\frac{2m\ell^2}{pE_0}}
$$

Exact analogy to a physical pendulum with $g \leftrightarrow pE_0/(m\ell)$.

---

## Problem 10 – Field Flux (Verification of Gauss's Law)

See **`problem10_gauss.html`** for the interactive visualization.

### 1. Definition

$$
\Phi_E = \oiint_S \vec{E}\cdot d\vec{A}
$$

### 2. Sphere around a point charge

$$
\Phi_E = k\frac{Q}{R^2}\cdot 4\pi R^2 = 4\pi kQ = \frac{Q}{\varepsilon_0}
$$

The flux is **independent of radius** — it depends only on the enclosed charge.

### 3. Discrete approximation

$$
\vec{r}_{ij} = R(\sin\theta_i\cos\phi_j,\ \sin\theta_i\sin\phi_j,\ \cos\theta_i),\qquad \Delta A_{ij} = R^2\sin\theta_i\,\Delta\theta\,\Delta\phi
$$

$$
\Phi_E \approx \sum_{i,j}\vec{E}(\vec{r}_{ij})\cdot\hat{r}_{ij}\,\Delta A_{ij}
$$

### 4. Convergence

The discretization error scales as $\mathcal{O}(1/N)$ for uniform grids. Doubling grid resolution halves the error.

### 5. Analytical result (for $Q=1\ \mu\mathrm{C}$)

$$
\boxed{\Phi_E = \frac{Q}{\varepsilon_0} = \frac{10^{-6}}{8.854\times10^{-12}} \approx 1.129\times10^5\ \mathrm{N\cdot m^2/C}}
$$

The visualization confirms this numerically for any sphere radius and any position of the charge inside the sphere.
