# Problem 5 – Elliptical motion (purely kinematic)

Given:

$$
x(t)=a\cos(\omega t), \qquad y(t)=b\sin(\omega t)
$$

We need to determine:

* the velocity,
* the acceleration,
* whether the magnitude of the velocity is constant,
* where the velocity is maximum,
* the trajectory,
* and the graphs of ( |\vec v(t)| ) and ( |\vec a(t)| ).

---

## 1. Position vector

The position vector is

$$
\vec r(t)=\bigl(x(t),y(t)\bigr)
$$

Substitute the given functions:

$$
\vec r(t)=\bigl(a\cos(\omega t),,b\sin(\omega t)\bigr)
$$

---

## 2. Velocity

Velocity is the derivative of the position vector with respect to time:

$$
\vec v(t)=\frac{d\vec r}{dt}
$$

So we differentiate each component.

### ( x )-component of velocity

$$
v_x(t)=\frac{dx}{dt}=\frac{d}{dt}\bigl(a\cos(\omega t)\bigr)
$$

Using the chain rule:

$$
v_x(t)=-a\omega\sin(\omega t)
$$

### ( y )-component of velocity

$$
v_y(t)=\frac{dy}{dt}=\frac{d}{dt}\bigl(b\sin(\omega t)\bigr)
$$

Again using the chain rule:

$$
v_y(t)=b\omega\cos(\omega t)
$$

Therefore:

$$
\vec v(t)=\bigl(-a\omega\sin(\omega t),,b\omega\cos(\omega t)\bigr)
$$

---

## 3. Acceleration

Acceleration is the derivative of velocity with respect to time:

$$
\vec a(t)=\frac{d\vec v}{dt}
$$

Differentiate each component.

### ( x )-component of acceleration

$$
a_x(t)=\frac{dv_x}{dt}=\frac{d}{dt}\bigl(-a\omega\sin(\omega t)\bigr)
$$

$$
a_x(t)=-a\omega^2\cos(\omega t)
$$

### ( y )-component of acceleration

$$
a_y(t)=\frac{dv_y}{dt}=\frac{d}{dt}\bigl(b\omega\cos(\omega t)\bigr)
$$

$$
a_y(t)=-b\omega^2\sin(\omega t)
$$

Therefore:

$$
\vec a(t)=\bigl(-a\omega^2\cos(\omega t),,-b\omega^2\sin(\omega t)\bigr)
$$

---

## 4. Magnitude of the velocity

The magnitude of velocity is

$$
|\vec v(t)|=\sqrt{v_x^2+v_y^2}
$$

Substitute the components:

$$
|\vec v(t)|=\sqrt{\bigl(-a\omega\sin(\omega t)\bigr)^2+\bigl(b\omega\cos(\omega t)\bigr)^2}
$$

$$
|\vec v(t)|=\sqrt{a^2\omega^2\sin^2(\omega t)+b^2\omega^2\cos^2(\omega t)}
$$

Factor out ( \omega^2 ):

$$
|\vec v(t)|=\omega\sqrt{a^2\sin^2(\omega t)+b^2\cos^2(\omega t)}
$$

So:

$$
|\vec v(t)|=\omega\sqrt{a^2\sin^2(\omega t)+b^2\cos^2(\omega t)}
$$

---

## 5. Is the magnitude of the velocity constant?

In general, the speed depends on ( t ), since

$$
|\vec v(t)|=\omega\sqrt{a^2\sin^2(\omega t)+b^2\cos^2(\omega t)}
$$

So the magnitude of the velocity is **not constant** in general.

It becomes constant only in the special case

$$
a=b
$$

Then the ellipse becomes a circle, and

$$
|\vec v(t)|=\omega\sqrt{a^2\sin^2(\omega t)+a^2\cos^2(\omega t)}
$$

$$
|\vec v(t)|=\omega\sqrt{a^2\bigl(\sin^2(\omega t)+\cos^2(\omega t)\bigr)}
$$

$$
|\vec v(t)|=\omega\sqrt{a^2}=\omega a
$$

Therefore, the speed is constant only when ( a=b ).

---

## 6. Where is the velocity maximum?

To find where the speed is maximum, we maximize

$$
|\vec v(t)|=\omega\sqrt{a^2\sin^2(\omega t)+b^2\cos^2(\omega t)}
$$

Since ( \omega ) and the square root are monotonic, it is enough to maximize

$$
a^2\sin^2(\omega t)+b^2\cos^2(\omega t)
$$

There are two cases.

### Case 1: ( a>b )

The coefficient of ( \sin^2(\omega t) ) is larger, so the maximum occurs when

$$
\sin^2(\omega t)=1, \qquad \cos^2(\omega t)=0
$$

That means

$$
\omega t=\frac{\pi}{2},\frac{3\pi}{2},\dots
$$

At these times,

$$
x=a\cos(\omega t)=0, \qquad y=b\sin(\omega t)=\pm b
$$

So the maximum speed occurs at

$$
(0,\pm b)
$$

and its value is

$$
|\vec v|_{\max}=a\omega
$$

### Case 2: ( b>a )

Now the coefficient of ( \cos^2(\omega t) ) is larger, so the maximum occurs when

$$
\cos^2(\omega t)=1, \qquad \sin^2(\omega t)=0
$$

That means

$$
\omega t=0,\pi,2\pi,\dots
$$

At these times,

$$
x=a\cos(\omega t)=\pm a, \qquad y=b\sin(\omega t)=0
$$

So the maximum speed occurs at

$$
(\pm a,0)
$$

and its value is

$$
|\vec v|_{\max}=b\omega
$$

### General result

Therefore:

$$
|\vec v|_{\max}=\omega\max(a,b)
$$

---

## 7. Magnitude of the acceleration

The magnitude of acceleration is

$$
|\vec a(t)|=\sqrt{a_x^2+a_y^2}
$$

Substitute the components:

$$
|\vec a(t)|=\sqrt{\bigl(-a\omega^2\cos(\omega t)\bigr)^2+\bigl(-b\omega^2\sin(\omega t)\bigr)^2}
$$

$$
|\vec a(t)|=\sqrt{a^2\omega^4\cos^2(\omega t)+b^2\omega^4\sin^2(\omega t)}
$$

Factor out ( \omega^4 ):

$$
|\vec a(t)|=\omega^2\sqrt{a^2\cos^2(\omega t)+b^2\sin^2(\omega t)}
$$

So:

$$
|\vec a(t)|=\omega^2\sqrt{a^2\cos^2(\omega t)+b^2\sin^2(\omega t)}
$$

---

## 8. Trajectory

We eliminate the parameter ( t ).

From

$$
x(t)=a\cos(\omega t)
$$

we get

$$
\frac{x}{a}=\cos(\omega t)
$$

From

$$
y(t)=b\sin(\omega t)
$$

we get

$$
\frac{y}{b}=\sin(\omega t)
$$

Now square both equations and add:

$$
\frac{x^2}{a^2}+\frac{y^2}{b^2}=\cos^2(\omega t)+\sin^2(\omega t)
$$

Using the identity

$$
\cos^2(\omega t)+\sin^2(\omega t)=1
$$

we obtain

$$
\frac{x^2}{a^2}+\frac{y^2}{b^2}=1
$$

Therefore, the trajectory is an ellipse:

$$
\frac{x^2}{a^2}+\frac{y^2}{b^2}=1
$$

---

## 9. Graphs of ( |\vec v(t)| ) and ( |\vec a(t)| )

### Graph of ( |\vec v(t)| )

We found

$$
|\vec v(t)|=\omega\sqrt{a^2\sin^2(\omega t)+b^2\cos^2(\omega t)}
$$

This is a periodic function of time.

Its minimum value is

$$
|\vec v|_{\min}=\omega\min(a,b)
$$

and its maximum value is

$$
|\vec v|_{\max}=\omega\max(a,b)
$$

So the graph oscillates periodically between these two values.

### Graph of ( |\vec a(t)| )

We found

$$
|\vec a(t)|=\omega^2\sqrt{a^2\cos^2(\omega t)+b^2\sin^2(\omega t)}
$$

This is also periodic.

Its minimum value is

$$
|\vec a|_{\min}=\omega^2\min(a,b)
$$

and its maximum value is

$$
|\vec a|_{\max}=\omega^2\max(a,b)
$$

So this graph also oscillates periodically between its minimum and maximum values.

---

## Final answers for Problem 5

$$
\vec v(t)=\bigl(-a\omega\sin(\omega t),,b\omega\cos(\omega t)\bigr)
$$

$$
\vec a(t)=\bigl(-a\omega^2\cos(\omega t),,-b\omega^2\sin(\omega t)\bigr)
$$

$$
|\vec v(t)|=\omega\sqrt{a^2\sin^2(\omega t)+b^2\cos^2(\omega t)}
$$

The magnitude of the velocity is not constant unless ( a=b ).

$$
|\vec v|_{\max}=\omega\max(a,b)
$$

If ( a>b ), the maximum occurs at

$$
(0,\pm b)
$$

If ( b>a ), the maximum occurs at

$$
(\pm a,0)
$$

$$
|\vec a(t)|=\omega^2\sqrt{a^2\cos^2(\omega t)+b^2\sin^2(\omega t)}
$$

$$
\frac{x^2}{a^2}+\frac{y^2}{b^2}=1
$$

The trajectory is an ellipse.

---
