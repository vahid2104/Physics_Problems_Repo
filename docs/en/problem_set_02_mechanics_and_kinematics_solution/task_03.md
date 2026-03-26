# Problem 3 – Elimination of time and interpretation of acceleration

Given the parametric equations

$$
x(t)=2t^2, \qquad y(t)=3t^3
$$

We need to determine:

- the Cartesian equation of the trajectory by eliminating the parameter \( t \),
- the shape of the trajectory,
- the velocity vector \( \vec v(t) \) and its magnitude \( |\vec v(t)| \),
- the acceleration vector \( \vec a(t) \) and its magnitude \( |\vec a(t)| \),
- whether the acceleration is constant.

---

## 1. Eliminate the parameter \( t \)

We start from

$$
x=2t^2
$$

Hence,

$$
t^2=\frac{x}{2}
$$

Now take the equation

$$
y=3t^3
$$

and square both sides:

$$
y^2=9t^6
$$

Since

$$
t^6=(t^2)^3
$$

we substitute \( t^2=\frac{x}{2} \):

$$
t^6=\left(\frac{x}{2}\right)^3
$$

Therefore,

$$
y^2=9\left(\frac{x}{2}\right)^3
$$

$$
y^2=\frac{9}{8}x^3
$$

So the Cartesian equation of the trajectory is

$$
y^2=\frac{9}{8}x^3
$$

---

## 2. Shape of the trajectory

The trajectory is given by

$$
y^2=\frac{9}{8}x^3
$$

This curve is a **semicubical parabola**.

We note that

$$
x=2t^2 \ge 0
$$

for all \( t \), so the curve exists only for \( x\ge 0 \).

Also, since

$$
y=3t^3
$$

the value of \( y \) can be positive, negative, or zero.

Therefore:

- the curve passes through the origin \( (0,0) \),
- it exists only on the right side of the plane,
- it is symmetric with respect to the \( x \)-axis.

So the trajectory is a semicubical parabola opening to the right.

---

## 3. Velocity vector \( \vec v(t) \)

The velocity vector is the derivative of the position:

$$
\vec v(t)=\left(\frac{dx}{dt},\frac{dy}{dt}\right)
$$

Differentiate each coordinate.

### \( x \)-component

$$
\frac{dx}{dt}=\frac{d}{dt}(2t^2)=4t
$$

### \( y \)-component

$$
\frac{dy}{dt}=\frac{d}{dt}(3t^3)=9t^2
$$

Therefore,

$$
\vec v(t)=(4t,9t^2)
$$

---

## 4. Magnitude of the velocity

The speed is the magnitude of the velocity vector:

$$
|\vec v(t)|=\sqrt{(4t)^2+(9t^2)^2}
$$

$$
|\vec v(t)|=\sqrt{16t^2+81t^4}
$$

We can also factor out \( t^2 \):

$$
|\vec v(t)|=\sqrt{t^2(16+81t^2)}
$$

$$
|\vec v(t)|=|t|\sqrt{16+81t^2}
$$

So,

$$
|\vec v(t)|=\sqrt{16t^2+81t^4}=|t|\sqrt{16+81t^2}
$$

---

## 5. Acceleration vector \( \vec a(t) \)

The acceleration vector is the derivative of the velocity:

$$
\vec a(t)=\left(\frac{d^2x}{dt^2},\frac{d^2y}{dt^2}\right)
$$

Differentiate again.

### \( x \)-component

$$
\frac{d^2x}{dt^2}=\frac{d}{dt}(4t)=4
$$

### \( y \)-component

$$
\frac{d^2y}{dt^2}=\frac{d}{dt}(9t^2)=18t
$$

Therefore,

$$
\vec a(t)=(4,18t)
$$

---

## 6. Magnitude of the acceleration

The magnitude of the acceleration vector is

$$
|\vec a(t)|=\sqrt{4^2+(18t)^2}
$$

$$
|\vec a(t)|=\sqrt{16+324t^2}
$$

So,

$$
|\vec a(t)|=\sqrt{16+324t^2}
$$

---

## 7. Is the acceleration constant?

To be constant, the acceleration vector must not depend on \( t \).

But we found

$$
\vec a(t)=(4,18t)
$$

The second component depends on \( t \), so the acceleration vector changes with time.

Also, its magnitude is

$$
|\vec a(t)|=\sqrt{16+324t^2}
$$

which also depends on \( t \).

Therefore, the acceleration is **not constant**.

---

## Final answers for Problem 3

$$
y^2=\frac{9}{8}x^3
$$

The trajectory is a semicubical parabola opening to the right.

$$
\vec v(t)=(4t,9t^2)
$$

$$
|\vec v(t)|=\sqrt{16t^2+81t^4}=|t|\sqrt{16+81t^2}
$$

$$
\vec a(t)=(4,18t)
$$

$$
|\vec a(t)|=\sqrt{16+324t^2}
$$

The acceleration is not constant.

---