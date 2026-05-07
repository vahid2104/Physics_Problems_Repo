# Problem 9 – Dipole in an external field

A dipole is placed in a uniform electric field

$$
E_0
$$

We need to:

* derive the torque acting on the dipole,
* calculate the potential energy,
* determine the equation of angular motion,
* linearize the equation for small displacements,
* and interpret the system as a harmonic oscillator.

---

## Given idea

An electric dipole consists of two equal and opposite charges:

$$
+q
$$

and

$$
-q
$$

separated by a distance

$$
d
$$

The electric dipole moment is defined as

$$
\vec p=q\vec d
$$

The direction of

$$
\vec p
$$

is from the negative charge to the positive charge.

The magnitude of the dipole moment is

$$
p=qd
$$

The dipole is placed in a uniform electric field

$$
\vec E_0
$$

Let the angle between the dipole moment and the electric field be

$$
\theta
$$

---

# 1. Torque acting on the dipole

The electric field exerts a force on each charge.

On the positive charge:

$$
F_+=qE_0
$$

The force is in the direction of the electric field.

On the negative charge:

$$
F_-=qE_0
$$

The magnitude is the same, but the force is opposite to the electric field.

So the two forces are equal in magnitude and opposite in direction.

Because the forces act at different points, they form a couple.

A couple produces torque.

---

## Torque from the two forces

The torque tends to rotate the dipole so that the dipole moment aligns with the electric field.

The magnitude of the torque is

$$
\tau=pE_0\sin\theta
$$

In vector form,

$$
\vec \tau=\vec p\times \vec E_0
$$

Therefore,

$$
|\vec\tau|=pE_0\sin\theta
$$

---

## Direction of the torque

The torque acts to reduce the angle

$$
\theta
$$

between

$$
\vec p
$$

and

$$
\vec E_0
$$

So if we take positive

$$
\theta
$$

as the displacement away from equilibrium, then the torque is a restoring torque.

Therefore,

$$
\tau=-pE_0\sin\theta
$$

The negative sign means the torque acts opposite to the angular displacement.

So the torque on the dipole is

$$
\boxed{\tau=-pE_0\sin\theta}
$$

---

# 2. Potential energy of the dipole

The potential energy of a dipole in a uniform electric field is

$$
U=-\vec p\cdot \vec E_0
$$

Using the dot product,

$$
\vec p\cdot \vec E_0=pE_0\cos\theta
$$

Therefore,

$$
U=-pE_0\cos\theta
$$

So the potential energy is

$$
\boxed{U=-pE_0\cos\theta}
$$

---

## Meaning of the potential energy

When the dipole is aligned with the field,

$$
\theta=0
$$

Then

$$
U=-pE_0\cos 0
$$

Since

$$
\cos 0=1
$$

we get

$$
U=-pE_0
$$

This is the minimum potential energy.

So the dipole is stable when it points in the same direction as the electric field.

---

When the dipole is opposite to the field,

$$
\theta=\pi
$$

Then

$$
U=-pE_0\cos\pi
$$

Since

$$
\cos\pi=-1
$$

we get

$$
U=+pE_0
$$

This is the maximum potential energy.

So the dipole is unstable when it points opposite to the electric field.

---

# 3. Equation of angular motion

For rotational motion, Newton’s second law is

$$
\tau=I\alpha
$$

where

$$
I
$$

is the moment of inertia of the dipole, and

$$
\alpha
$$

is the angular acceleration.

Angular acceleration is

$$
\alpha=\frac{d^2\theta}{dt^2}
$$

So

$$
\tau=I\frac{d^2\theta}{dt^2}
$$

But from the torque formula,

$$
\tau=-pE_0\sin\theta
$$

Therefore,

$$
I\frac{d^2\theta}{dt^2}=-pE_0\sin\theta
$$

Bring everything to one side:

$$
I\frac{d^2\theta}{dt^2}+pE_0\sin\theta=0
$$

Now divide by

$$
I
$$

We get

$$
\frac{d^2\theta}{dt^2}+\frac{pE_0}{I}\sin\theta=0
$$

So the equation of angular motion is

$$
\boxed{\frac{d^2\theta}{dt^2}+\frac{pE_0}{I}\sin\theta=0}
$$

This is the exact equation of motion.

It is nonlinear because it contains

$$
\sin\theta
$$

instead of just

$$
\theta
$$

---

# 4. Linearization for small displacements

For small angular displacements,

$$
\theta\ll 1
$$

in radians.

For small angles, we use the approximation

$$
\sin\theta\approx \theta
$$

So the exact equation

$$
\frac{d^2\theta}{dt^2}+\frac{pE_0}{I}\sin\theta=0
$$

becomes

$$
\frac{d^2\theta}{dt^2}+\frac{pE_0}{I}\theta=0
$$

Therefore, the linearized equation is

$$
\boxed{\frac{d^2\theta}{dt^2}+\frac{pE_0}{I}\theta=0}
$$

This equation is now linear because it contains

$$
\theta
$$

not

$$
\sin\theta
$$

---

# 5. Interpretation as a harmonic oscillator

The standard equation for simple harmonic motion is

$$
\frac{d^2x}{dt^2}+\omega^2 x=0
$$

For angular motion, the similar form is

$$
\frac{d^2\theta}{dt^2}+\omega^2\theta=0
$$

Our linearized equation is

$$
\frac{d^2\theta}{dt^2}+\frac{pE_0}{I}\theta=0
$$

Compare this with

$$
\frac{d^2\theta}{dt^2}+\omega^2\theta=0
$$

So,

$$
\omega^2=\frac{pE_0}{I}
$$

Therefore,

$$
\omega=\sqrt{\frac{pE_0}{I}}
$$

So the angular frequency of small oscillations is

$$
\boxed{\omega=\sqrt{\frac{pE_0}{I}}}
$$

---

## Period of oscillation

The period of a harmonic oscillator is

$$
T=\frac{2\pi}{\omega}
$$

Substitute

$$
\omega=\sqrt{\frac{pE_0}{I}}
$$

Then

$$
T=\frac{2\pi}{\sqrt{\frac{pE_0}{I}}}
$$

This can be written as

$$
T=2\pi\sqrt{\frac{I}{pE_0}}
$$

Therefore,

$$
\boxed{T=2\pi\sqrt{\frac{I}{pE_0}}}
$$

---

# Physical interpretation

The dipole behaves like a rotational harmonic oscillator for small angles.

That means if the dipole is slightly displaced from its stable equilibrium position, it oscillates back and forth around

$$
\theta=0
$$

The restoring torque is approximately proportional to the angular displacement:

$$
\tau\approx -pE_0\theta
$$

This is similar to the restoring force of a spring:

$$
F=-kx
$$

So we can compare:

$$
\tau=-pE_0\theta
$$

with

$$
F=-kx
$$

The quantity

$$
pE_0
$$

acts like an angular spring constant.

So we can write

$$
\kappa=pE_0
$$

where

$$
\kappa
$$

is the rotational spring constant.

Then the equation becomes

$$
I\frac{d^2\theta}{dt^2}+\kappa\theta=0
$$

This is the equation of a torsional harmonic oscillator.

---

# Final answers for Problem 9

The torque acting on the dipole is

$$
\boxed{\vec\tau=\vec p\times \vec E_0}
$$

and its magnitude is

$$
\boxed{\tau=pE_0\sin\theta}
$$

As a restoring torque,

$$
\boxed{\tau=-pE_0\sin\theta}
$$

The potential energy of the dipole is

$$
\boxed{U=-\vec p\cdot \vec E_0}
$$

or

$$
\boxed{U=-pE_0\cos\theta}
$$

The equation of angular motion is

$$
\boxed{\frac{d^2\theta}{dt^2}+\frac{pE_0}{I}\sin\theta=0}
$$

For small angular displacements,

$$
\sin\theta\approx\theta
$$

so the equation becomes

$$
\boxed{\frac{d^2\theta}{dt^2}+\frac{pE_0}{I}\theta=0}
$$

This is the equation of a harmonic oscillator with angular frequency

$$
\boxed{\omega=\sqrt{\frac{pE_0}{I}}}
$$

and period

$$
\boxed{T=2\pi\sqrt{\frac{I}{pE_0}}}
$$

Therefore, for small oscillations, the dipole behaves like a rotational harmonic oscillator. ✅
