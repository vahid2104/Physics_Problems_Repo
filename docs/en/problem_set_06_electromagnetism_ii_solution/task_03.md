# Problem 3 – Magnetic moment of a loop

We have a conducting loop with:

* number of turns: (N)
* area of one loop: (S)
* current: (I)
* uniform magnetic field: (\vec B)

We need to:

* define the magnetic moment (\vec \mu),
* determine the torque (\vec M),
* find when torque is maximum,
* determine the potential energy (U),
* indicate stable and unstable positions.

---

## Given data

The loop has

$$
N
$$

turns.

The area of the loop is

$$
S
$$

The current through the loop is

$$
I
$$

The magnetic field is

$$
\vec B
$$

We assume the magnetic field is uniform, meaning it has the same value and direction everywhere.

---

# 1. Magnetic moment of the loop

A current-carrying loop behaves like a small magnet.

The magnetic moment of a loop is defined as

$$
\vec \mu = N I \vec S
$$

Here:

* (N) is the number of turns,
* (I) is the current,
* (\vec S) is the area vector of the loop.

The magnitude of the magnetic moment is

$$
\mu = NIS
$$

---

## Direction of (\vec \mu)

The direction of (\vec \mu) is perpendicular to the surface of the loop.

We find its direction using the right-hand rule:

If the fingers of your right hand follow the direction of the current, then your thumb points in the direction of (\vec \mu).

So:

$$
\vec \mu
$$

is normal to the plane of the loop.

---

## Final answer for part 1

$$
\boxed{\vec \mu = N I \vec S}
$$

and its magnitude is

$$
\boxed{\mu = NIS}
$$

---

# 2. Torque acting on the loop

When a magnetic moment is placed in a magnetic field, a torque acts on it.

The torque is given by the vector product:

$$
\vec M = \vec \mu \times \vec B
$$

Sometimes torque is also written as (\vec \tau), but in this problem we use (\vec M).

So:

$$
\vec M = \vec \mu \times \vec B
$$

The magnitude of torque is

$$
M = \mu B \sin \theta
$$

where (\theta) is the angle between (\vec \mu) and (\vec B).

Since

$$
\mu = NIS
$$

we get

$$
M = NISB \sin \theta
$$

---

## Final answer for part 2

The torque vector is

$$
\boxed{\vec M = \vec \mu \times \vec B}
$$

The magnitude of the torque is

$$
\boxed{M = \mu B \sin \theta}
$$

or

$$
\boxed{M = NISB \sin \theta}
$$

---

# 3. Angle for maximum torque

The torque magnitude is

$$
M = NISB \sin \theta
$$

Here (N), (I), (S), and (B) are constant.

So torque depends only on

$$
\sin \theta
$$

The maximum value of (\sin \theta) is

$$
1
$$

This happens when

$$
\theta = 90^\circ
$$

Therefore, torque is maximum when the magnetic moment is perpendicular to the magnetic field.

So:

$$
\vec \mu \perp \vec B
$$

---

## Maximum torque

If

$$
\sin 90^\circ = 1
$$

then

$$
M_{\max} = NISB
$$

---

## Final answer for part 3

The torque is maximum when

$$
\boxed{\theta = 90^\circ}
$$

and the maximum torque is

$$
\boxed{M_{\max}=NISB}
$$

---

# 4. Potential energy of the loop

The potential energy of a magnetic moment in a magnetic field is

$$
U = -\vec \mu \cdot \vec B
$$

The dot product formula is

$$
\vec \mu \cdot \vec B = \mu B \cos \theta
$$

So:

$$
U = -\mu B \cos \theta
$$

Since

$$
\mu = NIS
$$

we get

$$
U = -NISB \cos \theta
$$

---

## Final answer for part 4

The potential energy is

$$
\boxed{U=-\vec \mu \cdot \vec B}
$$

or in scalar form:

$$
\boxed{U=-\mu B \cos \theta}
$$

Since

$$
\mu=NIS
$$

we can also write:

$$
\boxed{U=-NISB\cos\theta}
$$

---

# 5. Stable and unstable positions

To understand stable and unstable positions, we look at the potential energy:

$$
U=-\mu B\cos\theta
$$

The system is stable when potential energy is minimum.

The system is unstable when potential energy is maximum.

---

## Stable position

The minimum potential energy happens when

$$
\cos\theta = 1
$$

This occurs at

$$
\theta = 0^\circ
$$

Then:

$$
U=-\mu B
$$

This is the lowest value of potential energy.

So the stable position is when

$$
\vec \mu
$$

is in the same direction as

$$
\vec B
$$

That means:

$$
\vec \mu \parallel \vec B
$$

---

## Stable position final answer

$$
\boxed{\theta=0^\circ}
$$

The loop is stable when

$$
\boxed{\vec \mu \text{ is parallel to } \vec B}
$$

At this position:

$$
\boxed{U_{\min}=-\mu B}
$$

or

$$
\boxed{U_{\min}=-NISB}
$$

---

## Unstable position

The maximum potential energy happens when

$$
\cos\theta = -1
$$

This occurs at

$$
\theta = 180^\circ
$$

Then:

$$
U=+\mu B
$$

This is the highest value of potential energy.

So the unstable position is when

$$
\vec \mu
$$

is opposite to

$$
\vec B
$$

That means:

$$
\vec \mu \text{ anti-parallel to } \vec B
$$

---

## Unstable position final answer

$$
\boxed{\theta=180^\circ}
$$

The loop is unstable when

$$
\boxed{\vec \mu \text{ is opposite to } \vec B}
$$

At this position:

$$
\boxed{U_{\max}=+\mu B}
$$

or

$$
\boxed{U_{\max}=+NISB}
$$

---

# Simple physical interpretation

A current loop in a magnetic field behaves like a small magnet.

The magnetic field tries to rotate the loop so that its magnetic moment (\vec \mu) becomes aligned with the magnetic field (\vec B).

So the loop wants to rotate toward the stable position:

$$
\vec \mu \parallel \vec B
$$

This is similar to a compass needle rotating until it aligns with Earth’s magnetic field.

---

# Important special cases

## Case 1: (\theta=0^\circ)

The magnetic moment and magnetic field are in the same direction:

$$
\vec \mu \parallel \vec B
$$

Torque:

$$
M=NISB\sin 0^\circ
$$

$$
M=0
$$

Potential energy:

$$
U=-NISB\cos 0^\circ
$$

$$
U=-NISB
$$

This is a stable position.

---

## Case 2: (\theta=90^\circ)

The magnetic moment is perpendicular to the magnetic field:

$$
\vec \mu \perp \vec B
$$

Torque:

$$
M=NISB\sin 90^\circ
$$

$$
M=NISB
$$

Potential energy:

$$
U=-NISB\cos 90^\circ
$$

$$
U=0
$$

This is the position where torque is maximum.

---

## Case 3: (\theta=180^\circ)

The magnetic moment is opposite to the magnetic field:

$$
\vec \mu \text{ anti-parallel to } \vec B
$$

Torque:

$$
M=NISB\sin 180^\circ
$$

$$
M=0
$$

Potential energy:

$$
U=-NISB\cos 180^\circ
$$

Since

$$
\cos 180^\circ=-1
$$

we get

$$
U=+NISB
$$

This is an unstable position.

---

# Final answers for Problem 3

The magnetic moment of the loop is

$$
\boxed{\vec \mu = N I \vec S}
$$

The magnitude of the magnetic moment is

$$
\boxed{\mu=NIS}
$$

The torque acting on the loop is

$$
\boxed{\vec M=\vec \mu \times \vec B}
$$

The magnitude of the torque is

$$
\boxed{M=\mu B\sin\theta}
$$

or

$$
\boxed{M=NISB\sin\theta}
$$

The torque is maximum when

$$
\boxed{\theta=90^\circ}
$$

The maximum torque is

$$
\boxed{M_{\max}=NISB}
$$

The potential energy is

$$
\boxed{U=-\vec \mu \cdot \vec B}
$$

or

$$
\boxed{U=-\mu B\cos\theta}
$$

or

$$
\boxed{U=-NISB\cos\theta}
$$

The stable position is

$$
\boxed{\theta=0^\circ}
$$

where

$$
\boxed{\vec \mu \parallel \vec B}
$$

and

$$
\boxed{U_{\min}=-NISB}
$$

The unstable position is

$$
\boxed{\theta=180^\circ}
$$

where

$$
\boxed{\vec \mu \text{ is opposite to } \vec B}
$$

and

$$
\boxed{U_{\max}=+NISB}
$$

So the loop rotates in the magnetic field until its magnetic moment becomes aligned with the magnetic field. ✅
