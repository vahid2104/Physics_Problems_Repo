
# Problem 1 – Harmonic motion: motion parameters

A harmonic motion is described by

$$
x(t)=A\cos(\omega t+\varphi)
$$

We need to determine:

* the period $T$,
* the frequency $f$,
* the maximum velocity,
* the maximum acceleration,
* and then calculate these quantities for

$$
A=0.2\ \text{m}, \qquad f=2\ \text{Hz}
$$

---

## 1. Period and frequency

The function

$$
x(t)=A\cos(\omega t+\varphi)
$$

describes periodic motion.

For cosine motion, one full cycle happens when the angle increases by

$$
2\pi
$$

So we require

$$
\omega T=2\pi
$$

Therefore, the period is

$$
T=\frac{2\pi}{\omega}
$$

The frequency is the number of oscillations per second, so

$$
f=\frac{1}{T}
$$

Substitute the formula for $T$:

$$
f=\frac{1}{2\pi/\omega}
$$

So

$$
f=\frac{\omega}{2\pi}
$$

Therefore,

$$
T=\frac{2\pi}{\omega}
$$

and

$$
f=\frac{\omega}{2\pi}
$$

---

## 2. Maximum velocity

Velocity is the derivative of position:

$$
v(t)=\frac{dx}{dt}
$$

Differentiate

$$
x(t)=A\cos(\omega t+\varphi)
$$

Using

$$
\frac{d}{dt}\cos(\omega t+\varphi)=-\omega \sin(\omega t+\varphi)
$$

we get

$$
v(t)=-A\omega \sin(\omega t+\varphi)
$$

The sine function always satisfies

$$
-1\le \sin(\omega t+\varphi)\le 1
$$

So the largest possible magnitude of velocity is when

$$
|\sin(\omega t+\varphi)|=1
$$

Thus the maximum velocity is

$$
v_{\max}=A\omega
$$

Therefore,

$$
v_{\max}=A\omega
$$

---

## 3. Maximum acceleration

Acceleration is the derivative of velocity:

$$
a(t)=\frac{dv}{dt}
$$

Differentiate

$$
v(t)=-A\omega \sin(\omega t+\varphi)
$$

Using

$$
\frac{d}{dt}\sin(\omega t+\varphi)=\omega \cos(\omega t+\varphi)
$$

we get

$$
a(t)=-A\omega^2\cos(\omega t+\varphi)
$$

Again, cosine satisfies

$$
-1\le \cos(\omega t+\varphi)\le 1
$$

So the largest possible magnitude of acceleration is when

$$
|\cos(\omega t+\varphi)|=1
$$

Thus the maximum acceleration is

$$
a_{\max}=A\omega^2
$$

Therefore,

$$
a_{\max}=A\omega^2
$$

---

## 4. Numerical calculations for $A=0.2$ m and $f=2$ Hz

We are given

$$
A=0.2\ \text{m}
$$

$$
f=2\ \text{Hz}
$$

We now calculate:

* $\omega$,
* $v_{\max}$,
* $a_{\max}$.

---

### 4.1 Calculate $\omega$

We use the relation

$$
\omega=2\pi f
$$

Substitute $f=2$:

$$
\omega=2\pi\cdot 2
$$

$$
\omega=4\pi\ \text{rad/s}
$$

Approximate value:

$$
\omega \approx 12.57\ \text{rad/s}
$$

Therefore,

$$
\omega=4\pi\ \text{rad/s}\approx 12.57\ \text{rad/s}
$$

---

### 4.2 Calculate the maximum velocity

Use

$$
v_{\max}=A\omega
$$

Substitute the values:

$$
v_{\max}=0.2\cdot 4\pi
$$

$$
v_{\max}=0.8\pi\ \text{m/s}
$$

Approximate value:

$$
v_{\max}\approx 2.51\ \text{m/s}
$$

Therefore,

$$
v_{\max}=0.8\pi\ \text{m/s}\approx 2.51\ \text{m/s}
$$

---

### 4.3 Calculate the maximum acceleration

Use

$$
a_{\max}=A\omega^2
$$

Substitute the values:

$$
a_{\max}=0.2\cdot (4\pi)^2
$$

First compute

$$
(4\pi)^2=16\pi^2
$$

So

$$
a_{\max}=0.2\cdot 16\pi^2
$$

$$
a_{\max}=3.2\pi^2\ \text{m/s}^2
$$

Approximate value:

$$
a_{\max}\approx 31.58\ \text{m/s}^2
$$

Therefore,

$$
a_{\max}=3.2\pi^2\ \text{m/s}^2\approx 31.58\ \text{m/s}^2
$$

---

## 5. Interpretation

Let us explain what these results mean physically.

### Period

The period tells us how long one full oscillation takes.

Since

$$
f=2\ \text{Hz}
$$

the body performs 2 oscillations every second.

So the period is

$$
T=\frac{1}{f}=\frac{1}{2}=0.5\ \text{s}
$$

This means one full back-and-forth motion takes half a second.

---

### Maximum velocity

The maximum velocity is

$$
v_{\max}=A\omega
$$

This means:

* larger amplitude $A$ gives larger maximum speed,
* larger angular frequency $\omega$ also gives larger maximum speed.

So if the body oscillates farther from equilibrium or oscillates faster, its top speed becomes bigger.

In this problem,

$$
v_{\max}\approx 2.51\ \text{m/s}
$$

So at its fastest moment, the body moves with speed about $2.51\ \text{m/s}$.

---

### Maximum acceleration

The maximum acceleration is

$$
a_{\max}=A\omega^2
$$

This means acceleration grows even faster with frequency, because of the square $\omega^2$.

So when oscillations are very rapid, acceleration can become quite large.

In this problem,

$$
a_{\max}\approx 31.58\ \text{m/s}^2
$$

This is much larger than the maximum velocity numerically, because acceleration depends on $\omega^2$, not just $\omega$.

---

## Final answers for Problem 1

The general formulas are:

$$
T=\frac{2\pi}{\omega}
$$

$$
f=\frac{\omega}{2\pi}
$$

$$
v_{\max}=A\omega
$$

$$
a_{\max}=A\omega^2
$$

For

$$
A=0.2\ \text{m}, \qquad f=2\ \text{Hz}
$$

we get

$$
\omega=4\pi\ \text{rad/s}\approx 12.57\ \text{rad/s}
$$

$$
v_{\max}=0.8\pi\ \text{m/s}\approx 2.51\ \text{m/s}
$$

$$
a_{\max}=3.2\pi^2\ \text{m/s}^2\approx 31.58\ \text{m/s}^2
$$

The motion has period

$$
T=0.5\ \text{s}
$$

so the body completes one oscillation in half a second.

---

