# Problem 7 – 2D motion with a given acceleration

Given:

$$
\vec a=(2,-3)
$$

with initial conditions

$$
\vec v(0)=(1,0), \qquad \vec r(0)=(0,0)
$$

We need to determine:

* the velocity vector ( \vec v(t) ),
* the position vector ( \vec r(t) ),
* the trajectory,
* and describe the velocity and acceleration vectors at selected moments.

---

## 1. Given acceleration

The acceleration is constant:

$$
\vec a=(2,-3)
$$

This means

$$
\vec a=\vec r,''(t)=\vec v,'(t)
$$

So the derivative of velocity is constant.

---

## 2. Determine the velocity vector ( \vec v(t) )

Since acceleration is the derivative of velocity, we integrate:

$$
\vec v,'(t)=(2,-3)
$$

Integrating componentwise:

$$
\vec v(t)=(2t+C_1,,-3t+C_2)
$$

Now use the initial condition

$$
\vec v(0)=(1,0)
$$

Substitute ( t=0 ):

$$
\vec v(0)=(C_1,C_2)=(1,0)
$$

So

$$
C_1=1,\qquad C_2=0
$$

Therefore:

$$
\vec v(t)=(2t+1,,-3t)
$$

---

## 3. Determine the position vector ( \vec r(t) )

Now integrate the velocity:

$$
\vec r,'(t)=\vec v(t)=(2t+1,,-3t)
$$

Integrating componentwise:

$$
\vec r(t)=\left(t^2+t+C_3,,-\frac{3}{2}t^2+C_4\right)
$$

Use the initial condition

$$
\vec r(0)=(0,0)
$$

Substitute ( t=0 ):

$$
\vec r(0)=(C_3,C_4)=(0,0)
$$

So

$$
C_3=0,\qquad C_4=0
$$

Therefore:

$$
\vec r(t)=\left(t^2+t,,-\frac{3}{2}t^2\right)
$$

---

## 4. Final formulas

### Velocity

$$
\vec v(t)=(2t+1,,-3t)
$$

### Position

$$
\vec r(t)=\left(t^2+t,,-\frac{3}{2}t^2\right)
$$

---

## 5. Determine the trajectory

Let

$$
x(t)=t^2+t
$$

$$
y(t)=-\frac{3}{2}t^2
$$

We want the relation between ( x ) and ( y ).

From

$$
y=-\frac{3}{2}t^2
$$

we get

$$
t^2=-\frac{2}{3}y
$$

Also,

$$
x=t^2+t
$$

So the trajectory is given parametrically by

$$
x=t^2+t,\qquad y=-\frac{3}{2}t^2
$$

This is a parabola-shaped path in the plane.

---

## 6. Values at a few selected moments

### At ( t=0 )

Position:

$$
\vec r(0)=(0,0)
$$

Velocity:

$$
\vec v(0)=(1,0)
$$

Acceleration:

$$
\vec a=(2,-3)
$$

So at ( t=0 ), the particle starts at the origin, moving to the right, while acceleration points right and downward.

---

### At ( t=1 )

Position:

$$
\vec r(1)=\left(1^2+1,,-\frac{3}{2}\cdot 1^2\right)=\left(2,-\frac{3}{2}\right)
$$

Velocity:

$$
\vec v(1)=(2\cdot 1+1,,-3\cdot 1)=(3,-3)
$$

Acceleration:

$$
\vec a=(2,-3)
$$

---

### At ( t=2 )

Position:

$$
\vec r(2)=\left(2^2+2,,-\frac{3}{2}\cdot 2^2\right)=(6,-6)
$$

Velocity:

$$
\vec v(2)=(2\cdot 2+1,,-3\cdot 2)=(5,-6)
$$

Acceleration:

$$
\vec a=(2,-3)
$$

---

## 7. Interpretation of the motion

* The acceleration is constant and always equal to

$$
(2,-3)
$$

* So the particle is continuously accelerated to the right and downward.
* The velocity changes linearly with time:

$$
\vec v(t)=(2t+1,-3t)
$$

* The position changes quadratically with time:

$$
\vec r(t)=\left(t^2+t,-\frac{3}{2}t^2\right)
$$

Thus the path is a parabola.

---

## Final answers for Problem 7

$$
\vec v(t)=(2t+1,,-3t)
$$

$$
\vec r(t)=\left(t^2+t,,-\frac{3}{2}t^2\right)
$$

Trajectory:

$$
x(t)=t^2+t,\qquad y(t)=-\frac{3}{2}t^2
$$

Selected values:

$$
t=0:\quad \vec r(0)=(0,0),\quad \vec v(0)=(1,0),\quad \vec a=(2,-3)
$$

$$
t=1:\quad \vec r(1)=\left(2,-\frac{3}{2}\right),\quad \vec v(1)=(3,-3),\quad \vec a=(2,-3)
$$

$$
t=2:\quad \vec r(2)=(6,-6),\quad \vec v(2)=(5,-6),\quad \vec a=(2,-3)
$$

---

I can also format this into a cleaner homework-style version with a tiny ASCII sketch of the trajectory.
