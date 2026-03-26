
# Problem 4 – Circular motion

A body moves in a circle of radius (R) with angular velocity (\omega).

We need to determine:

* the position vector ( \vec r(t) ),
* the velocity vector ( \vec v(t) ),
* the acceleration vector ( \vec a(t) ),
* the magnitudes ( |\vec r(t)| ), ( |\vec v(t)| ), and ( |\vec a(t)| ),
* whether the acceleration is centripetal,
* the geometric meaning of the vectors ( \vec r ), ( \vec v ), and ( \vec a ).

---

## 1. Position vector ( \vec r(t) )

For uniform circular motion in the (xy)-plane, the angular position is

$$
\theta(t)=\omega t
$$

If the circle has radius (R), then the coordinates of the body are

$$
x(t)=R\cos(\omega t), \qquad y(t)=R\sin(\omega t)
$$

Therefore, the position vector is

$$
\vec r(t)=\bigl(R\cos(\omega t),,R\sin(\omega t)\bigr)
$$

---

## 2. Velocity vector ( \vec v(t) )

The velocity vector is the derivative of the position vector:

$$
\vec v(t)=\frac{d\vec r(t)}{dt}
$$

Differentiate each component.

### First component

$$
\frac{d}{dt}\bigl(R\cos(\omega t)\bigr)=-R\omega\sin(\omega t)
$$

### Second component

$$
\frac{d}{dt}\bigl(R\sin(\omega t)\bigr)=R\omega\cos(\omega t)
$$

Therefore,

$$
\vec v(t)=\bigl(-R\omega\sin(\omega t),,R\omega\cos(\omega t)\bigr)
$$

---

## 3. Acceleration vector ( \vec a(t) )

The acceleration vector is the derivative of the velocity vector:

$$
\vec a(t)=\frac{d\vec v(t)}{dt}
$$

Differentiate again.

### First component

$$
\frac{d}{dt}\bigl(-R\omega\sin(\omega t)\bigr)=-R\omega^2\cos(\omega t)
$$

### Second component

$$
\frac{d}{dt}\bigl(R\omega\cos(\omega t)\bigr)=-R\omega^2\sin(\omega t)
$$

Therefore,

$$
\vec a(t)=\bigl(-R\omega^2\cos(\omega t),,-R\omega^2\sin(\omega t)\bigr)
$$

---

## 4. Magnitude of the position vector

The magnitude of ( \vec r(t) ) is

$$
|\vec r(t)|=\sqrt{\bigl(R\cos(\omega t)\bigr)^2+\bigl(R\sin(\omega t)\bigr)^2}
$$

$$
|\vec r(t)|=\sqrt{R^2\cos^2(\omega t)+R^2\sin^2(\omega t)}
$$

Factor out (R^2):

$$
|\vec r(t)|=R\sqrt{\cos^2(\omega t)+\sin^2(\omega t)}
$$

Using ( \cos^2 x+\sin^2 x=1 ), we get

$$
|\vec r(t)|=R
$$

So:

$$
|\vec r(t)|=R
$$

---

## 5. Magnitude of the velocity vector

The magnitude of ( \vec v(t) ) is

$$
|\vec v(t)|=\sqrt{\bigl(-R\omega\sin(\omega t)\bigr)^2+\bigl(R\omega\cos(\omega t)\bigr)^2}
$$

$$
|\vec v(t)|=\sqrt{R^2\omega^2\sin^2(\omega t)+R^2\omega^2\cos^2(\omega t)}
$$

Factor out (R^2\omega^2):

$$
|\vec v(t)|=R\omega\sqrt{\sin^2(\omega t)+\cos^2(\omega t)}
$$

Using ( \sin^2 x+\cos^2 x=1 ), we obtain

$$
|\vec v(t)|=R\omega
$$

So:

$$
|\vec v(t)|=R\omega
$$

---

## 6. Magnitude of the acceleration vector

The magnitude of ( \vec a(t) ) is

$$
|\vec a(t)|=\sqrt{\bigl(-R\omega^2\cos(\omega t)\bigr)^2+\bigl(-R\omega^2\sin(\omega t)\bigr)^2}
$$

$$
|\vec a(t)|=\sqrt{R^2\omega^4\cos^2(\omega t)+R^2\omega^4\sin^2(\omega t)}
$$

Factor out (R^2\omega^4):

$$
|\vec a(t)|=R\omega^2\sqrt{\cos^2(\omega t)+\sin^2(\omega t)}
$$

Using ( \cos^2 x+\sin^2 x=1 ), we get

$$
|\vec a(t)|=R\omega^2
$$

So:

$$
|\vec a(t)|=R\omega^2
$$

---

## 7. Show that the acceleration is centripetal

From above,

$$
\vec a(t)=\bigl(-R\omega^2\cos(\omega t),,-R\omega^2\sin(\omega t)\bigr)
$$

Factor out ( -\omega^2 ):

$$
\vec a(t)=-\omega^2\bigl(R\cos(\omega t),,R\sin(\omega t)\bigr)
$$

But

$$
\bigl(R\cos(\omega t),,R\sin(\omega t)\bigr)=\vec r(t)
$$

Hence,

$$
\vec a(t)=-\omega^2\vec r(t)
$$

This shows that the acceleration vector always points in the direction opposite to the position vector.

Since the position vector points from the center of the circle to the body, the opposite direction points toward the center.

Therefore, the acceleration is **centripetal**.

Also, since ( |\vec v|=R\omega ), we have

$$
|\vec a|=R\omega^2=\frac{(R\omega)^2}{R}=\frac{|\vec v|^2}{R}
$$

So the centripetal acceleration formula is

$$
|\vec a|=\frac{v^2}{R}
$$

---

## 8. Geometric meaning of the vectors

In circular motion:

* ( \vec r(t) ) points from the center of the circle to the body,
* ( \vec v(t) ) is tangent to the circle,
* ( \vec a(t) ) points toward the center of the circle.

Thus:

$$
\vec v(t)\perp \vec r(t)
$$

and

$$
\vec a(t)\parallel -\vec r(t)
$$

This means the velocity is perpendicular to the radius, while the acceleration is directed inward.

---

## Final answers for Problem 4

$$
\vec r(t)=\bigl(R\cos(\omega t),,R\sin(\omega t)\bigr)
$$

$$
\vec v(t)=\bigl(-R\omega\sin(\omega t),,R\omega\cos(\omega t)\bigr)
$$

$$
\vec a(t)=\bigl(-R\omega^2\cos(\omega t),,-R\omega^2\sin(\omega t)\bigr)
$$

$$
|\vec r(t)|=R
$$

$$
|\vec v(t)|=R\omega
$$

$$
|\vec a(t)|=R\omega^2
$$

$$
\vec a(t)=-\omega^2\vec r(t)
$$

Therefore, the acceleration is centripetal.

Geometrically, ( \vec r ) is radial, ( \vec v ) is tangential, and ( \vec a ) points toward the center.

---


