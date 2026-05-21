# Problem Set 3 – Solutions
## Mechanics II: Dynamics and Energy

---

## Problem 1 – Newton's Second Law (Constant Force)

**Given:** $m = 2\ \text{kg}$, $\vec{F} = (6, 2)\ \text{N}$, $\vec{v}(0) = (1, -1)\ \text{m/s}$, $\vec{r}(0) = (0, 0)$

### Acceleration

By Newton's second law $\vec{F} = m\vec{a}$:

$$
\vec{a} = \frac{\vec{F}}{m} = \frac{(6,\ 2)}{2} = (3,\ 1)\ \text{m/s}^2
$$

### Velocity

$$
\vec{v}(t) = \vec{v}(0) + \vec{a}\,t = (1 + 3t,\ -1 + t)
$$

### Position

$$
\vec{r}(t) = \vec{r}(0) + \vec{v}(0)\,t + \tfrac{1}{2}\vec{a}\,t^2 = \left(t + \tfrac{3}{2}t^2,\ -t + \tfrac{1}{2}t^2\right)
$$

### Work done at $t = 3\ \text{s}$

Using the work-energy theorem $W = \Delta E_k$:

$$
\vec{v}(3) = (1+9,\ -1+3) = (10,\ 2)\ \text{m/s}
$$

$$
E_k(0) = \tfrac{1}{2} \cdot 2 \cdot (1^2 + 1^2) = 2\ \text{J}
$$

$$
E_k(3) = \tfrac{1}{2} \cdot 2 \cdot (100 + 4) = 104\ \text{J}
$$

$$
\boxed{W = \Delta E_k = 104 - 2 = 102\ \text{J}}
$$

**Verification via direct calculation:**

$$
\vec{r}(3) = (3 + 13.5,\ -3 + 4.5) = (16.5,\ 1.5)\ \text{m}
$$

$$
W = \vec{F} \cdot \vec{r}(3) = 6 \cdot 16.5 + 2 \cdot 1.5 = 99 + 3 = 102\ \text{J} \checkmark
$$

---

## Problem 2 – Inclined Plane with Friction

**Setup:** mass $m$, angle $\alpha$, kinetic friction $\mu$, height $h$.

### Forces acting on the body

- Gravity component along slope: $F_{\parallel} = mg\sin\alpha$ (down the slope)
- Normal force: $N = mg\cos\alpha$
- Friction force: $F_f = \mu N = \mu mg\cos\alpha$ (up the slope, opposing motion)

### Acceleration

Applying Newton's second law along the slope:

$$
ma = mg\sin\alpha - \mu mg\cos\alpha
$$

$$
\boxed{a = g(\sin\alpha - \mu\cos\alpha)}
$$

For motion to occur we need $\tan\alpha > \mu$.

### Time of descent from height $h$

The length of the slope: $L = h/\sin\alpha$. Starting from rest ($v_0 = 0$):

$$
L = \tfrac{1}{2}at^2 \implies t = \sqrt{\frac{2L}{a}} = \sqrt{\frac{2h}{a\sin\alpha}}
$$

$$
\boxed{t = \sqrt{\frac{2h}{g\sin\alpha(\sin\alpha - \mu\cos\alpha)}}}
$$

### Final velocity

$$
\boxed{v = at = \sqrt{2aL} = \sqrt{2gh\,\frac{\sin\alpha - \mu\cos\alpha}{\sin\alpha}}}
$$

### Energy balance check

Work by gravity: $W_g = mgh$

Work by friction: $W_f = -\mu mg\cos\alpha \cdot L = -\mu mgh\cot\alpha \cdot \sin\alpha = -\mu mgh\cos\alpha/\sin\alpha \cdot \sin\alpha= -\mu mg h \frac{\cos\alpha}{\sin\alpha}\cdot \sin\alpha$

$$
W_f = -\mu mgh \frac{\cos\alpha}{\sin\alpha}
$$

Kinetic energy gained:

$$
\tfrac{1}{2}mv^2 = mgh\left(1 - \frac{\mu\cos\alpha}{\sin\alpha}\right) = W_g + W_f \checkmark
$$

---

## Problem 3 – Work of a Variable Force

**Given:** $F(x) = -kx$

### Equation of motion and solution

$$
m\ddot{x} = -kx \implies \ddot{x} + \omega_0^2 x = 0, \quad \omega_0 = \sqrt{\frac{k}{m}}
$$

General solution:

$$
x(t) = A\cos(\omega_0 t) + B\sin(\omega_0 t)
$$

This is **simple harmonic motion**.

### Work from $0$ to $x_0$

$$
W = \int_0^{x_0} F(x)\,dx = \int_0^{x_0} (-kx)\,dx = -\frac{1}{2}kx_0^2
$$

### Potential energy

The work done against the force equals the stored potential energy:

$$
\boxed{U(x) = \frac{1}{2}kx^2}
$$

### Verification: $F = -dU/dx$

$$
-\frac{dU}{dx} = -\frac{d}{dx}\left(\frac{1}{2}kx^2\right) = -kx = F(x) \checkmark
$$

---

## Problem 4 – Conservation of Energy (Free Fall)

**Setup:** body falls from height $h$, no air resistance. Taking ground as $U = 0$.

### Total energy

$$
E = T + U = \frac{1}{2}mv^2 + mgh = \text{const} = mgh_0
$$

### Velocity as a function of height

$$
\frac{1}{2}mv^2 = mg(h_0 - h) \implies \boxed{v(h) = \sqrt{2g(h_0 - h)}}
$$

This matches the kinematic result from Newton's second law directly.

### Height where $T = 0.75\,E$

$$
T = 0.75\,E \implies mgh = 0.25\,E = 0.25\,mgh_0
$$

$$
\boxed{h = \frac{h_0}{4}}
$$

---

## Problem 5 – Elastic Collision (1D)

**Conservation laws:**

$$
m_1 v_1 + m_2 v_2 = m_1 v_1' + m_2 v_2' \quad \text{(momentum)}
$$

$$
\frac{1}{2}m_1 v_1^2 + \frac{1}{2}m_2 v_2^2 = \frac{1}{2}m_1 v_1'^2 + \frac{1}{2}m_2 v_2'^2 \quad \text{(energy)}
$$

### General solution

$$
\boxed{v_1' = \frac{m_1 - m_2}{m_1 + m_2}v_1 + \frac{2m_2}{m_1 + m_2}v_2}
$$

$$
\boxed{v_2' = \frac{2m_1}{m_1 + m_2}v_1 + \frac{m_2 - m_1}{m_1 + m_2}v_2}
$$

### Case $m_1 = m_2$

$$
v_1' = v_2, \quad v_2' = v_1
$$

The bodies **exchange velocities** — a well-known billiard-ball result.

### Limit $m_2 \gg m_1$ (with $v_2 = 0$)

$$
v_1' \approx -v_1, \quad v_2' \approx 0
$$

The light body **bounces back** with the same speed; the heavy body barely moves (e.g., ball hitting a wall).

---

## Problem 6 – Motion with Linear Drag

**Equation of motion:** $m\dot{v} = -kv$

### Solution

Separable ODE:

$$
\frac{dv}{v} = -\frac{k}{m}\,dt \implies \ln v = -\frac{k}{m}t + C
$$

$$
\boxed{v(t) = v_0\,e^{-k t/m}}
$$

Position (integrating):

$$
\boxed{x(t) = \frac{mv_0}{k}\left(1 - e^{-kt/m}\right)}
$$

### Limit $t \to \infty$

$$
\lim_{t\to\infty} v(t) = 0, \qquad \lim_{t\to\infty} x(t) = \frac{mv_0}{k}
$$

The body **stops at a finite distance** $x_\infty = mv_0/k$.

### Comparison with drag-free motion

Without drag: $v(t) = v_0$ (constant), $x(t) = v_0 t$ (unbounded).

With drag: exponential decay, finite stopping distance.

---

## Problem 7 – Vertical Throw with Drag

**Equation of motion:** $m\dot{v} = -mg - kv$, $v(0) = v_0 > 0$

### Solution

Define the terminal velocity $v_t = mg/k$. The equation becomes:

$$
m\dot{v} = -k(v + v_t)
$$

Separating variables:

$$
\frac{dv}{v + v_t} = -\frac{k}{m}\,dt
$$

$$
\boxed{v(t) = (v_0 + v_t)\,e^{-kt/m} - v_t}
$$

Position:

$$
\boxed{x(t) = \frac{m}{k}(v_0 + v_t)\left(1 - e^{-kt/m}\right) - v_t\,t}
$$

### Maximum height

At $v(t_{\max}) = 0$:

$$
t_{\max} = \frac{m}{k}\ln\!\left(1 + \frac{v_0}{v_t}\right)
$$

$$
x_{\max} = \frac{m}{k}\left[v_0 - v_t\ln\!\left(1 + \frac{v_0}{v_t}\right)\right]
$$

### Comparison without drag

Without drag: $x_{\max} = v_0^2/(2g)$. With drag: always smaller, since energy is dissipated by friction.

---

## Problem 8 – Harmonic Oscillator

**Equation of motion:** $m\ddot{x} + kx = 0$

### Solution

$$
\boxed{x(t) = A\cos(\omega_0 t + \varphi)}, \quad \omega_0 = \sqrt{\frac{k}{m}}
$$

where $A$ and $\varphi$ are determined by initial conditions.

### Natural frequency

$$
f_0 = \frac{\omega_0}{2\pi} = \frac{1}{2\pi}\sqrt{\frac{k}{m}}
$$

### Energy as a function of time

$$
T(t) = \frac{1}{2}m\dot{x}^2 = \frac{1}{2}m\omega_0^2 A^2\sin^2(\omega_0 t + \varphi) = \frac{1}{2}kA^2\sin^2(\omega_0 t + \varphi)
$$

$$
U(t) = \frac{1}{2}kx^2 = \frac{1}{2}kA^2\cos^2(\omega_0 t + \varphi)
$$

$$
E = T + U = \frac{1}{2}kA^2\bigl[\sin^2 + \cos^2\bigr] = \frac{1}{2}kA^2 = \text{const} \checkmark
$$

### Phase space

In the $(x, v)$ plane, the trajectory is an **ellipse**:

$$
\frac{x^2}{A^2} + \frac{v^2}{(A\omega_0)^2} = 1
$$

Energy is constant along this ellipse — each orbit corresponds to a fixed $E = \frac{1}{2}kA^2$.

---

## Problem 9 – Potential and Conservative Field

**Given:** $U(x,y) = \frac{k}{2}(x^2 + y^2)$

### Force from gradient

$$
\vec{F} = -\nabla U = -\left(\frac{\partial U}{\partial x},\ \frac{\partial U}{\partial y}\right) = (-kx,\ -ky) = -k\vec{r}
$$

This is a **central restoring force** (2D harmonic oscillator).

### Equations of motion

$$
m\ddot{x} = -kx, \qquad m\ddot{y} = -ky
$$

### Type of motion

Both coordinates oscillate independently at the same frequency $\omega_0 = \sqrt{k/m}$:

$$
x(t) = A\cos(\omega_0 t + \varphi_x), \qquad y(t) = B\cos(\omega_0 t + \varphi_y)
$$

The trajectory is in general an **ellipse** (or circle if $A = B$, $\Delta\varphi = \pi/2$) — a **Lissajous figure** with equal frequencies.

### Total energy

$$
E = \frac{1}{2}m(\dot{x}^2 + \dot{y}^2) + \frac{k}{2}(x^2 + y^2) = \frac{1}{2}kA^2 + \frac{1}{2}kB^2 = \text{const}
$$

---

## Problem 10 – Numerical Model: Anharmonic Oscillator

**Potential:** $U(x) = \frac{k}{2}x^2 + \lambda x^4$

### Force

$$
F(x) = -\frac{dU}{dx} = -kx - 4\lambda x^3
$$

### Equation of motion

$$
m\ddot{x} = -kx - 4\lambda x^3
$$

This is a **nonlinear ODE** — no closed-form solution in general.

### Key observations

- For $\lambda = 0$: reduces to simple harmonic oscillator.
- For $\lambda > 0$: the restoring force is stronger than linear → **stiffer** potential, higher frequency for larger amplitudes.
- For $\lambda < 0$ (with $k > 0$): double-well potential if $\lambda < -k^2/(8|x_0|^2)$; can exhibit bounded or unbounded motion depending on energy.

### Phase portrait interpretation

The phase portrait $(x, \dot{x})$ shows:
- **Closed orbits** (ellipses for $\lambda=0$, deformed for $\lambda \neq 0$) for bounded motion.
- **Separatrix** (saddle-point orbit) for the double-well case separating libration from rotation.
- The period of oscillation **increases with amplitude** for $\lambda > 0$.
