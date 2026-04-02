## Problem 3 – Work of a variable force

We are given the one-dimensional force

$$
F(x)=-kx
$$

where (k>0) is a constant.

We need to determine:

* the equation of motion and its solution,
* the work done during the displacement from (0) to (x_0),
* the interpretation in terms of potential energy,
* the verification that
  $$
  F=-\frac{dU}{dx},
  $$
* and the graphs of (F(x)) and (U(x)).

---

## 1. Equation of motion

From Newton’s second law,

$$
F=ma
$$

In one dimension, acceleration is

$$
a=\frac{d^2x}{dt^2}
$$

So

$$
m\frac{d^2x}{dt^2}=F(x)
$$

Since

$$
F(x)=-kx,
$$

we get

$$
m\frac{d^2x}{dt^2}=-kx
$$

or equivalently

$$
\frac{d^2x}{dt^2}+\frac{k}{m}x=0
$$

Therefore, the equation of motion is

$$
\boxed{\frac{d^2x}{dt^2}+\frac{k}{m}x=0}
$$

This is the equation of a simple harmonic oscillator.

---

## 2. Solution of the equation of motion

We solve

$$
\frac{d^2x}{dt^2}+\frac{k}{m}x=0
$$

Let

$$
\omega=\sqrt{\frac{k}{m}}
$$

Then the equation becomes

$$
\frac{d^2x}{dt^2}+\omega^2 x=0
$$

The general solution is

$$
x(t)=A\cos(\omega t)+B\sin(\omega t)
$$

So we obtain

$$
\boxed{x(t)=A\cos\left(\sqrt{\frac{k}{m}},t\right)+B\sin\left(\sqrt{\frac{k}{m}},t\right)}
$$

where (A) and (B) are constants determined by the initial conditions.

### Basic interpretation

This means:

* the body does not move in a straight increasing or decreasing way,
* it oscillates around the point (x=0),
* the force always points toward the origin.

That is why this force is called a **restoring force**.

---

## 3. Work done from (0) to (x_0)

The work done by a variable force in one dimension is

$$
W=\int_{x=0}^{x=x_0} F(x),dx
$$

Since

$$
F(x)=-kx,
$$

we have

$$
W=\int_0^{x_0} (-kx),dx
$$

Take the constant (-k) outside the integral:

$$
W=-k\int_0^{x_0} x,dx
$$

Now integrate:

$$
\int x,dx=\frac{x^2}{2}
$$

So

$$
W=-k\left[\frac{x^2}{2}\right]_0^{x_0}
$$

Substitute the limits:

$$
W=-k\left(\frac{x_0^2}{2}-0\right)
$$

Thus,

$$
\boxed{W=-\frac{1}{2}kx_0^2}
$$

Therefore, the work done by the force during the displacement from (0) to (x_0) is

$$
\boxed{W=-\frac{1}{2}kx_0^2}
$$

### Meaning of the sign

The work is negative because:

* if the body is moved from (0) to a positive position (x_0),
* the force points in the opposite direction,
* so the force resists the motion.

---

## 4. Interpretation as potential energy

For a conservative force, the change in potential energy is related to the work by

$$
\Delta U=-W
$$

From the previous result,

$$
W=-\frac{1}{2}kx_0^2
$$

So

$$
\Delta U=\frac{1}{2}kx_0^2
$$

If we choose the potential energy at the origin to be zero, that is,

$$
U(0)=0,
$$

then the potential energy at position (x) is

$$
\boxed{U(x)=\frac{1}{2}kx^2}
$$

Therefore, the force (F(x)=-kx) corresponds to the potential energy

$$
\boxed{U(x)=\frac{1}{2}kx^2}
$$

### Basic interpretation

This tells us:

* at (x=0), the potential energy is minimum,
* as (|x|) increases, the potential energy increases,
* the farther the body is from equilibrium, the more energy is stored.

This is exactly what happens for a spring.

---

## 5. Verify that (F=-\dfrac{dU}{dx})

We found

$$
U(x)=\frac{1}{2}kx^2
$$

Now differentiate with respect to (x):

$$
\frac{dU}{dx}=\frac{d}{dx}\left(\frac{1}{2}kx^2\right)
$$

Since (k) is constant,

$$
\frac{dU}{dx}=\frac{1}{2}k\cdot 2x
$$

So

$$
\frac{dU}{dx}=kx
$$

Therefore,

$$
-\frac{dU}{dx}=-kx
$$

But the given force is

$$
F(x)=-kx
$$

Thus,

$$
\boxed{F(x)=-\frac{dU}{dx}}
$$

So the required relation is verified.

---

## 6. Graph of (F(x))

The force is

$$
F(x)=-kx
$$

This is a straight line passing through the origin with negative slope.

### Important points

At (x=0):

$$
F(0)=0
$$

At (x>0):

$$
F(x)<0
$$

At (x<0):

$$
F(x)>0
$$

So:

* on the right side, the force points left,
* on the left side, the force points right,
* the force always points toward the origin.

### Shape of the graph

It looks like this:

```text
F(x)
 ^
 |
 |\
 | \
 |  \
 |   \
 |    \
 |-----\-----------> x
 |      \
 |       \
 |        \
 |
```

It is a decreasing straight line through ((0,0)).

---

## 7. Graph of (U(x))

The potential energy is

$$
U(x)=\frac{1}{2}kx^2
$$

This is a parabola opening upward.

### Important points

At (x=0):

$$
U(0)=0
$$

At (x>0) or (x<0):

$$
U(x)>0
$$

So:

* the minimum value is at the origin,
* the graph is symmetric with respect to the vertical axis,
* the energy increases as we move away from equilibrium.

### Shape of the graph

It looks like this:

```text
U(x)
 ^
 |
 |        *
 |      *   *
 |    *       *
 |  *           *
 | *             *
 |_______*_______________> x
         0
```

It is an upward-opening parabola with vertex at ((0,0)).

---

## 8. Physical meaning of both graphs

The two graphs are closely related:

* (F(x)) is linear in (x),
* (U(x)) is quadratic in (x).

This means:

* the restoring force grows linearly with distance,
* the stored potential energy grows like the square of the distance.

That is the standard model of an ideal spring.

---

## Final answers for Problem 3

The equation of motion is

$$
\boxed{m\frac{d^2x}{dt^2}=-kx}
$$

or

$$
\boxed{\frac{d^2x}{dt^2}+\frac{k}{m}x=0}
$$

Its general solution is

$$
\boxed{x(t)=A\cos\left(\sqrt{\frac{k}{m}},t\right)+B\sin\left(\sqrt{\frac{k}{m}},t\right)}
$$

The work done by the force from (0) to (x_0) is

$$
\boxed{W=-\frac{1}{2}kx_0^2}
$$

The corresponding potential energy is

$$
\boxed{U(x)=\frac{1}{2}kx^2}
$$

The relation between force and potential energy is satisfied:

$$
\boxed{F=-\frac{dU}{dx}}
$$

The graph of (F(x)) is a straight line through the origin with negative slope, and the graph of (U(x)) is an upward-opening parabola.

---

