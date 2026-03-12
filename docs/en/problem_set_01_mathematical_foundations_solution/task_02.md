# Problem 2 – Parametric trajectory, velocity, and acceleration

Given:

$$
\vec r(t)=(t^2,\sin t,5)
$$

We need to determine:

- the velocity \( \vec v(t) \),
- the acceleration \( \vec a(t) \),
- the value \( |\vec v(1)| \),
- the dot product \( \vec v\cdot\vec a \),
- the cross product \( \vec v\times\vec a \).

---

## 1. Velocity vector \( \vec v(t) \)

Velocity is the derivative of the position vector:

$$
\vec v(t)=\frac{d\vec r(t)}{dt}
$$

Differentiate each component of \( \vec r(t)=(t^2,\sin t,5) \):

$$
\frac{d}{dt}(t^2)=2t
$$

$$
\frac{d}{dt}(\sin t)=\cos t
$$

$$
\frac{d}{dt}(5)=0
$$

Therefore:

$$
\vec v(t)=(2t,\cos t,0)
$$

---

## 2. Acceleration vector \( \vec a(t) \)

Acceleration is the derivative of velocity:

$$
\vec a(t)=\frac{d\vec v(t)}{dt}
$$

Differentiate each component of \( \vec v(t)=(2t,\cos t,0) \):

$$
\frac{d}{dt}(2t)=2
$$

$$
\frac{d}{dt}(\cos t)=-\sin t
$$

$$
\frac{d}{dt}(0)=0
$$

Therefore:

$$
\vec a(t)=(2,-\sin t,0)
$$

---

## 3. Magnitude \( |\vec v(1)| \)

First compute \( \vec v(1) \):

$$
\vec v(1)=(2\cdot 1,\cos 1,0)=(2,\cos 1,0)
$$

Now calculate its magnitude:

$$
|\vec v(1)|=\sqrt{2^2+\cos^2 1+0^2}
$$

$$
|\vec v(1)|=\sqrt{4+\cos^2 1}
$$

Approximation:

$$
|\vec v(1)|\approx 2.07
$$

---

## 4. Dot product \( \vec v\cdot\vec a \)

We have

$$
\vec v(t)=(2t,\cos t,0), \qquad \vec a(t)=(2,-\sin t,0)
$$

Compute the dot product:

$$
\vec v\cdot\vec a=(2t)(2)+(\cos t)(-\sin t)+0\cdot 0
$$

$$
\vec v\cdot\vec a=4t-\sin t\cos t
$$

Therefore:

$$
\vec v\cdot\vec a=4t-\sin t\cos t
$$

---

## 5. Cross product \( \vec v\times\vec a \)

We compute the determinant:

$$
\vec v\times\vec a=
\begin{vmatrix}
\mathbf i & \mathbf j & \mathbf k\\
2t & \cos t & 0\\
2 & -\sin t & 0
\end{vmatrix}
$$

Expand along the first row:

$$
\vec v\times\vec a=
\mathbf i
\begin{vmatrix}
\cos t & 0\\
-\sin t & 0
\end{vmatrix}
-\mathbf j
\begin{vmatrix}
2t & 0\\
2 & 0
\end{vmatrix}
+\mathbf k
\begin{vmatrix}
2t & \cos t\\
2 & -\sin t
\end{vmatrix}
$$

Now calculate each component.

### \( \mathbf i \)-component

$$
\cos t\cdot 0-0\cdot(-\sin t)=0
$$

### \( \mathbf j \)-component

$$
2t\cdot 0-0\cdot 2=0
$$

### \( \mathbf k \)-component

$$
(2t)(-\sin t)-(\cos t)(2)=-2t\sin t-2\cos t
$$

Therefore:

$$
\vec v\times\vec a=(0,0,-2t\sin t-2\cos t)
$$

---

## Final answers for Problem 2

$$
\vec v(t)=(2t,\cos t,0)
$$

$$
\vec a(t)=(2,-\sin t,0)
$$

$$
|\vec v(1)|=\sqrt{4+\cos^2 1}\approx 2.07
$$

$$
\vec v\cdot\vec a=4t-\sin t\cos t
$$

$$
\vec v\times\vec a=(0,0,-2t\sin t-2\cos t)
$$