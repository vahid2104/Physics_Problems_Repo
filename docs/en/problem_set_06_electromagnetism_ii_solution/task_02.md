# Problem 2 – Velocity selection with crossed fields

We have crossed electric and magnetic fields:

$$
\vec E=(0,E,0)
$$

$$
\vec B=(0,0,B)
$$

This means:

* electric field points in the **positive y-direction**
* magnetic field points in the **positive z-direction**
* the particle moves through both fields

We need to find when the particle moves in a straight line.

---

## Given data

The electric field is

$$
E=400\ \mathrm{V/m}
$$

The magnetic field is

$$
B=0.8\ \mathrm{T}
$$

The electric field vector is

$$
\vec E=(0,E,0)
$$

The magnetic field vector is

$$
\vec B=(0,0,B)
$$

The Lorentz force is

$$
\vec F=q(\vec E+\vec v\times \vec B)
$$

where:

* $q$ is the particle charge,
* $\vec E$ is the electric field,
* $\vec v$ is the particle velocity,
* $\vec B$ is the magnetic field.

---

# 1. Condition for rectilinear motion

Rectilinear motion means **straight-line motion**.

For the particle to move in a straight line, the total force must be zero:

$$
\vec F=0
$$

Using Lorentz force:

$$
q(\vec E+\vec v\times \vec B)=0
$$

Since $q\neq 0$, we can divide by $q$:

$$
\vec E+\vec v\times \vec B=0
$$

Therefore:

$$
\vec E=-(\vec v\times \vec B)
$$

This means the electric force and magnetic force must cancel each other.

---

## Direction of velocity

Assume the particle moves along the x-axis:

$$
\vec v=(v,0,0)
$$

The magnetic field is:

$$
\vec B=(0,0,B)
$$

Now calculate the cross product:

$$
\vec v\times \vec B
===================

(v,0,0)\times(0,0,B)
$$

Using the cross product formula:

$$
\vec v\times \vec B=(v_yB_z-v_zB_y,\ v_zB_x-v_xB_z,\ v_xB_y-v_yB_x)
$$

Substitute:

$$
v_x=v,\quad v_y=0,\quad v_z=0
$$

and

$$
B_x=0,\quad B_y=0,\quad B_z=B
$$

So:

$$
\vec v\times \vec B=(0\cdot B-0\cdot 0,\ 0\cdot 0-vB,\ v\cdot 0-0\cdot 0)
$$

Therefore:

$$
\vec v\times \vec B=(0,-vB,0)
$$

The electric field is:

$$
\vec E=(0,E,0)
$$

So the total field part is:

$$
\vec E+\vec v\times \vec B=(0,E,0)+(0,-vB,0)
$$

$$
\vec E+\vec v\times \vec B=(0,E-vB,0)
$$

For straight-line motion:

$$
\vec E+\vec v\times \vec B=0
$$

So:

$$
E-vB=0
$$

Therefore:

$$
E=vB
$$

Now solve for velocity:

$$
v=\frac{E}{B}
$$

So the condition for rectilinear motion is:

$$
\boxed{v_d=\frac{E}{B}}
$$

This velocity is called the **drift velocity** or **selected velocity**.

---

# 2. Calculate $v_d$ for $E=400\ \mathrm{V/m}$ and $B=0.8\ \mathrm{T}$

We use:

$$
v_d=\frac{E}{B}
$$

Substitute the values:

$$
v_d=\frac{400}{0.8}
$$

Calculate:

$$
v_d=500\ \mathrm{m/s}
$$

Therefore:

$$
\boxed{v_d=500\ \mathrm{m/s}}
$$

So only particles moving with velocity

$$
500\ \mathrm{m/s}
$$

will pass through in a straight line.

---

# 3. Does the kinetic energy change in steady motion?

Kinetic energy is:

$$
K=\frac{1}{2}mv^2
$$

If the particle moves steadily in a straight line, its velocity does not change.

So:

$$
v=\text{constant}
$$

Therefore:

$$
K=\text{constant}
$$

So the kinetic energy does **not** change.

---

## Why?

In steady motion, the total force is zero:

$$
\vec F=0
$$

That means there is no acceleration:

$$
\vec a=0
$$

So the particle does not speed up or slow down.

Also, the magnetic force never does work because it is always perpendicular to velocity:

$$
\vec F_B=q(\vec v\times \vec B)
$$

The magnetic force changes direction only, not speed.

In the velocity selector case, the electric force and magnetic force cancel each other:

$$
\vec F_E+\vec F_B=0
$$

So the net work is zero:

$$
W_{\text{net}}=0
$$

Therefore:

$$
\Delta K=0
$$

So:

$$
\boxed{\text{The kinetic energy does not change in steady motion.}}
$$

---

# 4. Operating principle of the velocity selector

A velocity selector uses crossed electric and magnetic fields to allow only particles with one specific velocity to pass straight through.

The electric force is:

$$
\vec F_E=q\vec E
$$

The magnetic force is:

$$
\vec F_B=q(\vec v\times \vec B)
$$

For straight-line motion:

$$
\vec F_E+\vec F_B=0
$$

So the forces must have equal magnitudes and opposite directions.

The magnitude of the electric force is:

$$
F_E=qE
$$

The magnitude of the magnetic force is:

$$
F_B=qvB
$$

For cancellation:

$$
qE=qvB
$$

Cancel $q$:

$$
E=vB
$$

So:

$$
v=\frac{E}{B}
$$

This means the selected velocity depends only on $E$ and $B$, not on the charge or mass of the particle.

---

## What happens to particles with different velocities?

### If the particle has the correct velocity

If:

$$
v=\frac{E}{B}
$$

then:

$$
F_E=F_B
$$

The forces cancel:

$$
F_{\text{net}}=0
$$

So the particle moves straight.

---

### If the particle is too slow

If:

$$
v<\frac{E}{B}
$$

then:

$$
qvB<qE
$$

So the magnetic force is weaker than the electric force.

The particle is deflected in the direction of the electric force.

---

### If the particle is too fast

If:

$$
v>\frac{E}{B}
$$

then:

$$
qvB>qE
$$

So the magnetic force is stronger than the electric force.

The particle is deflected in the opposite direction.

---

# Final answers for Problem 2

The condition for rectilinear motion is:

$$
\vec E+\vec v\times \vec B=0
$$

For

$$
\vec E=(0,E,0),\quad \vec B=(0,0,B),\quad \vec v=(v,0,0)
$$

we get:

$$
E-vB=0
$$

Therefore:

$$
\boxed{v_d=\frac{E}{B}}
$$

For:

$$
E=400\ \mathrm{V/m}
$$

and

$$
B=0.8\ \mathrm{T}
$$

the selected velocity is:

$$
v_d=\frac{400}{0.8}
$$

$$
\boxed{v_d=500\ \mathrm{m/s}}
$$

The kinetic energy does not change in steady motion:

$$
\boxed{\Delta K=0}
$$

because the net force is zero and the particle moves with constant velocity.

The velocity selector works by balancing the electric and magnetic forces:

$$
qE=qvB
$$

Only particles with velocity

$$
\boxed{v=\frac{E}{B}}
$$

pass straight through.

Particles that are too slow or too fast are deflected away. ✅
