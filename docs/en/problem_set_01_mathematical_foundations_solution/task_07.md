# Problem 7 – Work of a force along a trajectory

Given force:

$$
\vec F(x,y)=(y,2x)
$$

Trajectory:

$$
x=t,\qquad y=t^2,\qquad t\in[0,1]
$$

We need to determine:

- the velocity vector \( \vec v(t) \),
- the work done by the force along the trajectory,
  $$
  W=\int_C \vec F\cdot d\vec r,
  $$
- the integral written as the limit of a Riemann sum,
- and its numerical value.

---

## 1. Position vector \( \vec r(t) \)

From the parametric equations

$$
x=t,\qquad y=t^2
$$

the position vector is

$$
\vec r(t)=(t,t^2)
$$

---

## 2. Velocity vector \( \vec v(t) \)

Velocity is the derivative of the position vector:

$$
\vec v(t)=\frac{d\vec r(t)}{dt}
$$

Differentiate each component:

$$
\frac{d}{dt}(t)=1
$$

$$
\frac{d}{dt}(t^2)=2t
$$

Therefore:

$$
\vec v(t)=(1,2t)
$$

---

## 3. Force along the trajectory

The force field is

$$
\vec F(x,y)=(y,2x)
$$

On the trajectory we have

$$
x=t,\qquad y=t^2
$$

So substitute these into the force:

$$
\vec F(\vec r(t))=\vec F(t,t^2)=(t^2,2t)
$$

Therefore, along the curve,

$$
\vec F(t)=(t^2,2t)
$$

---

## 4. Work integral

The work done by the force along the curve is

$$
W=\int_C \vec F\cdot d\vec r
$$

For a parametric curve \( \vec r(t) \), this becomes

$$
W=\int_0^1 \vec F(\vec r(t))\cdot \vec r'(t)\,dt
$$

We already found:

$$
\vec F(\vec r(t))=(t^2,2t)
$$

and

$$
\vec r'(t)=\vec v(t)=(1,2t)
$$

Now compute the dot product:

$$
\vec F(\vec r(t))\cdot \vec r'(t)
=
(t^2,2t)\cdot(1,2t)
$$

$$
\vec F(\vec r(t))\cdot \vec r'(t)
=
t^2\cdot 1 + 2t\cdot 2t
$$

$$
\vec F(\vec r(t))\cdot \vec r'(t)
=
t^2+4t^2=5t^2
$$

So the work is

$$
W=\int_0^1 5t^2\,dt
$$

---

## 5. Analytical calculation of the work

Now integrate:

$$
W=\int_0^1 5t^2\,dt
$$

Take the constant outside:

$$
W=5\int_0^1 t^2\,dt
$$

Use the antiderivative:

$$
\int t^2\,dt=\frac{t^3}{3}
$$

Therefore:

$$
W=5\left[\frac{t^3}{3}\right]_0^1
$$

Substitute the bounds:

$$
W=5\left(\frac{1^3}{3}-\frac{0^3}{3}\right)
$$

$$
W=5\cdot\frac13
$$

Therefore:

$$
W=\frac53
$$

---

## 6. Riemann sum form

We divide the interval \( [0,1] \) into \( N \) equal parts.

The step size is

$$
\Delta t=\frac{1}{N}
$$

Let

$$
t_i=\frac{i}{N},\qquad i=0,1,2,\dots,N
$$

Since the integrand is

$$
f(t)=5t^2
$$

the Riemann sum for the work can be written as

$$
W_N=\sum_{i=1}^{N} 5t_i^2\,\Delta t
$$

Substitute \( t_i=\frac{i}{N} \) and \( \Delta t=\frac{1}{N} \):

$$
W_N=\sum_{i=1}^{N} 5\left(\frac{i}{N}\right)^2\frac{1}{N}
$$

$$
W_N=\frac{5}{N^3}\sum_{i=1}^{N} i^2
$$

Using the formula

$$
\sum_{i=1}^{N} i^2=\frac{N(N+1)(2N+1)}{6}
$$

we get

$$
W_N=\frac{5}{N^3}\cdot\frac{N(N+1)(2N+1)}{6}
$$

$$
W_N=\frac{5(N+1)(2N+1)}{6N^2}
$$

As \( N\to\infty \),

$$
\lim_{N\to\infty} W_N=\frac53
$$

So the Riemann sum converges to the exact analytical value.

---

## 7. Numerical examples

For example, if \( N=10 \), then

$$
W_{10}=\frac{5(10+1)(2\cdot 10+1)}{6\cdot 10^2}
$$

$$
W_{10}=\frac{5\cdot 11\cdot 21}{600}
$$

$$
W_{10}=\frac{1155}{600}=1.925
$$

This is an approximation.

The exact value is

$$
\frac53\approx 1.6667
$$

For larger \( N \), the approximation gets closer to \( \frac53 \).

For example, for \( N=100 \):

$$
W_{100}=\frac{5(101)(201)}{6\cdot 100^2}\approx 1.69175
$$

which is much closer to the exact value.

---

## 8. Error of the numerical method

If \( W=\frac53 \) is the exact value and \( W_N \) is the numerical approximation, then the error is

$$
E_N=\left|W-W_N\right|
$$

So here:

$$
E_N=\left|\frac53-W_N\right|
$$

As \( N \) increases, this error tends to zero.

---

## Final answers for Problem 7

$$
\vec r(t)=(t,t^2)
$$

$$
\vec v(t)=\frac{d\vec r}{dt}=(1,2t)
$$

$$
\vec F(\vec r(t))=(t^2,2t)
$$

$$
W=\int_C \vec F\cdot d\vec r
=\int_0^1 \vec F(\vec r(t))\cdot \vec r'(t)\,dt
$$

$$
W=\int_0^1 5t^2\,dt
$$

$$
W=\frac53
$$

The Riemann sum form is

$$
W_N=\sum_{i=1}^{N} 5t_i^2\,\Delta t,
\qquad
t_i=\frac{i}{N},\quad \Delta t=\frac1N
$$

that is,

$$
W_N=\frac{5}{N^3}\sum_{i=1}^{N} i^2
$$

$$
W_N=\frac{5(N+1)(2N+1)}{6N^2}
$$

and

$$
\lim_{N\to\infty}W_N=\frac53
$$

The numerical error is

$$
E_N=\left|\frac53-W_N\right|
$$