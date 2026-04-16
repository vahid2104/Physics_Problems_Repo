
# Problem 4 – Wave equation

The function is given:

$$
y(x,t)=A\cos(kx-\omega t)
$$

We need to:

1. verify that it satisfies the wave equation
   $$
   \frac{\partial^2 y}{\partial t^2}=v^2\frac{\partial^2 y}{\partial x^2}
   $$
2. determine the relation between $v$, $k$, and $\omega$.

---

## 1. Given wave function

We start with

$$
y(x,t)=A\cos(kx-\omega t)
$$

This function depends on both position $x$ and time $t$.

To check whether it satisfies the wave equation, we must calculate:

* the second derivative with respect to time $t$,
* the second derivative with respect to position $x$,

and then compare them.

---

## 2. Second derivative with respect to time

We first compute the first derivative with respect to $t$.

Given

$$
y(x,t)=A\cos(kx-\omega t)
$$

Let

$$
u=kx-\omega t
$$

Then

$$
y=A\cos u
$$

Using the chain rule,

$$
\frac{\partial y}{\partial t}
=============================

-A\sin(kx-\omega t)\cdot \frac{\partial}{\partial t}(kx-\omega t)
$$

Since $kx$ is constant with respect to $t$ and

$$
\frac{\partial}{\partial t}(kx-\omega t)=-\omega
$$

we get

$$
\frac{\partial y}{\partial t}
=============================

-A\sin(kx-\omega t)(-\omega)
$$

So

$$
\frac{\partial y}{\partial t}
=============================

A\omega \sin(kx-\omega t)
$$

---

Now differentiate again with respect to $t$:

$$
\frac{\partial^2 y}{\partial t^2}
=================================

A\omega \frac{\partial}{\partial t}\sin(kx-\omega t)
$$

Again using the chain rule,

$$
\frac{\partial}{\partial t}\sin(kx-\omega t)
============================================

\cos(kx-\omega t)(-\omega)
$$

Therefore,

$$
\frac{\partial^2 y}{\partial t^2}
=================================

A\omega \cos(kx-\omega t)(-\omega)
$$

So

$$
\frac{\partial^2 y}{\partial t^2}
=================================

-A\omega^2\cos(kx-\omega t)
$$

Thus,

$$
\boxed{\frac{\partial^2 y}{\partial t^2}=-A\omega^2\cos(kx-\omega t)}
$$

---

## 3. Second derivative with respect to position

Now we compute the first derivative with respect to $x$.

Starting again from

$$
y(x,t)=A\cos(kx-\omega t)
$$

Using the chain rule,

$$
\frac{\partial y}{\partial x}
=============================

-A\sin(kx-\omega t)\cdot \frac{\partial}{\partial x}(kx-\omega t)
$$

Since $-\omega t$ is constant with respect to $x$ and

$$
\frac{\partial}{\partial x}(kx-\omega t)=k
$$

we get

$$
\frac{\partial y}{\partial x}
=============================

-Ak\sin(kx-\omega t)
$$

---

Now differentiate again with respect to $x$:

$$
\frac{\partial^2 y}{\partial x^2}
=================================

-Ak\frac{\partial}{\partial x}\sin(kx-\omega t)
$$

Again using the chain rule,

$$
\frac{\partial}{\partial x}\sin(kx-\omega t)
============================================

\cos(kx-\omega t)\cdot k
$$

Therefore,

$$
\frac{\partial^2 y}{\partial x^2}
=================================

-Ak\cos(kx-\omega t)\cdot k
$$

So

$$
\frac{\partial^2 y}{\partial x^2}
=================================

-Ak^2\cos(kx-\omega t)
$$

Thus,

$$
\boxed{\frac{\partial^2 y}{\partial x^2}=-Ak^2\cos(kx-\omega t)}
$$

---

## 4. Substitute into the wave equation

The wave equation is

$$
\frac{\partial^2 y}{\partial t^2}=v^2\frac{\partial^2 y}{\partial x^2}
$$

From above,

$$
\frac{\partial^2 y}{\partial t^2}=-A\omega^2\cos(kx-\omega t)
$$

and

$$
\frac{\partial^2 y}{\partial x^2}=-Ak^2\cos(kx-\omega t)
$$

Multiply the second spatial derivative by $v^2$:

$$
v^2\frac{\partial^2 y}{\partial x^2}
====================================

v^2(-Ak^2\cos(kx-\omega t))
$$

So

$$
v^2\frac{\partial^2 y}{\partial x^2}
====================================

-A v^2 k^2 \cos(kx-\omega t)
$$

For the wave equation to be satisfied, we need

$$
-A\omega^2\cos(kx-\omega t)
===========================

-A v^2 k^2\cos(kx-\omega t)
$$

Since the common factor

$$
-A\cos(kx-\omega t)
$$

appears on both sides, we can cancel it.

That gives

$$
\omega^2=v^2k^2
$$

So the function satisfies the wave equation provided that

$$
\boxed{\omega^2=v^2k^2}
$$

---

## 5. Relation between $v$, $k$, and $\omega$

From

$$
\omega^2=v^2k^2
$$

take the square root:

$$
\omega=vk
$$

So

$$
\boxed{v=\frac{\omega}{k}}
$$

This is the required algebraic relation.

---

## 6. Interpretation

The formula

$$
v=\frac{\omega}{k}
$$

tells us the speed of the wave.

It means:

* larger angular frequency $\omega$ gives a larger wave speed,
* larger wave number $k$ gives a smaller wave speed.

This is the standard relation for a sinusoidal travelling wave.

---

## Final answers for Problem 4

The function

$$
y(x,t)=A\cos(kx-\omega t)
$$

has derivatives

$$
\frac{\partial^2 y}{\partial t^2}=-A\omega^2\cos(kx-\omega t)
$$

and

$$
\frac{\partial^2 y}{\partial x^2}=-Ak^2\cos(kx-\omega t)
$$

Substituting into

$$
\frac{\partial^2 y}{\partial t^2}=v^2\frac{\partial^2 y}{\partial x^2}
$$

gives

$$
\omega^2=v^2k^2
$$

Therefore, the required relation is

$$
\boxed{v=\frac{\omega}{k}}
$$

or equivalently

$$
\boxed{\omega=vk}
$$

