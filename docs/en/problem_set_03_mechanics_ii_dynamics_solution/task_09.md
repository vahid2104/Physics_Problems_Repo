Of course — here is **Problem 9** written in the same **basic, step-by-step style** as your Problem 1.

---

# Problem 9 – Potential and conservative field

Given the potential energy

$$
U(x,y)=\frac{k}{2}(x^2+y^2)
$$

We need to determine:

* the force as the gradient of the potential,
* the equations of motion,
* the type of motion,
* the total energy,
* the geometric interpretation of the trajectory.

---

## 1. Force from the potential

In mechanics, the force is related to the potential energy by

$$
\vec F=-\nabla U
$$

This means we take the partial derivatives of (U(x,y)) with respect to (x) and (y), and then add the minus sign.

The potential is

$$
U(x,y)=\frac{k}{2}(x^2+y^2)
$$

### Partial derivative with respect to (x)

$$
\frac{\partial U}{\partial x}=\frac{k}{2}\cdot 2x=kx
$$

### Partial derivative with respect to (y)

$$
\frac{\partial U}{\partial y}=\frac{k}{2}\cdot 2y=ky
$$

So the gradient is

$$
\nabla U=(kx,ky)
$$

Therefore the force is

$$
\vec F=-\nabla U=-(kx,ky)
$$

So

$$
\vec F=(-kx,-ky)
$$

Therefore,

$$
\boxed{\vec F(x,y)=(-kx,-ky)}
$$

---

## 2. Equations of motion

From Newton’s second law,

$$
m\vec a=\vec F
$$

Since

$$
\vec a=(\ddot x,\ddot y)
$$

we get

$$
m(\ddot x,\ddot y)=(-kx,-ky)
$$

So the motion in each coordinate satisfies:

$$
m\ddot x=-kx
$$

$$
m\ddot y=-ky
$$

or equivalently,

$$
\ddot x+\frac{k}{m}x=0
$$

$$
\ddot y+\frac{k}{m}y=0
$$

Therefore, the equations of motion are

$$
\boxed{\ddot x+\frac{k}{m}x=0}
$$

$$
\boxed{\ddot y+\frac{k}{m}y=0}
$$

---

## 3. Solve the equations of motion

Both equations have the same form. They are the equations of a harmonic oscillator.

Let

$$
\omega=\sqrt{\frac{k}{m}}
$$

Then the equations become

$$
\ddot x+\omega^2 x=0
$$

$$
\ddot y+\omega^2 y=0
$$

The general solutions are

$$
x(t)=A\cos(\omega t)+B\sin(\omega t)
$$

$$
y(t)=C\cos(\omega t)+D\sin(\omega t)
$$

where (A,B,C,D) are constants determined by the initial conditions.

Therefore,

$$
\boxed{x(t)=A\cos(\omega t)+B\sin(\omega t)}
$$

$$
\boxed{y(t)=C\cos(\omega t)+D\sin(\omega t)}
$$

with

$$
\boxed{\omega=\sqrt{\frac{k}{m}}}
$$

---

## 4. Type of motion

Since both (x(t)) and (y(t)) satisfy harmonic oscillator equations, the body performs **oscillatory motion** in both directions.

This is called a **two-dimensional harmonic oscillator**.

### Main idea

* Along the (x)-axis, the motion is simple harmonic.
* Along the (y)-axis, the motion is also simple harmonic.
* Together, the motion in the plane is a combination of two oscillations.

Because both oscillations have the same angular frequency

$$
\omega=\sqrt{\frac{k}{m}}
$$

the trajectory is generally a **closed curve**.

### Geometric form of the trajectory

Depending on the initial conditions, the path can be:

* an **ellipse**,
* a **circle** (special case),
* a **straight line through the origin** (special case).

So the type of motion is:

$$
\boxed{\text{two-dimensional simple harmonic motion}}
$$

and geometrically the trajectory is usually

$$
\boxed{\text{an ellipse centered at the origin}}
$$

---

## 5. Total energy

The total mechanical energy is

$$
E=T+U
$$

where:

* (T) is the kinetic energy,
* (U) is the potential energy.

### Kinetic energy

The velocity is

$$
\vec v=(\dot x,\dot y)
$$

So the kinetic energy is

$$
T=\frac{1}{2}m(\dot x^2+\dot y^2)
$$

### Potential energy

It is given in the problem:

$$
U=\frac{k}{2}(x^2+y^2)
$$

Therefore the total energy is

$$
E=\frac{1}{2}m(\dot x^2+\dot y^2)+\frac{k}{2}(x^2+y^2)
$$

So

$$
\boxed{E=\frac{1}{2}m(\dot x^2+\dot y^2)+\frac{k}{2}(x^2+y^2)}
$$

Since the force comes from a potential, it is a **conservative force**, so the total energy remains constant.

Therefore,

$$
\boxed{E=\text{constant}}
$$

---

## 6. Why the field is conservative

A force field is conservative if it comes from a potential.

Here,

$$
\vec F=-\nabla U
$$

so it is automatically conservative.

That means:

* the work depends only on the initial and final points,
* the total mechanical energy is conserved.

Thus,

$$
\boxed{\vec F=(-kx,-ky)\text{ is a conservative force field}}
$$

---

## 7. Geometric interpretation of the trajectory

The potential energy is

$$
U(x,y)=\frac{k}{2}(x^2+y^2)
$$

Notice that it depends only on

$$
x^2+y^2
$$

which is the square of the distance from the origin.

This means:

* the origin is the equilibrium point,
* the farther the body is from the origin, the larger the potential energy,
* the force always points toward the origin.

So this is like a restoring force pulling the particle back to the center.

### Geometric meaning

* The particle oscillates around the origin.
* In the plane, the orbit is usually an ellipse.
* If the amplitudes are equal and the phase shift is suitable, the orbit becomes a circle.
* If the motion in (x) and (y) stays proportional, the orbit becomes a straight line.

---

## Final answers for Problem 9

The force is

$$
\boxed{\vec F(x,y)=(-kx,-ky)}
$$

The equations of motion are

$$
\boxed{\ddot x+\frac{k}{m}x=0}
$$

$$
\boxed{\ddot y+\frac{k}{m}y=0}
$$

The solutions are

$$
\boxed{x(t)=A\cos(\omega t)+B\sin(\omega t)}
$$

$$
\boxed{y(t)=C\cos(\omega t)+D\sin(\omega t)}
$$

with

$$
\boxed{\omega=\sqrt{\frac{k}{m}}}
$$

The type of motion is

$$
\boxed{\text{two-dimensional harmonic motion}}
$$

The total energy is

$$
\boxed{E=\frac{1}{2}m(\dot x^2+\dot y^2)+\frac{k}{2}(x^2+y^2)}
$$

and it is constant.

Geometrically, the trajectory is usually

$$
\boxed{\text{an ellipse centered at the origin}}
$$

with special cases of a circle or a straight line.

---

## HTML/JS application

I also made a simple **HTML/JS app** for the trajectory visualization in the canvas on the side. It lets you change:

* (k)
* (m)
* initial position
* initial velocity
* time range

and it draws the trajectory.



