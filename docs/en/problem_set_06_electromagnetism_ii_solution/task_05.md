# Problem 5 – Induction in a moving rod

We have a conducting rod moving in a magnetic field.

We need to calculate:

* the induced EMF,
* the potential difference between the ends of the rod,
* what happens if the motion is not perpendicular to the magnetic field,
* how EMF depends on the rod length,
* and where the energy of the electric field comes from.

---

## Given data

The length of the rod is

$$
L=0.25\ \mathrm{m}
$$

The velocity of the rod is

$$
v=4\ \mathrm{m/s}
$$

The magnetic field is

$$
B=0.6\ \mathrm{T}
$$

The rod moves perpendicular to the magnetic field.

That means the angle between velocity and magnetic field is

$$
\theta=90^\circ
$$

So,

$$
\sin 90^\circ=1
$$

---

# 1. Determine the induced EMF (\mathcal{E})

When a conducting rod moves in a magnetic field, free charges inside the rod experience magnetic force.

The magnetic force on a charge is

$$
\vec F=q(\vec v\times \vec B)
$$

This force pushes positive and negative charges toward opposite ends of the rod.

Because of this separation of charges, an electric field appears inside the rod.

The induced EMF in a moving rod is

$$
\mathcal{E}=BLv\sin\theta
$$

Since the motion is perpendicular to the magnetic field,

$$
\theta=90^\circ
$$

Therefore,

$$
\sin\theta=1
$$

So the formula becomes

$$
\mathcal{E}=BLv
$$

Now substitute the values:

$$
\mathcal{E}=(0.6)(0.25)(4)
$$

First multiply:

$$
0.25\cdot4=1
$$

So,

$$
\mathcal{E}=0.6\cdot1
$$

Therefore,

$$
\mathcal{E}=0.6\ \mathrm{V}
$$

So,

$$
\boxed{\mathcal{E}=0.6\ \mathrm{V}}
$$

---

# 2. Determine the potential difference between the ends

The induced EMF is the work done per unit charge.

For a rod moving in a magnetic field, the EMF is also equal to the potential difference between the two ends of the rod.

So,

$$
\Delta V=\mathcal{E}
$$

We already found:

$$
\mathcal{E}=0.6\ \mathrm{V}
$$

Therefore,

$$
\boxed{\Delta V=0.6\ \mathrm{V}}
$$

So the potential difference between the ends of the rod is

$$
\boxed{0.6\ \mathrm{V}}
$$

One end becomes positively charged, and the other end becomes negatively charged.

Which end is positive depends on the direction of

$$
\vec v\times \vec B
$$

---

# 3. What happens if the motion is not perpendicular to (\vec B)?

In the general case, the induced EMF is

$$
\mathcal{E}=BLv\sin\theta
$$

where (\theta) is the angle between the velocity (\vec v) and the magnetic field (\vec B).

---

## Case 1: Motion perpendicular to magnetic field

If

$$
\theta=90^\circ
$$

then

$$
\sin90^\circ=1
$$

So,

$$
\mathcal{E}=BLv
$$

This gives the maximum EMF.

---

## Case 2: Motion at an angle

If the rod moves at some angle (\theta), then only the perpendicular part of velocity produces EMF.

The perpendicular component of velocity is

$$
v_\perp=v\sin\theta
$$

So,

$$
\mathcal{E}=BLv_\perp
$$

or

$$
\mathcal{E}=BLv\sin\theta
$$

---

## Case 3: Motion parallel to magnetic field

If the rod moves parallel to the magnetic field, then

$$
\theta=0^\circ
$$

and

$$
\sin0^\circ=0
$$

So,

$$
\mathcal{E}=BLv\cdot0
$$

Therefore,

$$
\mathcal{E}=0
$$

So if the rod moves parallel to the magnetic field, no EMF is induced.

Thus,

$$
\boxed{\mathcal{E}=BLv\sin\theta}
$$

and the EMF is maximum when the motion is perpendicular to (\vec B).

---

# 4. How does (\mathcal{E}) depend on (L)?

The formula is

$$
\mathcal{E}=BLv
$$

if the motion is perpendicular to the magnetic field.

Here, (B) and (v) are constant.

So,

$$
\mathcal{E}\propto L
$$

This means the induced EMF is directly proportional to the length of the rod.

If the rod is longer, more charge separation happens along the rod.

So the potential difference becomes larger.

---

## Example

If the length is doubled:

$$
L_{\text{new}}=2L
$$

then

$$
\mathcal{E}_{\text{new}}=B(2L)v
$$

So,

$$
\mathcal{E}_{\text{new}}=2BLv
$$

Therefore,

$$
\mathcal{E}_{\text{new}}=2\mathcal{E}
$$

So if the rod length is doubled, the EMF also doubles.

Since our original EMF is

$$
\mathcal{E}=0.6\ \mathrm{V}
$$

then for double length:

$$
\mathcal{E}_{\text{new}}=2(0.6)
$$

$$
\mathcal{E}_{\text{new}}=1.2\ \mathrm{V}
$$

Therefore,

$$
\boxed{\mathcal{E}\text{ increases linearly with }L}
$$

---

# 5. Where does the energy of the electric field in the rod come from?

The energy does not come from the magnetic field.

This is very important.

The magnetic force changes the direction of motion of charges, but the magnetic field itself does no work.

The energy comes from the external mechanical work used to move the rod.

---

## Explanation

When the rod moves through the magnetic field, charges inside the rod feel magnetic force:

$$
\vec F=q(\vec v\times \vec B)
$$

This force separates charges.

Because charges are separated, an electric field appears inside the rod.

This electric field creates a potential difference between the ends of the rod.

But to keep the rod moving, an external force must do work.

So mechanical energy is converted into electrical energy.

Therefore,

$$
\boxed{\text{Mechanical energy is converted into electrical energy.}}
$$

The source of energy is the work done by the external force that moves the rod.

---

# Physical interpretation

The rod contains free electrons.

When the rod moves through the magnetic field, the electrons move together with the rod.

Since the electrons are moving charges, the magnetic field acts on them.

The magnetic force pushes electrons toward one end of the rod.

So one end becomes negative, and the other end becomes positive.

This charge separation produces an electric field inside the rod.

Eventually, the electric force balances the magnetic force.

At equilibrium:

$$
F_E=F_B
$$

The electric force is

$$
F_E=qE
$$

The magnetic force is

$$
F_B=qvB
$$

So,

$$
qE=qvB
$$

Cancel (q):

$$
E=vB
$$

The potential difference across a rod of length (L) is

$$
\Delta V=EL
$$

Substitute (E=vB):

$$
\Delta V=vBL
$$

So,

$$
\Delta V=BLv
$$

This is the same as the induced EMF:

$$
\mathcal{E}=BLv
$$

---

# Final answers for Problem 5

The induced EMF is

$$
\boxed{\mathcal{E}=0.6\ \mathrm{V}}
$$

The potential difference between the ends is

$$
\boxed{\Delta V=0.6\ \mathrm{V}}
$$

If the motion is not perpendicular to (\vec B), then

$$
\boxed{\mathcal{E}=BLv\sin\theta}
$$

Only the perpendicular component of velocity produces EMF:

$$
\boxed{v_\perp=v\sin\theta}
$$

If the rod moves parallel to the magnetic field,

$$
\boxed{\mathcal{E}=0}
$$

The EMF depends directly on the length of the rod:

$$
\boxed{\mathcal{E}\propto L}
$$

So if (L) is doubled, the EMF is also doubled.

The energy of the electric field comes from mechanical work:

$$
\boxed{\text{External mechanical work } \rightarrow \text{ electrical energy}}
$$

So the magnetic field helps separate the charges, but the actual energy comes from the force that keeps the rod moving. ✅
