# Problem 4 – Geometry of parametric curves

We investigate the following curves:

### A)
$$
x(t)=R\cos t, \qquad y(t)=R\sin t
$$

### B)
$$
x(t)=a\cos t, \qquad y(t)=b\sin t
$$

### C)
$$
x(t)=t, \qquad y(t)=t^2
$$

### D)
$$
x(t)=\cosh t, \qquad y(t)=\sinh t
$$

For each curve we:
1. eliminate the parameter if possible,
2. determine the type of curve,
3. compute the velocity \( \vec v(t) \) and acceleration \( \vec a(t) \),
4. check whether \( |\vec v| \) or \( |\vec a| \) is constant.

---

# A) \( x(t)=R\cos t,\; y(t)=R\sin t \)

## 1. Eliminate the parameter

Using the identity

$$
\cos^2 t+\sin^2 t=1
$$

we get

$$
\left(\frac{x}{R}\right)^2+\left(\frac{y}{R}\right)^2=1
$$

so

$$
x^2+y^2=R^2
$$

## 2. Type of curve

This is a **circle** of radius \( R \) centered at the origin.

## 3. Velocity and acceleration

Position vector:

$$
\vec r(t)=(R\cos t,\;R\sin t)
$$

Velocity:

$$
\vec v(t)=\frac{d\vec r}{dt}=(-R\sin t,\;R\cos t)
$$

Acceleration:

$$
\vec a(t)=\frac{d\vec v}{dt}=(-R\cos t,\;-R\sin t)
$$

## 4. Check magnitudes

Velocity magnitude:

$$
|\vec v|=\sqrt{(-R\sin t)^2+(R\cos t)^2}
$$

$$
|\vec v|=\sqrt{R^2\sin^2 t+R^2\cos^2 t}
$$

$$
|\vec v|=\sqrt{R^2}=R
$$

So \( |\vec v| \) is constant.

Acceleration magnitude:

$$
|\vec a|=\sqrt{(-R\cos t)^2+(-R\sin t)^2}
$$

$$
|\vec a|=\sqrt{R^2\cos^2 t+R^2\sin^2 t}
$$

$$
|\vec a|=R
$$

So \( |\vec a| \) is also constant.

---

# B) \( x(t)=a\cos t,\; y(t)=b\sin t \)

## 1. Eliminate the parameter

We write

$$
\cos t=\frac{x}{a}, \qquad \sin t=\frac{y}{b}
$$

Using

$$
\cos^2 t+\sin^2 t=1
$$

we get

$$
\left(\frac{x}{a}\right)^2+\left(\frac{y}{b}\right)^2=1
$$

## 2. Type of curve

This is an **ellipse** centered at the origin with semi-axes \( a \) and \( b \).

## 3. Velocity and acceleration

Position vector:

$$
\vec r(t)=(a\cos t,\;b\sin t)
$$

Velocity:

$$
\vec v(t)=(-a\sin t,\;b\cos t)
$$

Acceleration:

$$
\vec a(t)=(-a\cos t,\;-b\sin t)
$$

## 4. Check magnitudes

Velocity magnitude:

$$
|\vec v|=\sqrt{a^2\sin^2 t+b^2\cos^2 t}
$$

This is generally **not constant** unless \( a=b \).

Acceleration magnitude:

$$
|\vec a|=\sqrt{a^2\cos^2 t+b^2\sin^2 t}
$$

This is also generally **not constant** unless \( a=b \).

---

# C) \( x(t)=t,\; y(t)=t^2 \)

## 1. Eliminate the parameter

Since

$$
x=t
$$

we substitute into \( y=t^2 \):

$$
y=x^2
$$

## 2. Type of curve

This is a **parabola** opening upward.

## 3. Velocity and acceleration

Position vector:

$$
\vec r(t)=(t,\;t^2)
$$

Velocity:

$$
\vec v(t)=\left(\frac{d}{dt}t,\frac{d}{dt}t^2\right)=(1,\;2t)
$$

Acceleration:

$$
\vec a(t)=\left(0,\;2\right)
$$

## 4. Check magnitudes

Velocity magnitude:

$$
|\vec v|=\sqrt{1^2+(2t)^2}=\sqrt{1+4t^2}
$$

This is **not constant**.

Acceleration magnitude:

$$
|\vec a|=\sqrt{0^2+2^2}=2
$$

So \( |\vec a| \) **is constant**.

---

# D) \( x(t)=\cosh t,\; y(t)=\sinh t \)

## 1. Eliminate the parameter

Using the hyperbolic identity

$$
\cosh^2 t-\sinh^2 t=1
$$

we get

$$
x^2-y^2=1
$$

## 2. Type of curve

This is a **hyperbola**.

More precisely, it is the **right branch** of the hyperbola \( x^2-y^2=1 \), because \( \cosh t \ge 1 \).

## 3. Velocity and acceleration

Position vector:

$$
\vec r(t)=(\cosh t,\;\sinh t)
$$

Velocity:

$$
\vec v(t)=(\sinh t,\;\cosh t)
$$

Acceleration:

$$
\vec a(t)=(\cosh t,\;\sinh t)
$$

## 4. Check magnitudes

Velocity magnitude:

$$
|\vec v|=\sqrt{\sinh^2 t+\cosh^2 t}
$$

This is **not constant**.

Acceleration magnitude:

$$
|\vec a|=\sqrt{\cosh^2 t+\sinh^2 t}
$$

This is also **not constant**.

---

# Final summary

## Curve A
- Equation:
$$
x^2+y^2=R^2
$$
- Type: circle
- Velocity:
$$
\vec v(t)=(-R\sin t,\;R\cos t)
$$
- Acceleration:
$$
\vec a(t)=(-R\cos t,\;-R\sin t)
$$
- \( |\vec v| \): constant
- \( |\vec a| \): constant

## Curve B
- Equation:
$$
\frac{x^2}{a^2}+\frac{y^2}{b^2}=1
$$
- Type: ellipse
- Velocity:
$$
\vec v(t)=(-a\sin t,\;b\cos t)
$$
- Acceleration:
$$
\vec a(t)=(-a\cos t,\;-b\sin t)
$$
- \( |\vec v| \): not constant in general
- \( |\vec a| \): not constant in general

## Curve C
- Equation:
$$
y=x^2
$$
- Type: parabola
- Velocity:
$$
\vec v(t)=(1,\;2t)
$$
- Acceleration:
$$
\vec a(t)=(0,\;2)
$$
- \( |\vec v| \): not constant
- \( |\vec a| \): constant

## Curve D
- Equation:
$$
x^2-y^2=1
$$
- Type: hyperbola
- Velocity:
$$
\vec v(t)=(\sinh t,\;\cosh t)
$$
- Acceleration:
$$
\vec a(t)=(\cosh t,\;\sinh t)
$$
- \( |\vec v| \): not constant
- \( |\vec a| \): not constant