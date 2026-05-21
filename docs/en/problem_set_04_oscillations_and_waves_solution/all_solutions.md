# Problem Set 4 – Solutions
## Oscillations and Waves: Dynamical Systems and Propagation of Disturbances

---

## Problem 1 – Harmonic Motion: Motion Parameters

**Given:** $x(t) = A\cos(\omega t + \varphi)$

### 1. Period and frequency

$$
T = \frac{2\pi}{\omega}, \qquad f = \frac{1}{T} = \frac{\omega}{2\pi}
$$

### 2. Maximum velocity and acceleration

Differentiating:

$$
v(t) = \dot{x}(t) = -A\omega\sin(\omega t + \varphi) \implies v_{\max} = A\omega
$$

$$
a(t) = \ddot{x}(t) = -A\omega^2\cos(\omega t + \varphi) \implies a_{\max} = A\omega^2
$$

### 3. Numerical case: $A = 0.2\ \text{m}$, $f = 2\ \text{Hz}$

$$
\omega = 2\pi f = 2\pi \cdot 2 = 4\pi \approx 12.57\ \text{rad/s}
$$

$$
v_{\max} = A\omega = 0.2 \cdot 4\pi \approx 2.51\ \text{m/s}
$$

$$
a_{\max} = A\omega^2 = 0.2 \cdot (4\pi)^2 \approx 31.6\ \text{m/s}^2
$$

**Interpretation:** The velocity is 90° ahead of position in phase. The acceleration is always directed toward the equilibrium and proportional to displacement, which is the defining property of SHM.

---

## Problem 2 – Energy of a Harmonic Oscillator

**Given:** $m=1\ \text{kg}$, $k=100\ \text{N/m}$, $x(0)=2\ \text{m}$, $v(0)=1\ \text{m/s}$

### 1. Natural frequency

$$
\omega_0 = \sqrt{\frac{k}{m}} = \sqrt{\frac{100}{1}} = 10\ \text{rad/s}, \qquad f_0 = \frac{10}{2\pi} \approx 1.59\ \text{Hz}
$$

### 2. Total energy

$$
E = \frac{1}{2}mv^2(0) + \frac{1}{2}kx^2(0) = \frac{1}{2}(1)(1)^2 + \frac{1}{2}(100)(2)^2 = 0.5 + 200 = 200.5\ \text{J}
$$

### 3. Displacement where $T = 50\%\,E$

$$
T = 0.5E \implies U = 0.5E \implies \frac{1}{2}kx^2 = \frac{1}{2}E
$$

$$
x = \sqrt{\frac{E}{k}} = \sqrt{\frac{200.5}{100}} \approx 1.415\ \text{m}
$$

---

## Problem 3 – Harmonic Wave

**Given:** $y(x,t) = A\sin(kx - \omega t)$

### 1. Wavelength

$$
\lambda = \frac{2\pi}{k}
$$

### 2. Phase velocity

A point of constant phase satisfies $kx - \omega t = \text{const}$, so:

$$
\boxed{v_{\text{ph}} = \frac{\omega}{k} = \lambda f}
$$

### 3. Numerical: $k = 4\pi\ \text{rad/m}$, $\omega = 20\pi\ \text{rad/s}$

$$
v_{\text{ph}} = \frac{20\pi}{4\pi} = 5\ \text{m/s}, \qquad \lambda = \frac{2\pi}{4\pi} = 0.5\ \text{m}
$$

### 4. Phase comparison of $x = \lambda$ vs $x = 0$

$$
y(0, t) = A\sin(-\omega t), \quad y(\lambda, t) = A\sin(k\lambda - \omega t) = A\sin(2\pi - \omega t) = A\sin(-\omega t)
$$

Yes — the two points oscillate **in phase** (differ by exactly $2\pi$). This is the definition of wavelength.

---

## Problem 4 – Wave Equation

**Given:** $y(x,t) = A\cos(kx - \omega t)$

### 1. Verification

$$
\frac{\partial^2 y}{\partial t^2} = -\omega^2 A\cos(kx - \omega t)
$$

$$
\frac{\partial^2 y}{\partial x^2} = -k^2 A\cos(kx - \omega t)
$$

Substituting into the wave equation $\partial^2 y/\partial t^2 = v^2\,\partial^2 y/\partial x^2$:

$$
-\omega^2 A\cos(\cdots) = v^2 \cdot (-k^2 A\cos(\cdots))
$$

This is satisfied if and only if:

$$
\boxed{v = \frac{\omega}{k}}
$$

### 2. Dispersion relation

The wave equation implies a **linear dispersion relation** $\omega = vk$, meaning the phase velocity is independent of frequency — the medium is **non-dispersive**.

---

## Problem 5 – Superposition of Waves, Beats, and Group Velocity

**Given:** $y_1 = A\sin(kx - \omega t)$, $y_2 = A\sin(kx - (\omega + \Delta\omega)t)$

### 1. Resultant wave (product form)

Using sum-to-product: $\sin\alpha + \sin\beta = 2\cos\!\left(\frac{\alpha-\beta}{2}\right)\sin\!\left(\frac{\alpha+\beta}{2}\right)$

$$
y = y_1 + y_2 = 2A\cos\!\left(\frac{\Delta\omega}{2}\,t\right)\sin\!\left(kx - \left(\omega + \frac{\Delta\omega}{2}\right)t\right)
$$

$$
\boxed{y = \underbrace{2A\cos\!\left(\frac{\Delta\omega}{2}\,t\right)}_{\text{envelope (slow)}}\cdot\underbrace{\sin\!\left(kx - \left(\omega + \tfrac{\Delta\omega}{2}\right)t\right)}_{\text{carrier (fast)}}}
$$

### 2. Beat frequency and period (at $x = 0$)

The envelope oscillates at $\Delta\omega/2$, but the amplitude repeats at twice that rate (absolute value):

$$
f_{\text{beat}} = \frac{\Delta\omega}{2\pi} = \Delta f, \qquad T_{\text{beat}} = \frac{1}{\Delta f} = \frac{2\pi}{\Delta\omega}
$$

### 3. Physical interpretation

- **Carrier wave:** oscillates at the average frequency $\bar{\omega} = \omega + \Delta\omega/2$ — this is what you "hear" as the tone.
- **Envelope:** modulates amplitude slowly at frequency $\Delta\omega/(2\pi)$ — this is the periodic "wah-wah" loudness variation heard as beats.
- **Group velocity:** $v_g = d\omega/dk$ (the speed at which the envelope — and thus energy — travels).

---

## Problem 6 – Damped Oscillator

**Equation:** $m\ddot{x} + b\dot{x} + kx = 0$

Define $\gamma = b/(2m)$ (damping coefficient), $\omega_0 = \sqrt{k/m}$ (natural frequency).

The characteristic equation: $r^2 + 2\gamma r + \omega_0^2 = 0 \implies r = -\gamma \pm \sqrt{\gamma^2 - \omega_0^2}$

### Cases

**Underdamped** ($\gamma < \omega_0$, i.e. $b < 2\sqrt{km}$):

$$
\omega_d = \sqrt{\omega_0^2 - \gamma^2}, \qquad x(t) = e^{-\gamma t}(C_1\cos\omega_d t + C_2\sin\omega_d t)
$$

Oscillates with exponentially decaying amplitude.

**Critically damped** ($\gamma = \omega_0$, i.e. $b = 2\sqrt{km}$):

$$
x(t) = (C_1 + C_2 t)\,e^{-\gamma t}
$$

Fastest return to equilibrium without oscillation.

**Overdamped** ($\gamma > \omega_0$, i.e. $b > 2\sqrt{km}$):

$$
r_{1,2} = -\gamma \pm \sqrt{\gamma^2 - \omega_0^2} \in \mathbb{R}, \qquad x(t) = C_1 e^{r_1 t} + C_2 e^{r_2 t}
$$

Slow return to equilibrium, no oscillation.

---

## Problem 7 – Forced Oscillator and Resonance

**Equation:** $m\ddot{x} + b\dot{x} + kx = F_0\cos(\Omega t)$

### Steady-state amplitude

The particular solution is $x_p(t) = C(\Omega)\cos(\Omega t - \delta)$ where:

$$
\boxed{C(\Omega) = \frac{F_0/m}{\sqrt{(\omega_0^2 - \Omega^2)^2 + (2\gamma\Omega)^2}}}
$$

### Phase shift

$$
\tan\delta = \frac{2\gamma\Omega}{\omega_0^2 - \Omega^2}
$$

### Resonance

Amplitude is maximized when $\frac{dC}{d\Omega} = 0$, giving:

$$
\Omega_{\text{res}} = \sqrt{\omega_0^2 - 2\gamma^2}
$$

For small damping $\gamma \ll \omega_0$: $\Omega_{\text{res}} \approx \omega_0$, and $C_{\max} \approx \frac{F_0}{2m\gamma\omega_0} = \frac{F_0 Q}{k}$ where $Q = \omega_0/(2\gamma)$ is the quality factor.

---

## Problem 8 – Two Coupled Springs

**Setup:** masses $m_1, m_2$ connected by springs $k_1, k_2, k_3$ in series (wall-$k_1$-$m_1$-$k_2$-$m_2$-$k_3$-wall).

### Equations of motion

$$
m_1\ddot{x}_1 = -k_1 x_1 - k_2(x_1 - x_2), \qquad m_2\ddot{x}_2 = -k_2(x_2 - x_1) - k_3 x_2
$$

Matrix form:

$$
\mathbf{M}\ddot{\vec{x}} + \mathbf{K}\vec{x} = 0, \quad \mathbf{M} = \begin{pmatrix}m_1&0\\0&m_2\end{pmatrix}, \quad \mathbf{K} = \begin{pmatrix}k_1+k_2 & -k_2\\-k_2 & k_2+k_3\end{pmatrix}
$$

### Normal mode frequencies

For $m_1 = m_2 = m$, $k_1 = k_3 = k$, $k_2 = k_c$ (coupling spring):

$$
\omega_{\pm}^2 = \frac{(2k + k_c) \pm k_c}{m} \implies \omega_- = \sqrt{\frac{k}{m}},\quad \omega_+ = \sqrt{\frac{k + 2k_c}{m}}
$$

**Mode shapes:**

- $\omega_-$: both masses move **in phase** (symmetric mode)
- $\omega_+$: masses move **out of phase** (antisymmetric mode)

---

## Problem 9 – Chain of $N$ Springs

**Equations of motion** for mass $i$ ($1 \le i \le N$):

$$
m\ddot{x}_i = k(x_{i+1} - x_i) - k(x_i - x_{i-1}) = k(x_{i+1} - 2x_i + x_{i-1})
$$

This is the **discrete wave equation**. In the long-wavelength limit ($\lambda \gg a$, lattice spacing):

$$
\frac{\partial^2 x}{\partial t^2} = \frac{ka^2}{m}\frac{\partial^2 x}{\partial s^2} \implies v_{\text{wave}} = a\sqrt{\frac{k}{m}}
$$

The dispersion relation is: $\omega(q) = 2\sqrt{k/m}\,\left|\sin\!\left(\frac{qa}{2}\right)\right|$

For small $q$: $\omega \approx v_{\text{wave}}\,q$ (linear, non-dispersive).

---

## Problem 10 – Double Pendulum and Deterministic Chaos

### Coordinates

$$
x_1 = l_1\sin\theta_1, \quad y_1 = -l_1\cos\theta_1
$$

$$
x_2 = x_1 + l_2\sin\theta_2, \quad y_2 = y_1 - l_2\cos\theta_2
$$

### Equations of motion (standard Lagrangian derivation)

Let $M = m_1 + m_2$. The coupled ODEs for $(\theta_1, \theta_2)$ are:

$$
\ddot{\theta}_1 = \frac{-m_2 l_2\dot\theta_2^2\sin(\theta_1-\theta_2) - (m_1+m_2)g\sin\theta_1 - m_2 l_1\dot\theta_1^2\sin(\theta_1-\theta_2)\cos(\theta_1-\theta_2) + m_2 g\sin\theta_2\cos(\theta_1-\theta_2)}{l_1(m_1+m_2) - m_2 l_1\cos^2(\theta_1-\theta_2)}
$$

(and similarly for $\ddot\theta_2$ — see code for the full RK4 implementation.)

### Chaos and sensitivity to initial conditions

- For small angles: nearly integrable, predictable.
- For large angles: the Lyapunov exponent $\lambda > 0$ means trajectories diverge exponentially as $\delta\theta \sim e^{\lambda t}$.
- With 50 copies perturbed by $\delta\theta_2 \sim 10^{-4}$–$10^{-2}$: at first all trajectories are indistinguishable; after a finite time they spread into fully independent orbits — this is the hallmark of **deterministic chaos**.
