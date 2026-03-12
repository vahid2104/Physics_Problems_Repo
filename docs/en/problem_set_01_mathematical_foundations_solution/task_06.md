# Problem 6 – Curve length and numerical integration

Given the parametric trajectory in 2D:

$$
x(t)=t,\qquad y(t)=t^2,\qquad t\in[0,1]
$$

We need to determine:

- the velocity vector
  $$
  \vec v(t)=\frac{d\vec r}{dt},
  $$
- the magnitude of the velocity \( |\vec v(t)| \),
- the arc length
  $$
  s=\int_0^1 |\vec v(t)|\,dt,
  $$
- the analytical value of this integral (if possible),
- and the numerical approximation using the trapezoidal rule.

---

## 1. Position vector \( \vec r(t) \)

From the parametric equations

$$
x(t)=t,\qquad y(t)=t^2
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

## 3. Magnitude of the velocity \( |\vec v(t)| \)

The magnitude of the vector \( \vec v(t)=(1,2t) \) is

$$
|\vec v(t)|=\sqrt{1^2+(2t)^2}
$$

$$
|\vec v(t)|=\sqrt{1+4t^2}
$$

Therefore:

$$
|\vec v(t)|=\sqrt{1+4t^2}
$$

---

## 4. Arc length of the trajectory

The arc length of a parametric curve is given by

$$
s=\int_0^1 |\vec v(t)|\,dt
$$

Substitute \( |\vec v(t)|=\sqrt{1+4t^2} \):

$$
s=\int_0^1 \sqrt{1+4t^2}\,dt
$$

So the problem reduces to calculating

$$
s=\int_0^1 \sqrt{1+4t^2}\,dt
$$

---

## 5. Analytical calculation of the integral

We use the standard formula

$$
\int \sqrt{1+4t^2}\,dt
=
\frac{t}{2}\sqrt{1+4t^2}+\frac{1}{4}\operatorname{arsinh}(2t)+C
$$

Now evaluate from \( 0 \) to \( 1 \):

$$
s=
\left[
\frac{t}{2}\sqrt{1+4t^2}+\frac{1}{4}\operatorname{arsinh}(2t)
\right]_0^1
$$

Substitute \( t=1 \):

$$
\frac{1}{2}\sqrt{1+4\cdot 1^2}+\frac{1}{4}\operatorname{arsinh}(2)
=
\frac{\sqrt5}{2}+\frac{1}{4}\operatorname{arsinh}(2)
$$

Substitute \( t=0 \):

$$
\frac{0}{2}\sqrt{1+0}+\frac{1}{4}\operatorname{arsinh}(0)=0
$$

Therefore:

$$
s=\frac{\sqrt5}{2}+\frac{1}{4}\operatorname{arsinh}(2)
$$

Since

$$
\operatorname{arsinh}(2)=\ln(2+\sqrt5)
$$

we can also write

$$
s=\frac{\sqrt5}{2}+\frac{1}{4}\ln(2+\sqrt5)
$$

---

## 6. Numerical value

Now approximate:

$$
\sqrt5\approx 2.23607
$$

$$
\ln(2+\sqrt5)\approx \ln(4.23607)\approx 1.44364
$$

So:

$$
s\approx \frac{2.23607}{2}+\frac{1.44364}{4}
$$

$$
s\approx 1.11803+0.36091
$$

$$
s\approx 1.47894
$$

Therefore:

$$
s\approx 1.47894
$$

---

## 7. Trapezoidal rule

To approximate the integral numerically, divide the interval \( [0,1] \) into \( N \) equal parts.

The step size is

$$
h=\frac{1-0}{N}=\frac{1}{N}
$$

The nodes are

$$
t_i=ih,\qquad i=0,1,2,\dots,N
$$

Define the function

$$
f(t)=\sqrt{1+4t^2}
$$

Then the trapezoidal-rule approximation is

$$
s_N
=
\frac{h}{2}
\left[
f(t_0)+2\sum_{i=1}^{N-1}f(t_i)+f(t_N)
\right]
$$

Substitute \( f(t)=\sqrt{1+4t^2} \):

$$
s_N
=
\frac{h}{2}
\left[
\sqrt{1+4t_0^2}
+
2\sum_{i=1}^{N-1}\sqrt{1+4t_i^2}
+
\sqrt{1+4t_N^2}
\right]
$$

where

$$
t_i=\frac{i}{N}
$$

---

## 8. Error of the numerical method

If \( s \) is the exact value and \( s_N \) is the trapezoidal approximation, then the error is

$$
E_N=|s-s_N|
$$

In this problem, the exact value is

$$
s=\frac{\sqrt5}{2}+\frac14\ln(2+\sqrt5)
$$

So the error can be written as

$$
E_N=
\left|
\frac{\sqrt5}{2}+\frac14\ln(2+\sqrt5)-s_N
\right|
$$

When \( N \) increases, the trapezoidal approximation should converge to the exact value, so \( E_N\to 0 \).

---

## Final answers for Problem 6

$$
\vec r(t)=(t,t^2)
$$

$$
\vec v(t)=\frac{d\vec r}{dt}=(1,2t)
$$

$$
|\vec v(t)|=\sqrt{1+4t^2}
$$

$$
s=\int_0^1\sqrt{1+4t^2}\,dt
$$

$$
s=\frac{\sqrt5}{2}+\frac14\operatorname{arsinh}(2)
$$

$$
s=\frac{\sqrt5}{2}+\frac14\ln(2+\sqrt5)
$$

$$
s\approx 1.47894
$$

The trapezoidal-rule approximation is

$$
s_N
=
\frac{h}{2}
\left[
f(t_0)+2\sum_{i=1}^{N-1}f(t_i)+f(t_N)
\right],
\qquad
f(t)=\sqrt{1+4t^2},
\quad h=\frac1N
$$

and the numerical error is

$$
E_N=|s-s_N|
$$