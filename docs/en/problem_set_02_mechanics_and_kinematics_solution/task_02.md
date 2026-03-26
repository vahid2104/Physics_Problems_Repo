# Problem 2 – Projectile Motion

Given:

A body moves in the Earth's gravitational field without air resistance. It is launched with initial velocity (v_0) at an angle (\alpha) relative to the horizontal.

We need to determine:

* the equations of motion in the horizontal and vertical directions,
* the time of flight,
* the maximum height,
* the range,
* the angle for which the range is maximum,
* an animation of the trajectory for different values of (\alpha).

---

## 1. Equations of motion

First, we resolve the initial velocity into horizontal and vertical components:

$$
v_{0x}=v_0\cos\alpha, \qquad v_{0y}=v_0\sin\alpha
$$

### Horizontal motion

There is no acceleration in the horizontal direction, so

$$
a_x=0
$$

Hence the horizontal velocity remains constant:

$$
v_x(t)=v_0\cos\alpha
$$

Therefore, the horizontal position is

$$
x(t)=v_0\cos\alpha\cdot t
$$

### Vertical motion

In the vertical direction, the only acceleration is gravity:

$$
a_y=-g
$$

So the vertical velocity is

$$
v_y(t)=v_0\sin\alpha-gt
$$

Therefore, the vertical position is

$$
y(t)=v_0\sin\alpha\cdot t-\frac12 gt^2
$$

Thus, the equations of motion are

$$
x(t)=v_0\cos\alpha\cdot t
$$

$$
y(t)=v_0\sin\alpha\cdot t-\frac12 gt^2
$$

---

## 2. Time of flight

The time of flight is the time when the projectile returns to the ground, that is when

$$
y(t)=0
$$

Substitute the expression for (y(t)):

$$
v_0\sin\alpha\cdot t-\frac12 gt^2=0
$$

Factor out (t):

$$
t\left(v_0\sin\alpha-\frac12 gt\right)=0
$$

This gives two solutions:

$$
t=0
$$

and

$$
v_0\sin\alpha-\frac12 gt=0
$$

Solving for the nonzero time:

$$
\frac12 gt=v_0\sin\alpha
$$

$$
t=\frac{2v_0\sin\alpha}{g}
$$

Therefore, the time of flight is

$$
T=\frac{2v_0\sin\alpha}{g}
$$

---

## 3. Maximum height

The maximum height is reached when the vertical velocity becomes zero:

$$
v_y(t)=0
$$

So we solve

$$
v_0\sin\alpha-gt=0
$$

Hence

$$
t_{\max}=\frac{v_0\sin\alpha}{g}
$$

Now substitute this into the vertical position formula:

$$
H_{\max}=v_0\sin\alpha\cdot \frac{v_0\sin\alpha}{g}-\frac12 g\left(\frac{v_0\sin\alpha}{g}\right)^2
$$

Simplify the first term:

$$
v_0\sin\alpha\cdot \frac{v_0\sin\alpha}{g}=\frac{v_0^2\sin^2\alpha}{g}
$$

Simplify the second term:

$$
\frac12 g\left(\frac{v_0^2\sin^2\alpha}{g^2}\right)=\frac12\frac{v_0^2\sin^2\alpha}{g}
$$

Therefore,

$$
H_{\max}=\frac{v_0^2\sin^2\alpha}{g}-\frac12\frac{v_0^2\sin^2\alpha}{g}
$$

$$
H_{\max}=\frac{v_0^2\sin^2\alpha}{2g}
$$

So the maximum height is

$$
H_{\max}=\frac{v_0^2\sin^2\alpha}{2g}
$$

---

## 4. Range

The range is the horizontal distance traveled during the full flight time:

$$
R=x(T)
$$

Substitute (T=\frac{2v_0\sin\alpha}{g}) into the formula for (x(t)):

$$
R=v_0\cos\alpha\cdot \frac{2v_0\sin\alpha}{g}
$$

$$
R=\frac{2v_0^2\sin\alpha\cos\alpha}{g}
$$

Using the trigonometric identity

$$
2\sin\alpha\cos\alpha=\sin 2\alpha
$$

we obtain

$$
R=\frac{v_0^2\sin 2\alpha}{g}
$$

Therefore, the range is

$$
R=\frac{v_0^2\sin 2\alpha}{g}
$$

---

## 5. Angle for maximum range

We use the formula for the range:

$$
R=\frac{v_0^2\sin 2\alpha}{g}
$$

Since (v_0^2/g) is constant, the range is maximum when (\sin 2\alpha) is maximum.

The maximum value of sine is

$$
\sin 2\alpha=1
$$

This happens when

$$
2\alpha=90^\circ
$$

Hence

$$
\alpha=45^\circ
$$

Therefore, the range is maximum for

$$
\alpha=45^\circ
$$

---

## 6. Animation of the trajectory

To visualize the motion, we can plot the trajectory for different launch angles (\alpha), for example:

$$
\alpha=15^\circ,;30^\circ,;45^\circ,;60^\circ,;75^\circ
$$

For each angle, the trajectory is described by

$$
x(t)=v_0\cos\alpha\cdot t
$$

$$
y(t)=v_0\sin\alpha\cdot t-\frac12 gt^2
$$

By varying (\alpha), we obtain different parabolic paths.

The animation file is attached here:

[Download the animation](sandbox:/mnt/data/projectile_motion_angles.gif)

---

## Final answers for Problem 2

$$
x(t)=v_0\cos\alpha\cdot t
$$

$$
y(t)=v_0\sin\alpha\cdot t-\frac12 gt^2
$$

$$
T=\frac{2v_0\sin\alpha}{g}
$$

$$
H_{\max}=\frac{v_0^2\sin^2\alpha}{2g}
$$

$$
R=\frac{v_0^2\sin 2\alpha}{g}
$$

$$
\alpha_{\max}=45^\circ
$$

The trajectory is parabolic, and different values of (\alpha) produce different projectile paths.

---
