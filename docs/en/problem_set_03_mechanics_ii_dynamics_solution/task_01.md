
# Problem 1 – Newton’s second law (constant force)

A constant force acts on a body of mass

$$
m=2\ \text{kg}
$$

The force is

$$
\vec F=(6,2)\ \text{N}
$$

The initial velocity is

$$
\vec v(0)=(1,-1)\ \text{m/s}
$$

and the initial position is

$$
\vec r(0)=(0,0)\ \text{m}
$$

We need to determine:

* the acceleration $\vec a(t)$,
* the velocity $\vec v(t)$,
* the position $\vec r(t)$,
* the trajectory of the motion,
* the work done by the force at time $t=3\ \text{s}$,
* the consistency with the work–energy theorem.

---

## 1. Acceleration

From Newton’s second law,

$$
\vec F=m\vec a
$$

So the acceleration is

$$
\vec a=\frac{\vec F}{m}
$$

Substitute the given values:

$$
\vec a=\frac{(6,2)}{2}
$$

$$
\vec a=(3,1)\ \text{m/s}^2
$$

Since the force is constant, the acceleration is also constant.

Therefore,

$$
\vec a(t)=(3,1)\ \text{m/s}^2
$$

---

## 2. Velocity

The velocity is obtained by integrating the acceleration:

$$
\vec v(t)=\vec v(0)+\vec a,t
$$

Substitute the known values:

$$
\vec v(t)=(1,-1)+(3,1)t
$$

So

$$
\vec v(t)=(1+3t,,-1+t)
$$

Therefore,

$$
\vec v(t)=(1+3t,,-1+t)\ \text{m/s}
$$

---

## 3. Position

The position is obtained by integrating the velocity:

$$
\vec r(t)=\vec r(0)+\vec v(0)t+\frac{1}{2}\vec a,t^2
$$

Substitute the given values:

$$
\vec r(t)=(0,0)+(1,-1)t+\frac{1}{2}(3,1)t^2
$$

So

$$
\vec r(t)=\left(t+\frac{3}{2}t^2,,-t+\frac{1}{2}t^2\right)
$$

Therefore,

$$
\vec r(t)=\left(t+\frac{3}{2}t^2,,-t+\frac{1}{2}t^2\right)\ \text{m}
$$

---

## 4. Trajectory of the motion

The position components are

$$
x(t)=t+\frac{3}{2}t^2
$$

$$
y(t)=-t+\frac{1}{2}t^2
$$

To describe the trajectory, we look at how the body moves in the plane.

### Basic shape of the motion

Let us calculate a few points.

At $t=0$:

$$
x(0)=0,\qquad y(0)=0
$$

So the body starts at

$$
(0,0)
$$

At $t=1$:

$$
x(1)=1+\frac{3}{2}=\frac{5}{2}
$$

$$
y(1)=-1+\frac{1}{2}=-\frac{1}{2}
$$

So one point is

$$
\left(\frac{5}{2},-\frac{1}{2}\right)
$$

At $t=2$:

$$
x(2)=2+\frac{3}{2}\cdot 4=2+6=8
$$

$$
y(2)=-2+\frac{1}{2}\cdot 4=-2+2=0
$$

So another point is

$$
(8,0)
$$

At $t=3$:

$$
x(3)=3+\frac{3}{2}\cdot 9=3+\frac{27}{2}=\frac{33}{2}
$$

$$
y(3)=-3+\frac{1}{2}\cdot 9=-3+\frac{9}{2}=\frac{3}{2}
$$

So another point is

$$
\left(\frac{33}{2},\frac{3}{2}\right)
$$

### Description of the graph

* The body starts at the origin.
* At first it moves downward because the initial vertical velocity is negative.
* Then it turns upward because the vertical acceleration is positive.
* The trajectory is a curved line in the plane.
* Its shape is a parabola.

---

## 5. Work done by the force at time $t=3\ \text{s}$

The work done by a constant force is

$$
W=\vec F\cdot \Delta \vec r
$$

First find the displacement at $t=3$.

From the position function:

$$
\vec r(3)=\left(3+\frac{3}{2}\cdot 9,,-3+\frac{1}{2}\cdot 9\right)
$$

$$
\vec r(3)=\left(3+\frac{27}{2},,-3+\frac{9}{2}\right)
$$

$$
\vec r(3)=\left(\frac{33}{2},\frac{3}{2}\right)
$$

Since the initial position is $(0,0)$, the displacement is

$$
\Delta \vec r=\left(\frac{33}{2},\frac{3}{2}\right)
$$

Now calculate the dot product:

$$
W=(6,2)\cdot \left(\frac{33}{2},\frac{3}{2}\right)
$$

$$
W=6\cdot \frac{33}{2}+2\cdot \frac{3}{2}
$$

$$
W=99+3
$$

$$
W=102\ \text{J}
$$

Therefore, the work done by the force at time $t=3\ \text{s}$ is

$$
W=102\ \text{J}
$$

---

## 6. Check the work–energy theorem

The work–energy theorem says

$$
W=\Delta E_k
$$

where $E_k$ is the kinetic energy.

### Initial kinetic energy

The initial velocity is

$$
\vec v(0)=(1,-1)
$$

Its magnitude squared is

$$
|\vec v(0)|^2=1^2+(-1)^2=2
$$

So the initial kinetic energy is

$$
E_{k0}=\frac{1}{2}m|\vec v(0)|^2
$$

$$
E_{k0}=\frac{1}{2}\cdot 2\cdot 2
$$

$$
E_{k0}=2\ \text{J}
$$

### Kinetic energy at $t=3$

From the velocity formula,

$$
\vec v(t)=(1+3t,,-1+t)
$$

At $t=3$:

$$
\vec v(3)=(10,2)
$$

Its magnitude squared is

$$
|\vec v(3)|^2=10^2+2^2=100+4=104
$$

So the kinetic energy at $t=3$ is

$$
E_k(3)=\frac{1}{2}m|\vec v(3)|^2
$$

$$
E_k(3)=\frac{1}{2}\cdot 2\cdot 104
$$

$$
E_k(3)=104\ \text{J}
$$

Now calculate the change in kinetic energy:

$$
\Delta E_k=E_k(3)-E_{k0}
$$

$$
\Delta E_k=104-2
$$

$$
\Delta E_k=102\ \text{J}
$$

We obtained before

$$
W=102\ \text{J}
$$

Thus,

$$
W=\Delta E_k
$$

So the result is consistent with the work–energy theorem.

---

## Final answers for Problem 1

$$
\vec a(t)=(3,1)\ \text{m/s}^2
$$

$$
\vec v(t)=(1+3t,,-1+t)\ \text{m/s}
$$

$$
\vec r(t)=\left(t+\frac{3}{2}t^2,,-t+\frac{1}{2}t^2\right)\ \text{m}
$$

At time $t=3\ \text{s}$, the work done by the force is

$$
W=102\ \text{J}
$$

The change in kinetic energy is

$$
\Delta E_k=102\ \text{J}
$$

Therefore, the work–energy theorem is satisfied:

$$
W=\Delta E_k
$$

The trajectory is a parabola in the plane. It starts at $(0,0)$, first goes downward, and then upward.

---

