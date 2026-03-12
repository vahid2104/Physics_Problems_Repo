# Problem 5 – Trajectory curvature and normal acceleration

For the ellipse:

$$
x=a\cos t, \qquad y=b\sin t
$$

we analyze velocity, acceleration, tangent vector, curvature, and physical interpretation.

---

# 1. Velocity and acceleration

Position vector:

$$
\vec r(t)=(a\cos t,\; b\sin t)
$$

Velocity:

$$
\vec v(t)=\frac{d\vec r}{dt}=(-a\sin t,\; b\cos t)
$$

Acceleration:

$$
\vec a(t)=\frac{d\vec v}{dt}=(-a\cos t,\; -b\sin t)
$$

Velocity magnitude:

$$
|\vec v(t)|=\sqrt{(-a\sin t)^2+(b\cos t)^2}
$$

$$
|\vec v(t)|=\sqrt{a^2\sin^2 t+b^2\cos^2 t}
$$

---

# 2. Unit tangent vector

The unit tangent vector is

$$
\hat T(t)=\frac{\vec v(t)}{|\vec v(t)|}
$$

so

$$
\hat T(t)=
\frac{(-a\sin t,\; b\cos t)}
{\sqrt{a^2\sin^2 t+b^2\cos^2 t}}
$$

---

# 3. Tangential and normal acceleration

Acceleration can be decomposed as

$$
\vec a = \vec a_t + \vec a_n
$$

where

- \( \vec a_t \) – tangential acceleration  
- \( \vec a_n \) – normal acceleration

---

## Tangential component

First compute the dot product

$$
\vec v\cdot\vec a
$$

$$
=(-a\sin t)(-a\cos t)+(b\cos t)(-b\sin t)
$$

$$
=a^2\sin t\cos t-b^2\sin t\cos t
$$

$$
=(a^2-b^2)\sin t\cos t
$$

Tangential scalar acceleration:

$$
a_t=
\frac{\vec v\cdot\vec a}{|\vec v|}
$$

$$
a_t=
\frac{(a^2-b^2)\sin t\cos t}
{\sqrt{a^2\sin^2 t+b^2\cos^2 t}}
$$

---

## Normal component

Using the relation

$$
a_n=\frac{|\vec v \times \vec a|}{|\vec v|}
$$

Treat vectors as 3D:

$$
\vec v=(-a\sin t,\; b\cos t,\;0)
$$

$$
\vec a=(-a\cos t,\; -b\sin t,\;0)
$$

Compute cross product

$$
\vec v\times\vec a=
\begin{vmatrix}
i & j & k \\
-a\sin t & b\cos t & 0 \\
-a\cos t & -b\sin t & 0
\end{vmatrix}
$$

Only the \(k\)-component remains:

$$
\vec v\times\vec a=(0,0,ab)
$$

So

$$
|\vec v\times\vec a|=ab
$$

Normal acceleration magnitude:

$$
a_n=
\frac{ab}
{\sqrt{a^2\sin^2 t+b^2\cos^2 t}}
$$

---

# 4. Radius of curvature at \( t=0 \)

Relation:

$$
a_n=\frac{v^2}{R}
$$

so

$$
R=\frac{v^2}{a_n}
$$

---

## Velocity at \(t=0\)

$$
\vec v(0)=(-a\sin0,\; b\cos0)
$$

$$
\vec v(0)=(0,b)
$$

$$
|\vec v(0)|=b
$$

---

## Normal acceleration at \(t=0\)

$$
a_n(0)=
\frac{ab}{\sqrt{a^2\sin^2 0+b^2\cos^2 0}}
$$

$$
a_n(0)=
\frac{ab}{\sqrt{b^2}}
$$

$$
a_n(0)=a
$$

---

## Radius of curvature

$$
R(0)=\frac{|\vec v(0)|^2}{a_n(0)}
$$

$$
R(0)=\frac{b^2}{a}
$$

---

# 5. Comparison with the circle case \( a=b \)

If \(a=b=R\), the ellipse becomes a circle.

Then

$$
R(0)=\frac{R^2}{R}=R
$$

So the curvature radius equals the circle radius.

---

# Physical interpretation

## 1. Does greater curvature imply greater normal acceleration?

From

$$
a_n=\frac{v^2}{R}
$$

for constant speed \(v\):

- smaller \(R\) → larger curvature  
- larger curvature → larger normal acceleration

So *yes*.

---

## 2. Where is the ellipse more curved?

At point \( (a,0) \):

$$
R=\frac{b^2}{a}
$$

At point \( (0,b) \):

$$
R=\frac{a^2}{b}
$$

If \(a>b\), then

$$
\frac{b^2}{a} < \frac{a^2}{b}
$$

So curvature is *greater at the ends of the major axis*.

---

## 3. Why does normal acceleration change direction?

Tangential acceleration changes *speed magnitude*.

Normal acceleration is perpendicular to velocity and therefore changes *direction of motion*.

Thus normal acceleration is responsible for bending the trajectory.

---

# Final results

Velocity:

$$
\vec v(t)=(-a\sin t,\; b\cos t)
$$

Acceleration:

$$
\vec a(t)=(-a\cos t,\; -b\sin t)
$$

Tangential acceleration:

$$
a_t=
\frac{(a^2-b^2)\sin t\cos t}
{\sqrt{a^2\sin^2 t+b^2\cos^2 t}}
$$

Normal acceleration:

$$
a_n=
\frac{ab}
{\sqrt{a^2\sin^2 t+b^2\cos^2 t}}
$$

Radius of curvature:

$$
R(0)=\frac{b^2}{a}
$$