# Problem 8 – Harmonic oscillator (formal dynamics)

We consider the equation

$$
m\ddot x+kx=0
$$

We need to:

* solve the equation,
* determine the natural frequency,
* write the energy as a function of time,
* show that energy is conserved,
* interpret the motion in phase space.

---

## 1. Solve the equation

We start from

$$
m\ddot x+kx=0
$$

Divide the whole equation by $m$:

$$
\ddot x+\frac{k}{m}x=0
$$

This is the standard equation of a harmonic oscillator.

Let us introduce the constant

$$
\omega_0^2=\frac{k}{m}
$$

Then the equation becomes

$$
\ddot x+\omega_0^2 x=0
$$

---

### General form of the solution

A standard solution of this equation is

$$
x(t)=A\cos(\omega_0 t)+B\sin(\omega_0 t)
$$

where $A$ and $B$ are constants determined by the initial conditions.

Therefore, the general solution is

$$
x(t)=A\cos(\omega_0 t)+B\sin(\omega_0 t)
$$

with

$$
\omega_0=\sqrt{\frac{k}{m}}
$$

---

### Check that this is really a solution

Differentiate once:

$$
\dot x(t)=-A\omega_0\sin(\omega_0 t)+B\omega_0\cos(\omega_0 t)
$$

Differentiate again:

$$
\ddot x(t)=-A\omega_0^2\cos(\omega_0 t)-B\omega_0^2\sin(\omega_0 t)
$$

Factor out $-\omega_0^2$:

$$
\ddot x(t)=-\omega_0^2\left[A\cos(\omega_0 t)+B\sin(\omega_0 t)\right]
$$

But the bracket is exactly $x(t)$, so

$$
\ddot x(t)=-\omega_0^2 x(t)
$$

Thus,

$$
\ddot x+\omega_0^2 x=0
$$

So the formula is correct.

---

## 2. Determine the natural frequency

From

$$
\ddot x+\frac{k}{m}x=0
$$

we identified

$$
\omega_0^2=\frac{k}{m}
$$

Hence the natural angular frequency is

$$
\omega_0=\sqrt{\frac{k}{m}}
$$

Therefore, the natural frequency is

$$
\boxed{\omega_0=\sqrt{\frac{k}{m}}}
$$

If we want the ordinary frequency in hertz, then

$$
f_0=\frac{\omega_0}{2\pi}
$$

So

$$
\boxed{f_0=\frac{1}{2\pi}\sqrt{\frac{k}{m}}}
$$

---

## 3. Energy as a function of time

For the harmonic oscillator, the total mechanical energy is

$$
E(t)=T+V
$$

where

* $T$ is the kinetic energy,
* $V$ is the potential energy.

---

### Kinetic energy

The kinetic energy is

$$
T=\frac12 m\dot x^2
$$

---

### Potential energy

The restoring force is

$$
F=-kx
$$

so the corresponding potential energy is

$$
V=\frac12 kx^2
$$

---

### Total energy

Therefore,

$$
E(t)=\frac12 m\dot x(t)^2+\frac12 kx(t)^2
$$

This is the energy as a function of time.

So we can write

$$
\boxed{E(t)=\frac12 m\dot x(t)^2+\frac12 kx(t)^2}
$$

---

### Write it more explicitly

We have

$$
x(t)=A\cos(\omega_0 t)+B\sin(\omega_0 t)
$$

and

$$
\dot x(t)=-A\omega_0\sin(\omega_0 t)+B\omega_0\cos(\omega_0 t)
$$

Substitute into the energy:

$$
E(t)=\frac12 m\left[-A\omega_0\sin(\omega_0 t)+B\omega_0\cos(\omega_0 t)\right]^2
+\frac12 k\left[A\cos(\omega_0 t)+B\sin(\omega_0 t)\right]^2
$$

This is the explicit energy formula.

---

## 4. Show that energy is conserved

We now prove that $E(t)$ does not change with time.

Start with

$$
E(t)=\frac12 m\dot x^2+\frac12 kx^2
$$

Differentiate with respect to time:

$$
\frac{dE}{dt}=m\dot x\ddot x+kx\dot x
$$

Factor out $\dot x$:

$$
\frac{dE}{dt}=\dot x(m\ddot x+kx)
$$

But the equation of motion says

$$
m\ddot x+kx=0
$$

Therefore,

$$
\frac{dE}{dt}=\dot x\cdot 0=0
$$

So

$$
\frac{dE}{dt}=0
$$

which means the energy is constant in time.

Therefore, energy is conserved:

$$
\boxed{E(t)=\text{constant}}
$$

---

### Constant value of the energy

Using $\omega_0^2=\frac{k}{m}$, one can show that the constant energy is

$$
E=\frac12 k(A^2+B^2)
$$

Indeed, since

$$
m\omega_0^2=k
$$

the time-dependent terms cancel, and the final result is constant.

So the total energy can also be written as

$$
\boxed{E=\frac12 k(A^2+B^2)}
$$

If the motion is written in the form

$$
x(t)=C\cos(\omega_0 t+\phi)
$$

then the amplitude is $C$, and the energy becomes

$$
\boxed{E=\frac12 kC^2}
$$

---

## 5. Interpret the motion in phase space

Phase space for this problem is the plane with coordinates

$$
(x,\dot x)
$$

That means:

* horizontal axis: position $x$,
* vertical axis: velocity $\dot x$.

---

### Express $x$ and $\dot x$

We have

$$
x(t)=A\cos(\omega_0 t)+B\sin(\omega_0 t)
$$

and

$$
\dot x(t)=-A\omega_0\sin(\omega_0 t)+B\omega_0\cos(\omega_0 t)
$$

As time passes, the point

$$
(x(t),\dot x(t))
$$

moves in phase space.

---

### Shape of the curve

To find the shape, let us use the energy:

$$
E=\frac12 m\dot x^2+\frac12 kx^2
$$

Multiply by 2:

$$
2E=m\dot x^2+kx^2
$$

Rearrange:

$$
kx^2+m\dot x^2=2E
$$

Divide by $2E$:

$$
\frac{x^2}{2E/k}+\frac{\dot x^2}{2E/m}=1
$$

This is the equation of an ellipse in the $(x,\dot x)$ plane.

Therefore, in phase space, the motion is along a closed ellipse.

---

### Physical meaning

This tells us:

* when $x$ is maximum, the velocity is zero,
* when $\dot x$ is maximum, the position is zero,
* the system moves periodically around the ellipse,
* the orbit is closed because the motion repeats again and again,
* the size of the ellipse depends on the total energy.

So the phase-space motion represents a periodic exchange between:

* potential energy $\frac12 kx^2$,
* kinetic energy $\frac12 m\dot x^2$.

When one is large, the other is small.

---

## Final answers for Problem 8

The differential equation

$$
m\ddot x+kx=0
$$

can be written as

$$
\ddot x+\omega_0^2x=0
\qquad \text{with} \qquad
\omega_0=\sqrt{\frac{k}{m}}
$$

So the general solution is

$$
\boxed{x(t)=A\cos(\omega_0 t)+B\sin(\omega_0 t)}
$$

with natural angular frequency

$$
\boxed{\omega_0=\sqrt{\frac{k}{m}}}
$$

and ordinary frequency

$$
\boxed{f_0=\frac{1}{2\pi}\sqrt{\frac{k}{m}}}
$$

The total energy is

$$
\boxed{E(t)=\frac12 m\dot x(t)^2+\frac12 kx(t)^2}
$$

and since

$$
\frac{dE}{dt}=\dot x(m\ddot x+kx)=0
$$

the energy is conserved:

$$
\boxed{E(t)=\text{constant}}
$$

In phase space $(x,\dot x)$, the motion satisfies

$$
\boxed{kx^2+m\dot x^2=2E}
$$

which is an ellipse. So the oscillator moves periodically on a closed curve in phase space.

---

If you want, I can also make this into an even more student-style version, exactly matching the formatting and tone of your Problem 1.
