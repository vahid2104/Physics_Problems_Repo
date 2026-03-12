# Problem 10 – Angular momentum in circular motion

Consider circular motion in the \(xy\) plane:

$$
\vec r(t)=\bigl(R\cos(\omega t),\,R\sin(\omega t),\,0\bigr)
$$

We need to determine:

- the velocity vector
  $$
  \vec v(t)=\dot{\vec r}(t),
  $$
- the angular momentum with respect to the origin
  $$
  \vec L(t)=m\,\vec r(t)\times\vec v(t),
  $$
- show that \( |\vec L|=mR^2\omega \) is constant,
- show that \( \vec L \) is perpendicular to the plane of motion,
- interpret the direction of \( \vec L \) using the right-hand rule,
- and optionally calculate the torque for a centripetal force and verify
  $$
  \vec\tau=\frac{d\vec L}{dt}.
  $$

---

## 1. Position vector \( \vec r(t) \)

The position vector is given directly:

$$
\vec r(t)=\bigl(R\cos(\omega t),\,R\sin(\omega t),\,0\bigr)
$$

This describes circular motion of radius \(R\) in the \(xy\)-plane.

---

## 2. Velocity vector \( \vec v(t) \)

Velocity is the derivative of the position vector:

$$
\vec v(t)=\frac{d\vec r(t)}{dt}
$$

Differentiate each component:

$$
\frac{d}{dt}\bigl(R\cos(\omega t)\bigr)=-R\omega\sin(\omega t)
$$

$$
\frac{d}{dt}\bigl(R\sin(\omega t)\bigr)=R\omega\cos(\omega t)
$$

$$
\frac{d}{dt}(0)=0
$$

Therefore:

$$
\vec v(t)=\bigl(-R\omega\sin(\omega t),\,R\omega\cos(\omega t),\,0\bigr)
$$

---

## 3. Angular momentum \( \vec L(t) \)

The angular momentum with respect to the origin is

$$
\vec L(t)=m\,\vec r(t)\times\vec v(t)
$$

Substitute the vectors:

$$
\vec r(t)=\bigl(R\cos(\omega t),\,R\sin(\omega t),\,0\bigr)
$$

$$
\vec v(t)=\bigl(-R\omega\sin(\omega t),\,R\omega\cos(\omega t),\,0\bigr)
$$

Now compute the cross product:

$$
\vec r(t)\times\vec v(t)=
\begin{vmatrix}
\mathbf i & \mathbf j & \mathbf k\\
R\cos(\omega t) & R\sin(\omega t) & 0\\
-R\omega\sin(\omega t) & R\omega\cos(\omega t) & 0
\end{vmatrix}
$$

Expand along the first row.

### \( \mathbf i \)-component

$$
R\sin(\omega t)\cdot 0 - 0\cdot R\omega\cos(\omega t)=0
$$

### \( \mathbf j \)-component

$$
R\cos(\omega t)\cdot 0 - 0\cdot\bigl(-R\omega\sin(\omega t)\bigr)=0
$$

### \( \mathbf k \)-component

$$
R\cos(\omega t)\cdot R\omega\cos(\omega t)
-
R\sin(\omega t)\cdot\bigl(-R\omega\sin(\omega t)\bigr)
$$

$$
=R^2\omega\cos^2(\omega t)+R^2\omega\sin^2(\omega t)
$$

$$
=R^2\omega\bigl(\cos^2(\omega t)+\sin^2(\omega t)\bigr)
$$

Using

$$
\cos^2(\omega t)+\sin^2(\omega t)=1
$$

we get

$$
\vec r(t)\times\vec v(t)=(0,0,R^2\omega)
$$

Therefore:

$$
\vec L(t)=m(0,0,R^2\omega)=(0,0,mR^2\omega)
$$

---

## 4. Magnitude of angular momentum

The magnitude of

$$
\vec L(t)=(0,0,mR^2\omega)
$$

is

$$
|\vec L|=\sqrt{0^2+0^2+(mR^2\omega)^2}
$$

$$
|\vec L|=mR^2\omega
$$

Therefore:

$$
|\vec L|=mR^2\omega
$$

This value does not depend on \(t\), so it is constant.

---

## 5. Why \( \vec L \) is perpendicular to the plane of motion

The particle moves in the \(xy\)-plane, so both \( \vec r(t) \) and \( \vec v(t) \) lie in the \(xy\)-plane.

The cross product of two vectors in the \(xy\)-plane is perpendicular to that plane.

Since

$$
\vec L(t)=(0,0,mR^2\omega),
$$

the angular momentum points along the \(z\)-axis.

So \( \vec L \) is perpendicular to the plane of motion.

---

## 6. Direction of \( \vec L \) – right-hand rule

To determine the direction of angular momentum, use the right-hand rule:

- point the fingers of your right hand in the direction of \( \vec r \),
- curl them toward \( \vec v \),
- your thumb shows the direction of \( \vec r\times\vec v \), hence also \( \vec L \).

In this case, for the motion

$$
\vec r(t)=\bigl(R\cos(\omega t),\,R\sin(\omega t),\,0\bigr),
$$

the motion is counterclockwise when viewed from the positive \(z\)-axis.

Therefore the angular momentum points in the positive \(z\)-direction:

$$
\vec L=(0,0,mR^2\omega)
$$

If the direction of rotation were reversed, the angular momentum would point in the negative \(z\)-direction.

---

## 7. Optional part – centripetal force

For uniform circular motion, the centripetal acceleration is directed toward the center:

$$
\vec a(t)=-\omega^2\vec r(t)
$$

So the force is

$$
\vec F(t)=m\vec a(t)=-m\omega^2\vec r(t)
$$

Substitute \( \vec r(t) \):

$$
\vec F(t)=\bigl(-m\omega^2R\cos(\omega t),\,-m\omega^2R\sin(\omega t),\,0\bigr)
$$

This force is always parallel to \( \vec r(t) \), but in the opposite direction.

---

## 8. Torque \( \vec\tau=\vec r\times\vec F \)

Torque is defined by

$$
\vec\tau=\vec r\times\vec F
$$

Since \( \vec F(t)=-m\omega^2\vec r(t) \), the vectors \( \vec r(t) \) and \( \vec F(t) \) are parallel.

The cross product of parallel vectors is zero, so:

$$
\vec\tau=\vec 0
$$

Therefore:

$$
\vec\tau=(0,0,0)
$$

---

## 9. Verify \( \vec\tau=\dfrac{d\vec L}{dt} \)

We found

$$
\vec L(t)=(0,0,mR^2\omega)
$$

This vector is constant, so its derivative is

$$
\frac{d\vec L}{dt}=(0,0,0)
$$

From the previous section we also found

$$
\vec\tau=(0,0,0)
$$

Therefore:

$$
\vec\tau=\frac{d\vec L}{dt}
$$

So the relation is verified for uniform circular motion.

---

## Final answers for Problem 10

$$
\vec r(t)=\bigl(R\cos(\omega t),\,R\sin(\omega t),\,0\bigr)
$$

$$
\vec v(t)=\bigl(-R\omega\sin(\omega t),\,R\omega\cos(\omega t),\,0\bigr)
$$

$$
\vec L(t)=m\,\vec r(t)\times\vec v(t)=(0,0,mR^2\omega)
$$

$$
|\vec L|=mR^2\omega
$$

The vector \( \vec L \) is constant and perpendicular to the plane of motion.

For counterclockwise motion in the \(xy\)-plane, \( \vec L \) points in the positive \(z\)-direction.

For the centripetal force

$$
\vec F(t)=-m\omega^2\vec r(t),
$$

the torque is

$$
\vec\tau=\vec r\times\vec F=(0,0,0)
$$

and

$$
\frac{d\vec L}{dt}=(0,0,0),
$$

so indeed

$$
\vec\tau=\frac{d\vec L}{dt}.
$$