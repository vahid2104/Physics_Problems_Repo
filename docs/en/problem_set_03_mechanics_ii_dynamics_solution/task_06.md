
---

# Problem 6 – Motion with linear drag

The drag force is

$$
F=-kv
$$

Initial conditions:

$$
v(0)=v_0,\qquad x(0)=0
$$

We need to determine:

* the equation of motion and solve it,
* the limit $\lim_{t\to\infty} v(t)$,
* the comparison with motion without drag.

---

## 1. Equation of motion

From Newton’s second law,

$$
m\frac{dv}{dt}=F
$$

Here the force is the drag force

$$
F=-kv
$$

So the equation of motion is

$$
m\frac{dv}{dt}=-kv
$$

Divide both sides by $m$:

$$
\frac{dv}{dt}=-\frac{k}{m}v
$$

This is a first-order differential equation.

---

## 2. Solve for the velocity (v(t))

We solve

$$
\frac{dv}{dt}=-\frac{k}{m}v
$$

by separating variables.

Move all terms with $v$ to one side:

$$
\frac{dv}{v}=-\frac{k}{m},dt
$$

Now integrate both sides:

$$
\int \frac{1}{v},dv=\int -\frac{k}{m},dt
$$

This gives

$$
\ln |v|=-\frac{k}{m}t+C
$$

where $C$ is a constant.

Now exponentiate both sides:

$$
|v|=e^C e^{-\frac{k}{m}t}
$$

We combine the constant $e^C$ into a new constant $C_1$:

$$
v(t)=C_1 e^{-\frac{k}{m}t}
$$

Now use the initial condition

$$
v(0)=v_0
$$

Substitute $t=0$:

$$
v_0=C_1 e^0=C_1
$$

So

$$
C_1=v_0
$$

Therefore, the velocity is

$$
v(t)=v_0 e^{-\frac{k}{m}t}
$$

---

## 3. Solve for the position (x(t))

We know that

$$
\frac{dx}{dt}=v(t)
$$

So

$$
\frac{dx}{dt}=v_0 e^{-\frac{k}{m}t}
$$

Now integrate:

$$
x(t)=\int v_0 e^{-\frac{k}{m}t},dt
$$

Take out the constant $v_0$:

$$
x(t)=v_0\int e^{-\frac{k}{m}t},dt
$$

The integral is

$$
\int e^{-\frac{k}{m}t},dt
=-\frac{m}{k}e^{-\frac{k}{m}t}+C
$$

So

$$
x(t)=-\frac{mv_0}{k}e^{-\frac{k}{m}t}+C
$$

Now use the initial condition

$$
x(0)=0
$$

Substitute $t=0$:

$$
0=-\frac{mv_0}{k}+C
$$

Hence

$$
C=\frac{mv_0}{k}
$$

Therefore,

$$
x(t)=\frac{mv_0}{k}\left(1-e^{-\frac{k}{m}t}\right)
$$

So the position is

$$
x(t)=\frac{mv_0}{k}\left(1-e^{-\frac{k}{m}t}\right)
$$

---

## 4. Investigate the limit of (v(t)) as (t\to\infty)

We found

$$
v(t)=v_0 e^{-\frac{k}{m}t}
$$

Now look at the limit:

$$
\lim_{t\to\infty} v(t)
=\lim_{t\to\infty} v_0 e^{-\frac{k}{m}t}
$$

Since $e^{-\frac{k}{m}t}\to 0$ as $t\to\infty$, we get

$$
\lim_{t\to\infty} v(t)=0
$$

Therefore, the velocity goes to zero as time increases.

### Physical meaning

The drag force always acts opposite to the motion, so it slows the body down.

Over a long time, the body approaches rest.

---

## 5. What happens to the position for large time?

From

$$
x(t)=\frac{mv_0}{k}\left(1-e^{-\frac{k}{m}t}\right)
$$

take the limit as $t\to\infty$:

$$
\lim_{t\to\infty} x(t)
=\frac{mv_0}{k}(1-0)
$$

So

$$
\lim_{t\to\infty} x(t)=\frac{mv_0}{k}
$$

This means the body does **not** travel forever.

It approaches a finite final position:

$$
x_{\infty}=\frac{mv_0}{k}
$$

---

## 6. Compare with motion without drag

### Case A: motion with drag

With drag force

$$
F=-kv
$$

we found

$$
v(t)=v_0 e^{-\frac{k}{m}t}
$$

and

$$
x(t)=\frac{mv_0}{k}\left(1-e^{-\frac{k}{m}t}\right)
$$

So:

* the velocity decreases exponentially,
* the velocity tends to zero,
* the position approaches a finite value.

---

### Case B: motion without drag

Without drag, the force is zero:

$$
F=0
$$

Then Newton’s second law gives

$$
m\frac{dv}{dt}=0
$$

So

$$
\frac{dv}{dt}=0
$$

This means the velocity is constant:

$$
v(t)=v_0
$$

Now integrate to find position:

$$
x(t)=x(0)+v_0 t
$$

Since $x(0)=0$,

$$
x(t)=v_0 t
$$

So without drag:

* the velocity remains constant,
* the body never slows down,
* the position increases linearly with time,
* the body keeps moving forever.

---

## 7. Main difference between the two motions

### With drag:

$$
v(t)=v_0 e^{-\frac{k}{m}t}
$$

The speed decreases and eventually becomes zero.

### Without drag:

$$
v(t)=v_0
$$

The speed stays constant forever.

So drag causes the motion to die out, while without drag the motion continues uniformly.

---

## Final answers for Problem 6

The equation of motion is

$$
m\frac{dv}{dt}=-kv
$$

or equivalently

$$
\frac{dv}{dt}=-\frac{k}{m}v
$$

Its solution is

$$
v(t)=v_0 e^{-\frac{k}{m}t}
$$

The position is

$$
x(t)=\frac{mv_0}{k}\left(1-e^{-\frac{k}{m}t}\right)
$$

The velocity limit is

$$
\lim_{t\to\infty} v(t)=0
$$

So the body eventually comes to rest.

Without drag, the motion is

$$
v(t)=v_0,\qquad x(t)=v_0 t
$$

Thus:

* **with drag:** velocity decreases exponentially and the body approaches a finite position,
* **without drag:** velocity remains constant and the body moves forever in a straight line.

---

