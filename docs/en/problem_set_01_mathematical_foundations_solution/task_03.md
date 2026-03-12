# Problem 3 – Integration of motion

## A) For a given velocity

Given:

$$
\vec v(t) = (2t,3,-e^{-t}), \qquad \vec r(0)=(0,1,2)
$$

We need to determine:

$$
\vec r(t)=\vec r(0)+\int_0^t \vec v(\tau)\,d\tau
$$

and the acceleration \( \vec a(t) \).

---

## 1. Position vector \( \vec r(t) \)

Using the formula:

$$
\vec r(t)=\vec r(0)+\int_0^t \vec v(\tau)\,d\tau
$$

Substitute the velocity:

$$
\vec r(t)=(0,1,2)+\int_0^t (2\tau,3,-e^{-\tau})\,d\tau
$$

Integrate component by component:

$$
\int_0^t 2\tau\,d\tau = \left[\tau^2\right]_0^t=t^2
$$

$$
\int_0^t 3\,d\tau = \left[3\tau\right]_0^t=3t
$$

$$
\int_0^t -e^{-\tau}\,d\tau
=
\left[e^{-\tau}\right]_0^t
=
e^{-t}-1
$$

So:

$$
\vec r(t)=(0,1,2)+(t^2,3t,e^{-t}-1)
$$

Therefore:

$$
\vec r(t)=(t^2,1+3t,1+e^{-t})
$$

---

## 2. Acceleration vector \( \vec a(t) \)

Acceleration is the derivative of velocity:

$$
\vec a(t)=\frac{d\vec v(t)}{dt}
$$

Differentiate each component:

$$
\vec a(t)=\left(\frac{d}{dt}(2t),\frac{d}{dt}(3),\frac{d}{dt}(-e^{-t})\right)
$$

$$
\vec a(t)=(2,0,e^{-t})
$$

---

## Final answers for part A

$$
\vec r(t)=(t^2,1+3t,1+e^{-t})
$$

$$
\vec a(t)=(2,0,e^{-t})
$$

---

# B) For a given acceleration

Given:

$$
\vec a(t)=(4,-\sin t,0), \qquad \vec v(0)=(1,0,2), \qquad \vec r(0)=(0,0,0)
$$

We need to determine:

$$
\vec v(t)=\vec v(0)+\int_0^t \vec a(\tau)\,d\tau
$$

and

$$
\vec r(t)=\int_0^t \vec v(\tau)\,d\tau + \vec r(0)
$$

---

## 1. Velocity vector \( \vec v(t) \)

Using the formula:

$$
\vec v(t)=\vec v(0)+\int_0^t \vec a(\tau)\,d\tau
$$

Substitute the acceleration:

$$
\vec v(t)=(1,0,2)+\int_0^t (4,-\sin\tau,0)\,d\tau
$$

Integrate component by component:

$$
\int_0^t 4\,d\tau = \left[4\tau\right]_0^t = 4t
$$

$$
\int_0^t -\sin\tau\,d\tau
=
\left[\cos\tau\right]_0^t
=
\cos t - 1
$$

$$
\int_0^t 0\,d\tau = 0
$$

So:

$$
\vec v(t)=(1,0,2)+(4t,\cos t-1,0)
$$

Therefore:

$$
\vec v(t)=(1+4t,\cos t-1,2)
$$

---

## 2. Position vector \( \vec r(t) \)

Using:

$$
\vec r(t)=\int_0^t \vec v(\tau)\,d\tau+\vec r(0)
$$

Since \( \vec r(0)=(0,0,0) \), we get:

$$
\vec r(t)=\int_0^t (1+4\tau,\cos\tau-1,2)\,d\tau
$$

Integrate component by component:

### First component

$$
\int_0^t (1+4\tau)\,d\tau
=
\left[\tau+2\tau^2\right]_0^t
=
t+2t^2
$$

### Second component

$$
\int_0^t (\cos\tau-1)\,d\tau
=
\left[\sin\tau-\tau\right]_0^t
=
\sin t - t
$$

### Third component

$$
\int_0^t 2\,d\tau
=
\left[2\tau\right]_0^t
=
2t
$$

Therefore:

$$
\vec r(t)=(t+2t^2,\sin t - t,2t)
$$

---

## Final answers for part B

$$
\vec v(t)=(1+4t,\cos t-1,2)
$$

$$
\vec r(t)=(t+2t^2,\sin t-t,2t)
$$