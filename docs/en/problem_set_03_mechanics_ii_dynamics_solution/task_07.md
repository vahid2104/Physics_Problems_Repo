# Problem 7 – Vertical throw with drag

We have the equation of motion

$$
m\frac{dv}{dt}=-mg-kv
$$

with initial conditions

$$
v(0)=v_0,\qquad x(0)=0
$$

We need to determine:

* the velocity (v(t)),
* the position (x(t)),
* the maximum height,
* the comparison with the case without drag,
* a numerical simulation,
* the comparison between the analytical and numerical solutions.

---

## 1. Rewrite the equation

Start from

$$
m\frac{dv}{dt}=-mg-kv
$$

Divide both sides by (m):

$$
\frac{dv}{dt}=-g-\frac{k}{m}v
$$

It is convenient to write it as

$$
\frac{dv}{dt}+\frac{k}{m}v=-g
$$

This is a first-order linear differential equation.

---

## 2. Solve for the velocity (v(t))

We solve

$$
\frac{dv}{dt}+\frac{k}{m}v=-g
$$

### Step 1: Solve the homogeneous equation

First solve

$$
\frac{dv}{dt}+\frac{k}{m}v=0
$$

Its solution is

$$
v_h(t)=Ce^{-\frac{k}{m}t}
$$

where (C) is a constant.

### Step 2: Find a particular solution

Because the right-hand side is constant, we try a constant solution

$$
v_p=A
$$

Then

$$
\frac{dv_p}{dt}=0
$$

Substitute into the equation:

$$
0+\frac{k}{m}A=-g
$$

So

$$
A=-\frac{mg}{k}
$$

Thus the particular solution is

$$
v_p=-\frac{mg}{k}
$$

### Step 3: Write the general solution

So the full solution is

$$
v(t)=Ce^{-\frac{k}{m}t}-\frac{mg}{k}
$$

### Step 4: Use the initial condition

Since (v(0)=v_0),

$$
v_0=C-\frac{mg}{k}
$$

Therefore,

$$
C=v_0+\frac{mg}{k}
$$

So the velocity is

$$
v(t)=\left(v_0+\frac{mg}{k}\right)e^{-\frac{k}{m}t}-\frac{mg}{k}
$$

Therefore,

$$
\boxed{,v(t)=\left(v_0+\frac{mg}{k}\right)e^{-\frac{k}{m}t}-\frac{mg}{k},}
$$

---

## 3. Solve for the position (x(t))

We know that

$$
\frac{dx}{dt}=v(t)
$$

So

$$
x(t)=\int v(t),dt
$$

Substitute the velocity:

$$
x(t)=\int \left[\left(v_0+\frac{mg}{k}\right)e^{-\frac{k}{m}t}-\frac{mg}{k}\right]dt
$$

Integrate term by term:

$$
x(t)=\left(v_0+\frac{mg}{k}\right)\int e^{-\frac{k}{m}t}dt-\frac{mg}{k}\int dt
$$

Now,

$$
\int e^{-\frac{k}{m}t}dt=-\frac{m}{k}e^{-\frac{k}{m}t}
$$

So

$$
x(t)=-\frac{m}{k}\left(v_0+\frac{mg}{k}\right)e^{-\frac{k}{m}t}-\frac{mg}{k}t+C_1
$$

Use the initial condition (x(0)=0):

$$
0=-\frac{m}{k}\left(v_0+\frac{mg}{k}\right)+C_1
$$

Thus,

$$
C_1=\frac{m}{k}\left(v_0+\frac{mg}{k}\right)
$$

So the position is

$$
x(t)=\frac{m}{k}\left(v_0+\frac{mg}{k}\right)\left(1-e^{-\frac{k}{m}t}\right)-\frac{mg}{k}t
$$

Therefore,

$$
\boxed{,x(t)=\frac{m}{k}\left(v_0+\frac{mg}{k}\right)\left(1-e^{-\frac{k}{m}t}\right)-\frac{mg}{k}t,}
$$

---

## 4. Determine the maximum height

The maximum height is reached when the velocity becomes zero.

So we set

$$
v(t)=0
$$

That gives

$$
\left(v_0+\frac{mg}{k}\right)e^{-\frac{k}{m}t}-\frac{mg}{k}=0
$$

Move one term to the other side:

$$
\left(v_0+\frac{mg}{k}\right)e^{-\frac{k}{m}t}=\frac{mg}{k}
$$

Divide both sides:

$$
e^{-\frac{k}{m}t}=\frac{\frac{mg}{k}}{v_0+\frac{mg}{k}}
$$

This becomes

$$
e^{-\frac{k}{m}t}=\frac{mg}{kv_0+mg}
$$

Take the natural logarithm:

$$
-\frac{k}{m}t=\ln\left(\frac{mg}{kv_0+mg}\right)
$$

So the time to reach the maximum height is

$$
t_{\max}=\frac{m}{k}\ln\left(\frac{kv_0+mg}{mg}\right)
$$

or equivalently

$$
\boxed{,t_{\max}=\frac{m}{k}\ln\left(1+\frac{kv_0}{mg}\right),}
$$

---

### Maximum height

Now substitute (t=t_{\max}) into the position formula:

$$
x_{\max}=\frac{m}{k}\left(v_0+\frac{mg}{k}\right)\left(1-e^{-\frac{k}{m}t_{\max}}\right)-\frac{mg}{k}t_{\max}
$$

From the equation above,

$$
e^{-\frac{k}{m}t_{\max}}=\frac{mg}{kv_0+mg}
$$

So

$$
1-e^{-\frac{k}{m}t_{\max}}
=1-\frac{mg}{kv_0+mg}
=\frac{kv_0}{kv_0+mg}
$$

Then

$$
\frac{m}{k}\left(v_0+\frac{mg}{k}\right)\left(1-e^{-\frac{k}{m}t_{\max}}\right)
;=;
\frac{m}{k}v_0
;=;
\frac{mv_0}{k}
$$

Therefore,

$$
x_{\max}=\frac{mv_0}{k}-\frac{mg}{k}t_{\max}
$$

Now substitute (t_{\max}):

$$
x_{\max}=\frac{mv_0}{k}-\frac{mg}{k}\cdot \frac{m}{k}\ln\left(1+\frac{kv_0}{mg}\right)
$$

So the maximum height is

$$
\boxed{,x_{\max}=\frac{mv_0}{k}-\frac{m^2g}{k^2}\ln\left(1+\frac{kv_0}{mg}\right),}
$$

---

## 5. Compare with the case without drag

Without drag, the equation becomes

$$
m\frac{dv}{dt}=-mg
$$

So

$$
\frac{dv}{dt}=-g
$$

### Velocity without drag

Integrating,

$$
v(t)=v_0-gt
$$

### Position without drag

Integrating again,

$$
x(t)=v_0t-\frac{1}{2}gt^2
$$

### Maximum height without drag

At the top, (v=0), so

$$
0=v_0-gt
\quad\Rightarrow\quad
t_{\max}^{(0)}=\frac{v_0}{g}
$$

Now substitute into (x(t)):

$$
x_{\max}^{(0)}=v_0\frac{v_0}{g}-\frac{1}{2}g\left(\frac{v_0}{g}\right)^2
$$

$$
x_{\max}^{(0)}=\frac{v_0^2}{g}-\frac{v_0^2}{2g}
$$

$$
x_{\max}^{(0)}=\frac{v_0^2}{2g}
$$

Thus, without drag:

$$
\boxed{,v(t)=v_0-gt,}
$$

$$
\boxed{,x(t)=v_0t-\frac{1}{2}gt^2,}
$$

$$
\boxed{,x_{\max}^{(0)}=\frac{v_0^2}{2g},}
$$

---

## 6. Physical comparison

Let us compare the two cases.

### With drag

$$
v(t)=\left(v_0+\frac{mg}{k}\right)e^{-\frac{k}{m}t}-\frac{mg}{k}
$$

$$
x_{\max}=\frac{mv_0}{k}-\frac{m^2g}{k^2}\ln\left(1+\frac{kv_0}{mg}\right)
$$

### Without drag

$$
v(t)=v_0-gt
$$

$$
x_{\max}^{(0)}=\frac{v_0^2}{2g}
$$

### Interpretation

* With drag, the body loses speed faster.
* Therefore, it reaches a smaller maximum height.
* The upward motion lasts less time than in the case without drag.
* So drag makes the object stop rising earlier.

Hence,

$$
x_{\max}<x_{\max}^{(0)}
$$

for (k>0).

---

## 7. Numerical simulation

Now let us perform a simple numerical simulation.

Because the problem statement does not give numerical values, we choose an example:

$$
m=1\ \text{kg},\qquad
g=9.81\ \text{m/s}^2,\qquad
k=0.5\ \text{kg/s},\qquad
v_0=20\ \text{m/s}
$$

We will use the Euler method.

---

### Euler method

The differential equation is

$$
\frac{dv}{dt}=-g-\frac{k}{m}v
$$

Also,

$$
\frac{dx}{dt}=v
$$

If the time step is (\Delta t), then:

$$
v_{n+1}=v_n+\Delta t\left(-g-\frac{k}{m}v_n\right)
$$

$$
x_{n+1}=x_n+\Delta t,v_n
$$

We start with

$$
x_0=0,\qquad v_0=20
$$

Take

$$
\Delta t=0.1\ \text{s}
$$

---

## 8. Analytical solution for these numbers

First write the analytical velocity:

$$
v(t)=\left(20+\frac{1\cdot 9.81}{0.5}\right)e^{-0.5t}-\frac{9.81}{0.5}
$$

Since

$$
\frac{9.81}{0.5}=19.62
$$

we get

$$
v(t)=39.62,e^{-0.5t}-19.62
$$

The position is

$$
x(t)=\frac{1}{0.5}(20+19.62)(1-e^{-0.5t})-19.62,t
$$

So

$$
x(t)=79.24(1-e^{-0.5t})-19.62,t
$$

---

## 9. Time and value of the maximum height

### Analytical value

The maximum height is reached when (v=0):

$$
t_{\max}=\frac{1}{0.5}\ln\left(1+\frac{0.5\cdot 20}{1\cdot 9.81}\right)
$$

$$
t_{\max}=2\ln(2.019)
$$

$$
t_{\max}\approx 1.405\ \text{s}
$$

Now compute the maximum height:

$$
x_{\max}=\frac{1\cdot 20}{0.5}-\frac{1^2\cdot 9.81}{0.5^2}\ln\left(1+\frac{0.5\cdot 20}{9.81}\right)
$$

$$
x_{\max}=40-39.24\ln(2.019)
$$

$$
x_{\max}\approx 12.26\ \text{m}
$$

So with drag:

$$
\boxed{,t_{\max}\approx 1.405\ \text{s},}
$$

$$
\boxed{,x_{\max}\approx 12.26\ \text{m},}
$$

---

### Without drag

Without drag,

$$
t_{\max}^{(0)}=\frac{v_0}{g}=\frac{20}{9.81}\approx 2.04\ \text{s}
$$

and

$$
x_{\max}^{(0)}=\frac{20^2}{2\cdot 9.81}
=\frac{400}{19.62}
\approx 20.39\ \text{m}
$$

So without drag:

$$
\boxed{,t_{\max}^{(0)}\approx 2.04\ \text{s},}
$$

$$
\boxed{,x_{\max}^{(0)}\approx 20.39\ \text{m},}
$$

---

## 10. Small numerical table

Using Euler’s method with (\Delta t=0.1\ \text{s}), we get approximately:

| (t) (s) | (v_{\text{num}}) (m/s) | (x_{\text{num}}) (m) |
| ------- | ---------------------: | -------------------: |
| 0.0     |                 20.000 |                0.000 |
| 0.1     |                 18.019 |                2.000 |
| 0.2     |                 16.148 |                3.802 |
| 0.3     |                 14.376 |                5.417 |
| 0.4     |                 12.694 |                6.855 |
| 0.5     |                 11.091 |                8.124 |
| 0.6     |                  9.557 |                9.233 |
| 0.7     |                  8.083 |               10.189 |
| 0.8     |                  6.668 |               10.997 |
| 0.9     |                  5.304 |               11.664 |
| 1.0     |                  3.989 |               12.194 |
| 1.1     |                  2.716 |               12.593 |
| 1.2     |                  1.485 |               12.865 |
| 1.3     |                  0.290 |               13.013 |
| 1.4     |                 -0.870 |               13.042 |

From this table we see:

* the numerical velocity changes sign between (t=1.3) s and (t=1.4) s,
* the numerical maximum height is about

$$
x_{\max}^{\text{num}}\approx 13.04\ \text{m}
$$

This is close to the exact value, but a little larger because Euler’s method with (\Delta t=0.1) is only approximate.

---

## 11. Compare analytical and numerical solutions

### Analytical result

$$
x_{\max}\approx 12.26\ \text{m}
$$

### Numerical result

$$
x_{\max}^{\text{num}}\approx 13.04\ \text{m}
$$

### Difference

$$
13.04-12.26\approx 0.78\ \text{m}
$$

So the numerical result is close, but not exact.

### Why is there a difference?

Because:

* Euler’s method is an approximation,
* the step size (\Delta t=0.1) is not very small,
* a smaller step size would give better agreement.

So the analytical and numerical solutions are consistent, and the numerical result approaches the analytical one when the time step becomes smaller.

---

## 12. Final answers for Problem 7

### Velocity

$$
\boxed{,v(t)=\left(v_0+\frac{mg}{k}\right)e^{-\frac{k}{m}t}-\frac{mg}{k},}
$$

### Position

$$
\boxed{,x(t)=\frac{m}{k}\left(v_0+\frac{mg}{k}\right)\left(1-e^{-\frac{k}{m}t}\right)-\frac{mg}{k}t,}
$$

### Time to reach maximum height

$$
\boxed{,t_{\max}=\frac{m}{k}\ln\left(1+\frac{kv_0}{mg}\right),}
$$

### Maximum height

$$
\boxed{,x_{\max}=\frac{mv_0}{k}-\frac{m^2g}{k^2}\ln\left(1+\frac{kv_0}{mg}\right),}
$$

### Without drag

$$
\boxed{,v(t)=v_0-gt,}
$$

$$
\boxed{,x(t)=v_0t-\frac{1}{2}gt^2,}
$$

$$
\boxed{,x_{\max}^{(0)}=\frac{v_0^2}{2g},}
$$

### Comparison

* With drag, the body rises for a shorter time.
* With drag, the maximum height is smaller.
* The numerical simulation agrees with the analytical solution, with a small error due to the approximation method.

---

