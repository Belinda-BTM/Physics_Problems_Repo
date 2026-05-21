# Problem Set 6 – Solutions
## Electromagnetism II: Magnetism, Induction, and Electrodynamics

---

## Problem 1 – Lorentz Force

**Given:**
$$\vec{B} = (0, 0, 1)\ \text{T}, \quad \vec{v} = (2, 3, 0)\ \text{m/s}, \quad q = 1\ \text{mC} = 10^{-3}\ \text{C}$$

---

### (a) Lorentz Force $\vec{F}$

The magnetic Lorentz force is:
$$\vec{F} = q\,\vec{v} \times \vec{B}$$


---

### (b) Equation of Motion

Newton's second law:
$$m\ddot{\vec{r}} = q\dot{\vec{r}} \times \vec{B}$$

With $\vec{B} = B\hat{z}$, the $z$-component is decoupled. For motion in the $xy$-plane:

$$m\ddot{x} = qB\dot{y}$$
$$m\ddot{y} = -qB\dot{x}$$

Define the cyclotron frequency $\omega_c = \frac{qB}{m}$.

Let $w = \dot{x} + i\dot{y}$. Then $\dot{w} = -i\omega_c w$, giving $w(t) = w_0 e^{-i\omega_c t}$.

With $\vec{v}_0 = (2, 3, 0)\ \text{m/s}$:
$$w_0 = 2 + 3i, \quad w(t) = (2+3i)e^{-i\omega_c t}$$

Integrating (with initial position at origin):
$$x(t) = \frac{1}{\omega_c}\left[3 - 3\cos(\omega_c t) + 2\sin(\omega_c t)\right] + 0$$
$$y(t) = \frac{1}{\omega_c}\left[-2 + 2\cos(\omega_c t) + 3\sin(\omega_c t)\right] + 0$$

The particle moves in a **circle** (uniform circular motion in the $xy$-plane).

---

### (c) Magnitude $|\vec{F}|$

$$|\vec{F}| = q|\vec{v} \times \vec{B}| = q\sqrt{3^2 + (-2)^2} = 10^{-3}\sqrt{13}\ \text{N}$$

$$\boxed{|\vec{F}| = \sqrt{13} \times 10^{-3}\ \text{N} \approx 3.61\ \text{mN}}$$

---

### (d) Does the Magnetic Force Do Work?

**No.** The magnetic force is always perpendicular to the velocity:
$$P = \vec{F} \cdot \vec{v} = q(\vec{v} \times \vec{B}) \cdot \vec{v} = 0$$

The magnetic force changes the *direction* of motion but never the *speed* or *kinetic energy*.

---

### (e) Radius of Trajectory ($m = 0.01\ \text{kg}$)

The radius of circular motion (cyclotron radius):
$$r = \frac{mv_\perp}{qB}$$

where $v_\perp = |\vec{v}_\perp| = \sqrt{v_x^2 + v_y^2} = \sqrt{4+9} = \sqrt{13}\ \text{m/s}$

$$\boxed{r = \frac{0.01 \cdot \sqrt{13}}{10^{-3} \cdot 1} = 10\sqrt{13} \approx 36.1\ \text{m}}$$

---

### (f) Effect of Doubling $B$

From $r = \frac{mv_\perp}{qB}$, we see $r \propto \frac{1}{B}$.

$$\boxed{r' = \frac{r}{2} \approx 18.0\ \text{m}}$$

Doubling $B$ **halves** the radius.

---

## Problem 2 – Velocity Selector (Crossed Fields)

**Given:**
$$\vec{E} = (0, E, 0), \quad \vec{B} = (0, 0, B)$$

---

### (a) Condition for Rectilinear Motion

For a particle moving with velocity $\vec{v} = v\hat{x}$, the total force is:
$$\vec{F} = q(\vec{E} + \vec{v} \times \vec{B}) = q(E\hat{y} + v\hat{x} \times B\hat{z}) = q(E\hat{y} - vB\hat{y})$$

For rectilinear (undeflected) motion, $\vec{F} = 0$:
$$qE = qvB \implies \boxed{v_d = \frac{E}{B}}$$

---

### (b) Drift Velocity for $E = 400\ \text{V/m}$, $B = 0.8\ \text{T}$

$$\boxed{v_d = \frac{400}{0.8} = 500\ \text{m/s}}$$

---

### (c) Does Kinetic Energy Change?

**No.** In steady (rectilinear) motion the net force is zero, so the particle is unaccelerated. The speed — and thus kinetic energy — remains constant.

---

### (d) Operating Principle

The velocity selector allows only particles with the exact speed $v_d = E/B$ to pass through undeflected. Faster particles are deflected in one direction (magnetic force dominates), slower particles in the opposite direction (electric force dominates). This principle is used in **mass spectrometers** and **electron guns** to produce monoenergetic beams.

---

## Problem 3 – Magnetic Moment of a Loop

**Given:** $N$ turns, area $S$, current $I$, uniform field $\vec{B}$.

---

### (a) Magnetic Moment $\vec{\mu}$

$$\boxed{\vec{\mu} = NI\vec{S} = NIS\,\hat{n}}$$

where $\hat{n}$ is the unit normal to the loop (direction given by the right-hand rule with the current).

---

### (b) Torque $\vec{M}$

$$\boxed{\vec{M} = \vec{\mu} \times \vec{B} = NIS\,(\hat{n} \times \vec{B})}$$

In magnitude: $M = NIS B \sin\theta$, where $\theta$ is the angle between $\vec{\mu}$ and $\vec{B}$.

---

### (c) Angle for Maximum Torque

$$M = NISB\sin\theta \implies \text{maximum when } \sin\theta = 1, \text{ i.e., } \theta = 90°$$

The torque is maximum when $\vec{\mu} \perp \vec{B}$ (the loop plane contains $\vec{B}$).

---

### (d) Potential Energy $U$

$$\boxed{U = -\vec{\mu} \cdot \vec{B} = -NISB\cos\theta}$$

---

### (e) Stable and Unstable Positions


## Problem 4 – Rotating Loop (Induction)

**Given:** Area $S$, $N$ turns, field $\vec{B}$, angular velocity $\omega$.

---

### (a) Magnetic Flux $\Phi(t)$

The angle between $\hat{n}$ and $\vec{B}$ changes as $\omega t$:
$$\boxed{\Phi(t) = NBS\cos(\omega t)}$$

---

### (b) Induced EMF $\mathcal{E}(t)$

By Faraday's law:
$$\boxed{\mathcal{E}(t) = -\frac{d\Phi}{dt} = NBS\omega\sin(\omega t) = \mathcal{E}_0\sin(\omega t)}$$

---

### (c) Amplitude $\mathcal{E}_0$

$$\boxed{\mathcal{E}_0 = NBS\omega}$$

---

### (d) Dependence on $\omega$

The amplitude is **directly proportional** to $\omega$. Doubling the rotation speed doubles the EMF amplitude.

---

### (e) Mechanism of EMF Generation

As the loop rotates, the flux through it changes sinusoidally. By Faraday's law, a changing flux induces an EMF. At the microsopic level, the free electrons in the rotating conductor experience a motional force $q\vec{v} \times \vec{B}$ (where $\vec{v}$ is the velocity due to rotation), which drives current. This is the fundamental principle of **AC generators**.

---

## Problem 5 – Induction in a Moving Rod

**Given:** $L = 0.25\ \text{m}$, $v = 4\ \text{m/s}$, $B = 0.6\ \text{T}$ (perpendicular to motion and rod).

---

### (a) Induced EMF

$$\boxed{\mathcal{E} = BLv = 0.6 \times 0.25 \times 4 = 0.6\ \text{V}}$$

---

### (b) Potential Difference Between Ends

The motional EMF drives charge separation along the rod. The potential difference between the ends equals:
$$\boxed{\Delta V = \mathcal{E} = BLv = 0.6\ \text{V}}$$

---

### (c) Non-Perpendicular Motion

If the velocity makes an angle $\alpha$ with the direction perpendicular to both the rod and $\vec{B}$:
$$\mathcal{E} = BLv\sin\alpha$$

Only the component of velocity perpendicular to the rod contributes. If motion is parallel to the rod, $\mathcal{E} = 0$.

---

### (d) Dependence on $L$

$$\mathcal{E} = BLv \implies \mathcal{E} \propto L$$

The EMF is **directly proportional** to the length of the rod.

---

### (e) Source of Energy

The energy stored in the electric field (which drives the current) comes from the **mechanical work** done by the external agent that maintains the rod's motion against the magnetic braking force. Ultimately, kinetic energy is converted to electrical energy.

---

## Problem 6 – Rod on Rails in a $\vec{B}$ Field

**Given:**
$$m = 0.20\ \text{kg},\quad L = 0.30\ \text{m},\quad B = 0.80\ \text{T},\quad R = 0.50\ \Omega,\quad \alpha = 25°,\quad g = 9.81\ \text{m/s}^2$$

---

### (a) Motional EMF and Current

$$\boxed{\mathcal{E}(v) = BLv = 0.80 \times 0.30 \times v = 0.24v\ \text{V}}$$

$$\boxed{I(v) = \frac{\mathcal{E}}{R} = \frac{0.24v}{0.50} = 0.48v\ \text{A}}$$

---

### (b) Magnetic Braking Force

The current-carrying rod in field $\vec{B}$ experiences a force opposing motion (Lenz's law):
$$\boxed{F_{\text{brake}} = BIL = B \cdot \frac{BLv}{R} \cdot L = \frac{B^2L^2}{R}v}$$



$$F_{\text{brake}} = 0.1152\,v\ \text{N}$$

---

### (c) Equation of Motion Along the Incline

Taking down the incline as positive:
$$m\dot{v} = mg\sin\alpha - \frac{B^2L^2}{R}v$$

$$\boxed{m\dot{v} = mg\sin\alpha - kv, \quad k = \frac{B^2L^2}{R}}$$

This is a **first-order linear ODE** with damping proportional to $v$ — analogous to a body falling through a viscous fluid.

---

### (d) Terminal Velocity $v_\infty$

At terminal velocity $\dot{v} = 0$:
$$mg\sin\alpha = \frac{B^2L^2}{R}v_\infty$$

$$\boxed{v_\infty = \frac{mgR\sin\alpha}{B^2L^2} = \frac{0.20 \times 9.81 \times 0.50 \times \sin 25°}{(0.80)^2(0.30)^2}}$$

$$v_\infty = \frac{0.20 \times 9.81 \times 0.50 \times 0.4226}{0.0576} \approx \frac{0.4135}{0.0576} \approx 7.18\ \text{m/s}$$

---

### (e) Power Balance in Steady State

At $v = v_\infty$, the net force is zero. The gravitational power input equals:
$$P_{\text{grav}} = mg\sin\alpha \cdot v_\infty$$

The Joule heating power:
$$P_{\text{Joule}} = I^2 R = \left(\frac{BLv_\infty}{R}\right)^2 R = \frac{B^2L^2v_\infty^2}{R}$$

Since $v_\infty = \frac{mgR\sin\alpha}{B^2L^2}$, substituting:
$$P_{\text{Joule}} = \frac{B^2L^2v_\infty}{R} \cdot v_\infty = mg\sin\alpha \cdot v_\infty = P_{\text{grav}}\ \checkmark$$

All gravitational energy is converted to Joule heat (no kinetic energy change in steady state).

---

## Problem 7 – Loop Pulled into a $B$ Field Region

**Given:**
$$a = 0.20\ \text{m},\quad b = 0.10\ \text{m},\quad B = 0.60\ \text{T},\quad R = 0.40\ \Omega,\quad v = 1.5\ \text{m/s}$$

---

### (a) Flux $\Phi(t)$ During Entry Phase

Let $x(t) = vt$ be the length of loop already inside the field ($0 \leq x \leq a$):
$$\boxed{\Phi(t) = B \cdot b \cdot x(t) = Bbvt}$$

---

### (b) Induced EMF and Current

$$\mathcal{E} = -\frac{d\Phi}{dt} = -Bbv$$

$$\boxed{|\mathcal{E}| = Bbv = 0.60 \times 0.10 \times 1.5 = 0.09\ \text{V}}$$

$$\boxed{I = \frac{\mathcal{E}}{R} = \frac{0.09}{0.40} = 0.225\ \text{A}}$$

The current direction opposes the increase in flux (Lenz's law).

---

### (c) Braking Force $F(v)$

$$\boxed{F = BIb = B \cdot \frac{Bbv}{R} \cdot b = \frac{B^2b^2}{R}v}$$

$$F = \frac{(0.60)^2(0.10)^2}{0.40} \times 1.5 = \frac{0.0036}{0.40} \times 1.5 = 0.009 \times 1.5 = 0.0135\ \text{N}$$

---

### (d) Mechanical Power = Thermal Power

Mechanical power supplied to maintain constant $v$:
$$P_{\text{mech}} = F \cdot v = \frac{B^2b^2v^2}{R} = \frac{(0.60)^2(0.10)^2(1.5)^2}{0.40} = \frac{0.0081}{0.40} = 0.02025\ \text{W}$$

Thermal (Joule) power:
$$P_{\text{Joule}} = I^2R = (0.225)^2 \times 0.40 = 0.050625 \times 0.40 = 0.02025\ \text{W}\ \checkmark$$

---

### (e) Current When Loop is Entirely Inside

When the loop is **completely inside** the uniform field, the flux is constant:
$$\Phi = B \cdot a \cdot b = \text{const} \implies \mathcal{E} = -\frac{d\Phi}{dt} = 0 \implies \boxed{I = 0}$$

No EMF is induced because there is no change in flux.

---

## Problem 8 – Self-Induction (RL Circuit)

**Given:**
$$L = 0.20\ \text{H},\quad R = 5.0\ \Omega,\quad U = 12\ \text{V}$$

---

### (a) Steady Current $I_0$

In steady state, $\frac{dI}{dt} = 0$, so the coil acts as a pure resistor:
$$\boxed{I_0 = \frac{U}{R} = \frac{12}{5.0} = 2.4\ \text{A}}$$

---

### (b) Current After Disconnection: $I(t)$, $\tau$, $U_L(t)$

After disconnection, the circuit equation is:
$$L\frac{dI}{dt} + RI = 0 \implies \frac{dI}{dt} = -\frac{R}{L}I$$

**Solution:**
$$\boxed{I(t) = I_0\,e^{-t/\tau}}$$

**Time constant:**
$$\boxed{\tau = \frac{L}{R} = \frac{0.20}{5.0} = 0.04\ \text{s} = 40\ \text{ms}}$$

**Voltage across the coil:**
$$\boxed{U_L(t) = L\frac{dI}{dt} = -RI_0\,e^{-t/\tau} = -12\,e^{-t/0.04}\ \text{V}}$$

(The magnitude equals $U_0 = 12\ \text{V}$ at $t=0$ and decays exponentially.)

---

### (c) Stored Energy Before Disconnection

$$\boxed{W = \frac{1}{2}LI_0^2 = \frac{1}{2} \times 0.20 \times (2.4)^2 = 0.10 \times 5.76 = 0.576\ \text{J}}$$

---

### (d) Energy Dissipated as Joule Heat

Total heat dissipated:
$$Q = \int_0^{\infty} I^2(t)\,R\,dt = \int_0^{\infty} I_0^2 e^{-2t/\tau} R\,dt = I_0^2 R \cdot \frac{\tau}{2} = I_0^2 R \cdot \frac{L}{2R} = \frac{1}{2}LI_0^2 = W\ \checkmark$$

All stored magnetic energy is converted into Joule heat. $\boxed{Q = W = 0.576\ \text{J}}$

---

### (e) Overvoltage at Disconnection

When the current is suddenly interrupted, $\frac{dI}{dt}$ becomes very large (ideally infinite). Since $U_L = L\frac{dI}{dt}$, the induced voltage across the coil spikes to a very high value — potentially many times the supply voltage. This **overvoltage** (back-EMF spike) can damage switches and insulation. In practice, a **freewheeling diode** or **snubber circuit** is used to provide a path for the current and limit the voltage spike.

---

## Problem 9 – Ideal vs. Real Transformer

### How a Transformer Works

A transformer consists of two coils (primary and secondary) wound on a common ferromagnetic core. An alternating current in the primary coil creates a time-varying magnetic flux in the core, which induces an EMF in the secondary coil (Faraday's law).

**Origin of the secondary voltage:** The changing flux $\Phi(t)$ created by the primary is shared with the secondary (mutual induction):
$$\mathcal{E}_2 = -N_2\frac{d\Phi}{dt}, \quad \mathcal{E}_1 = -N_1\frac{d\Phi}{dt}$$

$$\boxed{\frac{U_2}{U_1} = \frac{N_2}{N_1} = n \quad \text{(turns ratio)}}$$

### Ideal Transformer Properties

- No core losses (no hysteresis, no eddy currents)
- No winding resistance
- Perfect flux linkage (no leakage flux)
- Power is fully conserved: $U_1 I_1 = U_2 I_2$

$$\frac{I_1}{I_2} = \frac{N_2}{N_1} = n$$

### Real Transformer — Losses

| Loss Type | Cause | Mitigation |
|-----------|-------|------------|
| **Copper losses** ($I^2R$) | Winding resistance | Thicker wire |
| **Iron losses (eddy currents)** | Induced currents in core | Laminated core |
| **Hysteresis losses** | Magnetic domain reversal | Soft magnetic materials (Si-Fe) |
| **Leakage flux** | Flux not fully coupled | Better core geometry |

### Typical Values

- **Turns ratio:** from $n \approx 0.01$ (step-down, e.g. 230 V → 5 V) to $n \approx 100$ (step-up)
- **Efficiency:** large power transformers reach $\eta = 98\text{–}99\%$; small transformers $\eta \approx 80\text{–}95\%$

---

## Problem 10 – Eddy Currents

### Braking Using Eddy Currents

When a conducting material moves through a magnetic field, induced currents (eddy currents) flow in closed loops within the material. By Lenz's law, these currents produce a force that **opposes the motion** — a braking effect.

**Applications of eddy current braking:**
- Magnetic brakes in rail vehicles and roller coasters (smooth, wear-free)
- Dynamometers for measuring engine power
- Coin validators in vending machines
- Induction cooktops (heating via eddy currents)
- Dampers in weighing scales and galvanometers

### Advantages and Disadvantages

| Advantages | Disadvantages |
|-----------|---------------|
| No mechanical contact → no wear | Force depends on velocity (no braking at standstill) |
| Smooth, silent operation | Energy dissipated as heat |
| Self-regulating (more force at higher speed) | Requires strong magnets or high conductivity |
| No maintenance required | Less effective at low speeds |

### Best Materials for Eddy Currents

Materials with **high electrical conductivity** generate the strongest eddy currents:
- **Copper** (best conductor, $\sigma \approx 5.8 \times 10^7\ \text{S/m}$)
- **Aluminium** (good conductor, lightweight)
- **Silver** (highest conductivity, but expensive)

Ferromagnetic materials (iron, steel) combine eddy currents with hysteresis losses, but their higher resistivity limits eddy current braking efficiency.

### How to Increase the Braking Force

1. **Increase $B$** — force $\propto B^2$
2. **Use higher conductivity material** — larger induced currents
3. **Increase the relative velocity** — force $\propto v$
4. **Increase the area of the conductor** exposed to the field
5. **Use multiple magnets** or a longer magnetic region
6. **Reduce the thickness of the conductor** to concentrate currents (or conversely, use a solid thick piece for maximum eddy current loops)