# Problem 6 – Cycloid: trajectory of a point on a rolling circle

Given:

$$
x(t)=R(\omega t-\sin(\omega t)), \qquad y(t)=R(1-\cos(\omega t))
$$

We need to determine:

* the velocity vector ( \vec v(t) ),
* the acceleration vector ( \vec a(t) ),
* the speed ( |\vec v(t)| ),
* the moments when the point stops relative to the ground,
* the maximum values of ( |\vec v| ) and ( |\vec a| ),
* an HTML animation of the rolling circle and the cycloid,
* the comparison with circular motion in the frame attached to the circle.

---

## 1. Velocity vector ( \vec v(t) )

The velocity is the derivative of position:

$$
\vec v(t)=\left(\frac{dx}{dt},\frac{dy}{dt}\right)
$$

We differentiate each coordinate.

### Derivative of ( x(t) )

$$
x(t)=R(\omega t-\sin(\omega t))
$$

So

$$
\frac{dx}{dt}=R\left(\omega-\omega\cos(\omega t)\right)
$$

$$
\frac{dx}{dt}=R\omega(1-\cos(\omega t))
$$

### Derivative of ( y(t) )

$$
y(t)=R(1-\cos(\omega t))
$$

So

$$
\frac{dy}{dt}=R\omega\sin(\omega t)
$$

Therefore the velocity vector is

$$
\vec v(t)=\big(R\omega(1-\cos(\omega t)),,R\omega\sin(\omega t)\big)
$$

---

## 2. Acceleration vector ( \vec a(t) )

The acceleration is the derivative of velocity:

$$
\vec a(t)=\left(\frac{d^2x}{dt^2},\frac{d^2y}{dt^2}\right)
$$

Differentiate the velocity components.

### Derivative of ( v_x(t) )

$$
v_x(t)=R\omega(1-\cos(\omega t))
$$

So

$$
\frac{dv_x}{dt}=R\omega^2\sin(\omega t)
$$

### Derivative of ( v_y(t) )

$$
v_y(t)=R\omega\sin(\omega t)
$$

So

$$
\frac{dv_y}{dt}=R\omega^2\cos(\omega t)
$$

Therefore the acceleration vector is

$$
\vec a(t)=\big(R\omega^2\sin(\omega t),,R\omega^2\cos(\omega t)\big)
$$

---

## 3. Magnitude of the velocity ( |\vec v(t)| )

We use

$$
|\vec v|=\sqrt{v_x^2+v_y^2}
$$

Substitute the components:

$$
|\vec v|=\sqrt{[R\omega(1-\cos(\omega t))]^2+[R\omega\sin(\omega t)]^2}
$$

Factor out ( R\omega ):

$$
|\vec v|=R\omega\sqrt{(1-\cos(\omega t))^2+\sin^2(\omega t)}
$$

Expand:

$$
(1-\cos(\omega t))^2+\sin^2(\omega t)
=1-2\cos(\omega t)+\cos^2(\omega t)+\sin^2(\omega t)
$$

Since

$$
\cos^2(\omega t)+\sin^2(\omega t)=1
$$

we get

$$
=2-2\cos(\omega t)
$$

Thus

$$
|\vec v|=R\omega\sqrt{2-2\cos(\omega t)}
$$

Using the identity

$$
2-2\cos\theta=4\sin^2\left(\frac{\theta}{2}\right)
$$

we obtain

$$
|\vec v|=2R\omega\left|\sin\left(\frac{\omega t}{2}\right)\right|
$$

Therefore:

$$
|\vec v(t)|=2R\omega\left|\sin\left(\frac{\omega t}{2}\right)\right|
$$

---

## 4. Moments when the point stops relative to the ground

The point stops when the velocity is zero:

$$
|\vec v|=0
$$

So

$$
2R\omega\left|\sin\left(\frac{\omega t}{2}\right)\right|=0
$$

Hence

$$
\sin\left(\frac{\omega t}{2}\right)=0
$$

This happens when

$$
\frac{\omega t}{2}=k\pi \qquad (k\in\mathbb Z)
$$

Therefore

$$
t=\frac{2k\pi}{\omega}
$$

So the point temporarily stops at

$$
t=\frac{2k\pi}{\omega}, \qquad k=0,1,2,\dots
$$

These are exactly the cusp points of the cycloid, when the point touches the ground.

---

## 5. Maximum value of ( |\vec v| )

We have

$$
|\vec v|=2R\omega\left|\sin\left(\frac{\omega t}{2}\right)\right|
$$

The maximum value of sine is 1, so

$$
|\vec v|_{\max}=2R\omega
$$

Thus

$$
\boxed{|\vec v|_{\max}=2R\omega}
$$

This occurs when

$$
\left|\sin\left(\frac{\omega t}{2}\right)\right|=1
$$

that is,

$$
\frac{\omega t}{2}=\frac{\pi}{2}+k\pi
$$

so

$$
t=\frac{(2k+1)\pi}{\omega}
$$

---

## 6. Magnitude of the acceleration ( |\vec a(t)| )

We use

$$
|\vec a|=\sqrt{a_x^2+a_y^2}
$$

Substitute the components:

$$
|\vec a|=\sqrt{(R\omega^2\sin(\omega t))^2+(R\omega^2\cos(\omega t))^2}
$$

Factor out ( R\omega^2 ):

$$
|\vec a|=R\omega^2\sqrt{\sin^2(\omega t)+\cos^2(\omega t)}
$$

Since

$$
\sin^2(\omega t)+\cos^2(\omega t)=1
$$

we get

$$
|\vec a|=R\omega^2
$$

Therefore:

$$
|\vec a(t)|=R\omega^2
$$

So the acceleration magnitude is constant.

---

## 7. Maximum value of ( |\vec a| )

Because ( |\vec a| ) is constant,

$$
|\vec a|_{\max}=R\omega^2
$$

Thus

$$
\boxed{|\vec a|_{\max}=R\omega^2}
$$

---

## 8. HTML animation

Below is a simple HTML file that shows:

* the rolling circle,
* the point on the rim,
* the cycloid trace,
* the velocity vector,
* the acceleration vector.



---

## 9. Comparison with circular motion in the frame attached to the circle

Now compare the motion in two reference frames.

### In the ground frame

In the fixed frame, the circle rolls along the ( x )-axis, and the point traces a cycloid:

$$
x(t)=R(\omega t-\sin(\omega t)), \qquad y(t)=R(1-\cos(\omega t))
$$

So the motion is not a circle. It is a cycloid with cusps.

### In the frame attached to the center of the circle

In the frame moving with the circle’s center, the translational motion is removed.

The center of the circle has coordinates

$$
x_C(t)=R\omega t, \qquad y_C(t)=R
$$

Relative to the center, the point has coordinates

$$
x'(t)=x(t)-x_C(t)=-R\sin(\omega t)
$$

$$
y'(t)=y(t)-R=-R\cos(\omega t)
$$

Therefore

$$
x'(t)^2+y'(t)^2=R^2
$$

So in this frame the point moves on a circle of radius ( R ).

Thus:

* in the ground frame: the trajectory is a **cycloid**,
* in the circle-attached frame: the trajectory is **uniform circular motion**.

The cycloid is therefore the result of combining:

* translation of the circle’s center,
* rotation of the point around the center.

---

## Final answers for Problem 6

$$
\vec v(t)=\big(R\omega(1-\cos(\omega t)),,R\omega\sin(\omega t)\big)
$$

$$
\vec a(t)=\big(R\omega^2\sin(\omega t),,R\omega^2\cos(\omega t)\big)
$$

$$
|\vec v(t)|=2R\omega\left|\sin\left(\frac{\omega t}{2}\right)\right|
$$

The point temporarily stops when

$$
t=\frac{2k\pi}{\omega}, \qquad k=0,1,2,\dots
$$

$$
|\vec v|_{\max}=2R\omega
$$

$$
|\vec a(t)|=R\omega^2
$$

$$
|\vec a|_{\max}=R\omega^2
$$

In the ground frame, the point traces a cycloid.

In the frame attached to the circle, the point performs circular motion of radius ( R ).

---

