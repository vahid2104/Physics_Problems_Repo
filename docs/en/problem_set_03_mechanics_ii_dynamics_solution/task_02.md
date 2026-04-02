
---

# Problem 2 – Inclined plane with friction

A body of mass $m$ slides down an inclined plane that makes an angle $\alpha$ with the horizontal. The coefficient of kinetic friction is $\mu$.

We need to determine:

* all forces acting on the body,
* the acceleration $\vec a$,
* the time of descent from height $h$,
* the final velocity $\vec v$,
* the consistency with the energy balance.

---

## 1. Forces acting on the body

When the body slides down the incline, three forces act on it:

### (a) Gravity

The weight of the body is

$$
\vec F_g = m\vec g
$$

It acts vertically downward.

---

### (b) Normal force

The plane pushes on the body with the normal force $\vec N$.

This force is perpendicular to the surface of the incline.

Its magnitude is

$$
N = mg\cos\alpha
$$

because the component of gravity perpendicular to the plane is $mg\cos\alpha$.

---

### (c) Kinetic friction

Since the body is sliding, the friction force is kinetic friction.

Its magnitude is

$$
F_f = \mu N
$$

Substitute $N=mg\cos\alpha$:

$$
F_f = \mu mg\cos\alpha
$$

This force acts **up the plane**, opposite to the motion.

---

## 2. Choose axes

It is easiest to choose axes:

* one axis **along the plane**,
* one axis **perpendicular to the plane**.

Then we split gravity into two components:

### Component parallel to the plane

$$
mg\sin\alpha
$$

This component pulls the body **down the plane**.

### Component perpendicular to the plane

$$
mg\cos\alpha
$$

This component presses the body into the plane.

---

## 3. Equation of motion along the plane

Now apply Newton’s second law along the incline.

The forces along the plane are:

* downward: $mg\sin\alpha$,
* upward: friction $\mu mg\cos\alpha$.

So the net force along the plane is

$$
F_{\text{net}} = mg\sin\alpha - \mu mg\cos\alpha
$$

From Newton’s second law,

$$
F_{\text{net}} = ma
$$

Therefore,

$$
ma = mg\sin\alpha - \mu mg\cos\alpha
$$

Divide by $m$:

$$
a = g\sin\alpha - \mu g\cos\alpha
$$

So the acceleration along the plane is

$$
a = g(\sin\alpha - \mu\cos\alpha)
$$

Therefore,

$$
\vec a = g(\sin\alpha - \mu\cos\alpha),\hat e_{\parallel}
$$

where $\hat e_{\parallel}$ is the unit vector directed **down the plane**.

---

## 4. Condition for sliding down

For the body to actually accelerate downward, we need

$$
a>0
$$

So

$$
g(\sin\alpha-\mu\cos\alpha)>0
$$

Since $g>0$, this means

$$
\sin\alpha-\mu\cos\alpha>0
$$

or

$$
\tan\alpha>\mu
$$

So the body slides down only if

$$
\tan\alpha>\mu
$$

---

## 5. Distance traveled along the plane

The height of the incline is $h$.

Let $s$ be the distance traveled along the plane.

From the geometry of the incline,

$$
\sin\alpha = \frac{h}{s}
$$

So

$$
s = \frac{h}{\sin\alpha}
$$

---

## 6. Time of descent

Assume the body starts from rest.

Then the motion along the plane has constant acceleration $a$, so we use

$$
s = \frac{1}{2}at^2
$$

Substitute

$$
s=\frac{h}{\sin\alpha}
\qquad \text{and} \qquad
a=g(\sin\alpha-\mu\cos\alpha)
$$

Then

$$
\frac{h}{\sin\alpha}
====================

\frac{1}{2}g(\sin\alpha-\mu\cos\alpha)t^2
$$

Solve for $t^2$:

$$
t^2 =
\frac{2h}{g\sin\alpha(\sin\alpha-\mu\cos\alpha)}
$$

Therefore,

$$
t=
\sqrt{
\frac{2h}{g\sin\alpha(\sin\alpha-\mu\cos\alpha)}
}
$$

So the time of descent is

$$
t=
\sqrt{
\frac{2h}{g\sin\alpha(\sin\alpha-\mu\cos\alpha)}
}
$$

---

## 7. Final velocity

Again assume the body starts from rest.

For constant acceleration, we use

$$
v^2 = 2as
$$

Substitute

$$
a=g(\sin\alpha-\mu\cos\alpha)
\qquad \text{and} \qquad
s=\frac{h}{\sin\alpha}
$$

Then

$$
v^2 = 2,g(\sin\alpha-\mu\cos\alpha),\frac{h}{\sin\alpha}
$$

So

$$
v^2 = \frac{2gh(\sin\alpha-\mu\cos\alpha)}{\sin\alpha}
$$

Therefore,

$$
v=
\sqrt{
\frac{2gh(\sin\alpha-\mu\cos\alpha)}{\sin\alpha}
}
$$

Thus the final velocity vector is directed down the plane:

$$
\vec v=
\sqrt{
\frac{2gh(\sin\alpha-\mu\cos\alpha)}{\sin\alpha}
},\hat e_{\parallel}
$$

---

## 8. Check with the energy balance

Now let us verify the result using energy.

### Initial energy

The body starts from height $h$ and from rest.

So the initial mechanical energy is only gravitational potential energy:

$$
E_i = mgh
$$

---

### Work done by friction

The friction force has magnitude

$$
F_f = \mu mg\cos\alpha
$$

It acts opposite to the motion, so its work is negative:

$$
W_f = -F_f s
$$

Substitute $s=\dfrac{h}{\sin\alpha}$:

$$
W_f = -\mu mg\cos\alpha \cdot \frac{h}{\sin\alpha}
$$

So

$$
W_f = -\frac{\mu mgh\cos\alpha}{\sin\alpha}
$$

---

### Final energy

At the bottom, the potential energy is zero, and the kinetic energy is

$$
E_f = \frac{1}{2}mv^2
$$

---

### Energy equation

The change in mechanical energy is due to friction:

$$
E_i + W_f = E_f
$$

So

$$
mgh - \frac{\mu mgh\cos\alpha}{\sin\alpha}
==========================================

\frac{1}{2}mv^2
$$

Factor out $mgh$:

$$
mgh\left(1-\frac{\mu\cos\alpha}{\sin\alpha}\right)
==================================================

\frac{1}{2}mv^2
$$

Cancel $m$:

$$
gh\left(1-\frac{\mu\cos\alpha}{\sin\alpha}\right)
=================================================

\frac{1}{2}v^2
$$

Multiply by $2$:

$$
v^2 =
2gh\left(1-\frac{\mu\cos\alpha}{\sin\alpha}\right)
$$

Put everything over a common denominator:

$$
v^2 =
\frac{2gh(\sin\alpha-\mu\cos\alpha)}{\sin\alpha}
$$

Thus,

$$
v=
\sqrt{
\frac{2gh(\sin\alpha-\mu\cos\alpha)}{\sin\alpha}
}
$$

This is exactly the same result as before.

So the result is consistent with the energy balance.

---

## Final answers for Problem 2

### Forces acting on the body

* Gravity: $\vec F_g=m\vec g$
* Normal force: $N=mg\cos\alpha$
* Kinetic friction: $F_f=\mu mg\cos\alpha$

Friction acts up the plane, opposite to the motion.

---

### Acceleration

$$
\vec a = g(\sin\alpha-\mu\cos\alpha),\hat e_{\parallel}
$$

So its magnitude is

$$
a = g(\sin\alpha-\mu\cos\alpha)
$$

---

### Time of descent from height $h$

$$
t=
\sqrt{
\frac{2h}{g\sin\alpha(\sin\alpha-\mu\cos\alpha)}
}
$$

---

### Final velocity

$$
\vec v=
\sqrt{
\frac{2gh(\sin\alpha-\mu\cos\alpha)}{\sin\alpha}
},\hat e_{\parallel}
$$

---

### Energy check

Using energy, we get the same result:

$$
\frac{1}{2}mv^2
===============

mgh-\mu mg\cos\alpha\cdot \frac{h}{\sin\alpha}
$$

which gives

$$
v^2=
\frac{2gh(\sin\alpha-\mu\cos\alpha)}{\sin\alpha}
$$

So the solution is consistent with the energy balance.

---

