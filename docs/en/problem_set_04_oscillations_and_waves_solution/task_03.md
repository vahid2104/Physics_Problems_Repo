
---

# Problem 3 – Harmonic wave

The wave is described by

$$
y(x,t)=A\sin(kx-\omega t)
$$

We need to determine:

* the wavelength $\lambda$,
* the phase velocity $v$,
* calculate $v$ for

$$
k=4\pi,\qquad \omega=20\pi,
$$

* and decide whether the point $x=\lambda$ oscillates in phase with the point $x=0$.

---

## 1. Determine the wavelength

The general form of a harmonic wave is

$$
y(x,t)=A\sin(kx-\omega t)
$$

The quantity $k$ is called the **wave number**.

For a wave, the wave number and wavelength are related by

$$
k=\frac{2\pi}{\lambda}
$$

Now solve for $\lambda$.

Multiply both sides by $\lambda$:

$$
k\lambda=2\pi
$$

Now divide by $k$:

$$
\lambda=\frac{2\pi}{k}
$$

Therefore, the wavelength is

$$
\lambda=\frac{2\pi}{k}
$$

---

## 2. Determine the phase velocity

The **phase velocity** is the speed at which a point of constant phase moves.

For example, take a crest or any point for which the argument of the sine stays constant:

$$
kx-\omega t=\text{constant}
$$

We now use this to find the velocity.

Differentiate both sides with respect to time:

$$
\frac{d}{dt}(kx-\omega t)=0
$$

Since $k$ and $\omega$ are constants, we get

$$
k\frac{dx}{dt}-\omega=0
$$

But

$$
\frac{dx}{dt}=v
$$

so

$$
kv-\omega=0
$$

Hence,

$$
kv=\omega
$$

and therefore

$$
v=\frac{\omega}{k}
$$

So the phase velocity is

$$
v=\frac{\omega}{k}
$$

---

## 3. Calculate $v$ for $k=4\pi$ and $\omega=20\pi$

We use the formula

$$
v=\frac{\omega}{k}
$$

Substitute the given values:

$$
v=\frac{20\pi}{4\pi}
$$

The factor $\pi$ cancels:

$$
v=\frac{20}{4}
$$

$$
v=5
$$

Therefore,

$$
v=5\ \text{m/s}
$$

(if SI units are assumed)

---

## 4. Does the point $x=\lambda$ oscillate in phase with the point $x=0$?

We compare the motion at the two points.

---

### 4.1 At the point $x=0$

Substitute $x=0$ into the wave equation:

$$
y(0,t)=A\sin(0-\omega t)
$$

So

$$
y(0,t)=A\sin(-\omega t)
$$

---

### 4.2 At the point $x=\lambda$

Substitute $x=\lambda$:

$$
y(\lambda,t)=A\sin(k\lambda-\omega t)
$$

From the wavelength relation,

$$
k=\frac{2\pi}{\lambda}
$$

so

$$
k\lambda=2\pi
$$

Thus

$$
y(\lambda,t)=A\sin(2\pi-\omega t)
$$

Now use the periodicity of sine:

$$
\sin(\theta+2\pi)=\sin\theta
$$

So

$$
\sin(2\pi-\omega t)=\sin(-\omega t)
$$

Therefore,

$$
y(\lambda,t)=A\sin(-\omega t)
$$

But this is exactly the same as for $x=0$:

$$
y(\lambda,t)=y(0,t)
$$

So the two points oscillate **in phase**.

---

## 5. Interpretation

Let us explain the physical meaning of these results.

### Wavelength

The wavelength is

$$
\lambda=\frac{2\pi}{k}
$$

It tells us the distance between two neighboring points that oscillate in the same way, for example two neighboring crests.

So after moving by one wavelength, the wave pattern repeats in space.

---

### Phase velocity

The phase velocity is

$$
v=\frac{\omega}{k}
$$

It tells us how fast a point of constant phase moves, such as a crest, trough, or any fixed point on the wave shape.

In this problem,

$$
v=5\ \text{m/s}
$$

So the wave shape moves along the $x$-axis with speed $5\ \text{m/s}$.

Also, because the argument is

$$
kx-\omega t,
$$

the wave travels in the **positive $x$ direction**.

---

### In-phase points

Two points oscillate in phase if they always have the same displacement and the same stage of motion at the same time.

Points separated by one full wavelength satisfy this condition.

Since $x=\lambda$ is exactly one wavelength away from $x=0$, these two points oscillate in phase.

---

## Final answers for Problem 3

The general formulas are:

$$
\lambda=\frac{2\pi}{k}
$$

$$
v=\frac{\omega}{k}
$$

For

$$
k=4\pi,\qquad \omega=20\pi
$$

we get

$$
\lambda=\frac{2\pi}{4\pi}=\frac{1}{2}\ \text{m}
$$

$$
v=\frac{20\pi}{4\pi}=5\ \text{m/s}
$$

And:

* the point $x=\lambda$ **does oscillate in phase** with the point $x=0$.

---

