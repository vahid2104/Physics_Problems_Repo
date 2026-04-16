
---

# Problem 2 – Energy of a harmonic oscillator

A system with the following initial parameters is given:

$$
m=1\ \mathrm{kg}
$$

$$
k=100\ \mathrm{N/m}
$$

$$
x(0)=2\ \mathrm{m}
$$

$$
v(0)=1\ \mathrm{m/s}
$$

We need to determine:

* the natural frequency,
* the total energy of the system,
* for what displacement the kinetic energy is 50% of the total energy.

---

## 1. Natural frequency

For a mass–spring harmonic oscillator, the angular natural frequency is

$$
\omega_0=\sqrt{\frac{k}{m}}
$$

Now substitute the given values:

$$
\omega_0=\sqrt{\frac{100}{1}}
$$

$$
\omega_0=\sqrt{100}
$$

$$
\omega_0=10\ \mathrm{rad/s}
$$

Therefore, the **natural angular frequency** is

$$
\omega_0=10\ \mathrm{rad/s}
$$

If we also want the ordinary frequency in hertz, we use

$$
f=\frac{\omega_0}{2\pi}
$$

So

$$
f=\frac{10}{2\pi}=\frac{5}{\pi}\approx 1.59\ \mathrm{Hz}
$$

Therefore, the **natural frequency** is

$$
f\approx 1.59\ \mathrm{Hz}
$$

---

## 2. Total energy of the system

For a harmonic oscillator, the total mechanical energy is constant and is equal to

$$
E = E_k + E_p
$$

where:

* (E_k) is the kinetic energy,
* (E_p) is the elastic potential energy.

At the initial moment (t=0),

$$
E=\frac{1}{2}mv(0)^2+\frac{1}{2}kx(0)^2
$$

Now substitute the given values:

$$
E=\frac{1}{2}\cdot 1 \cdot 1^2+\frac{1}{2}\cdot 100 \cdot 2^2
$$

Compute each part separately.

### Initial kinetic energy

$$
E_k(0)=\frac{1}{2}\cdot 1\cdot 1^2=\frac{1}{2}=0.5\ \mathrm{J}
$$

### Initial potential energy

$$
E_p(0)=\frac{1}{2}\cdot 100\cdot 2^2
$$

$$
E_p(0)=50\cdot 4
$$

$$
E_p(0)=200\ \mathrm{J}
$$

### Total energy

$$
E=0.5+200
$$

$$
E=200.5\ \mathrm{J}
$$

Therefore, the **total energy of the system** is

$$
E=200.5\ \mathrm{J}
$$

---

## 3. Displacement for which kinetic energy is 50% of the total energy

We are told that the kinetic energy should be **50% of the total energy**.

That means

$$
E_k=\frac{1}{2}E
$$

Since the total energy is

$$
E=E_k+E_p
$$

if the kinetic energy is half of the total, then the potential energy must also be half of the total:

$$
E_p=\frac{1}{2}E
$$

For a spring,

$$
E_p=\frac{1}{2}kx^2
$$

So we set

$$
\frac{1}{2}kx^2=\frac{1}{2}E
$$

Now substitute the known values (k=100) and (E=200.5):

$$
\frac{1}{2}\cdot 100 , x^2=\frac{1}{2}\cdot 200.5
$$

$$
50x^2=100.25
$$

Now solve for (x^2):

$$
x^2=\frac{100.25}{50}
$$

$$
x^2=2.005
$$

Take the square root:

$$
x=\pm \sqrt{2.005}
$$

$$
x\approx \pm 1.416\ \mathrm{m}
$$

Therefore, the displacement at which the kinetic energy is 50% of the total energy is

$$
x\approx \pm 1.42\ \mathrm{m}
$$

---

## Interpretation

Let us explain what these results mean in a simple way.

### Natural frequency

The value

$$
\omega_0=10\ \mathrm{rad/s}
$$

tells us how fast the system would oscillate naturally if left to move freely.
Since the spring is quite stiff ((k=100\ \mathrm{N/m})) and the mass is small ((m=1\ \mathrm{kg})), the oscillation is relatively fast.

---

### Total energy

The total energy is

$$
E=200.5\ \mathrm{J}
$$

This energy stays constant during the motion, because in the ideal harmonic oscillator there is no friction or damping.

At the start:

* the spring is stretched a lot: (x(0)=2\ \mathrm{m}),
* the mass also has a small initial speed: (v(0)=1\ \mathrm{m/s}).

So most of the energy is stored in the spring as potential energy, and only a very small part is kinetic energy.

In fact:

$$
E_p(0)=200\ \mathrm{J}, \qquad E_k(0)=0.5\ \mathrm{J}
$$

So initially the energy is almost entirely elastic potential energy.

---

### Why the displacement is smaller than 2 m

We found that when kinetic energy is half of the total energy,

$$
x\approx \pm 1.42\ \mathrm{m}
$$

This makes sense, because:

* at the extreme positions of motion, the displacement is largest and the speed is smallest,
* near the center, the displacement is smaller and the speed is larger.

When the mass moves from (x=2\ \mathrm{m}) toward the center, some spring potential energy changes into kinetic energy.
At the point where the kinetic energy reaches half of the total, the remaining half is still stored in the spring. That happens at a displacement smaller than the initial one.

---

## Final answers for Problem 2

### 1. Natural frequency

Angular natural frequency:

$$
\omega_0=10\ \mathrm{rad/s}
$$

Ordinary frequency:

$$
f=\frac{10}{2\pi}\approx 1.59\ \mathrm{Hz}
$$

---

### 2. Total energy

$$
E=200.5\ \mathrm{J}
$$

---

### 3. Displacement where kinetic energy is 50% of total energy

$$
x=\pm 1.42\ \mathrm{m}
$$

---

