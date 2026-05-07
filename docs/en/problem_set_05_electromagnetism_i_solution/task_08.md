# Problem 8 – Energy of a three-charge system

We have a system of three point charges.

To make the numerical calculations clear, we will use the example

$$
q_1=q_2=q_3=4\ \mu\mathrm{C}
$$

so

$$
q_1=q_2=q_3=4\times 10^{-6}\ \mathrm{C}
$$

The Coulomb constant is

$$
k=8.99\times 10^9\ \mathrm{N,m^2/C^2}
$$

For the equilateral triangle part, we will use side length

$$
a=0.3\ \mathrm{m}
$$

---

## 1. Total energy of the system

For two charges, the electric potential energy is

$$
U=\frac{kq_1q_2}{r}
$$

where

* (q_1) and (q_2) are the charges,
* (r) is the distance between them,
* (k) is Coulomb’s constant.

For three charges, there are three pairs:

$$
(q_1,q_2)
$$

$$
(q_1,q_3)
$$

$$
(q_2,q_3)
$$

So the total electric potential energy is the sum of the energies of all pairs:

$$
U_{\text{total}}
================

\frac{kq_1q_2}{r_{12}}
+
\frac{kq_1q_3}{r_{13}}
+
\frac{kq_2q_3}{r_{23}}
$$

Therefore,

$$
\boxed{
U_{\text{total}}
================

k\left(
\frac{q_1q_2}{r_{12}}
+
\frac{q_1q_3}{r_{13}}
+
\frac{q_2q_3}{r_{23}}
\right)
}
$$

This is the general formula for the energy of a three-charge system.

---

## 2. Energy for an equilateral triangle configuration

In an equilateral triangle, all sides are equal.

So

$$
r_{12}=r_{13}=r_{23}=a
$$

We use

$$
a=0.3\ \mathrm{m}
$$

Also, for this first case,

$$
q_1=q_2=q_3=q
$$

where

$$
q=4\times 10^{-6}\ \mathrm{C}
$$

The total energy is

$$
U_{\text{total}}
================

\frac{kq^2}{a}
+
\frac{kq^2}{a}
+
\frac{kq^2}{a}
$$

Since all three terms are the same:

$$
U_{\text{total}}=3\frac{kq^2}{a}
$$

Now substitute the values:

$$
U_{\text{total}}
================

3\frac{(8.99\times 10^9)(4\times 10^{-6})^2}{0.3}
$$

First square the charge:

$$
(4\times 10^{-6})^2
===================

16\times 10^{-12}
$$

So

$$
U_{\text{total}}
================

3\frac{(8.99\times 10^9)(16\times 10^{-12})}{0.3}
$$

Multiply:

$$
(8.99\times 10^9)(16\times 10^{-12})
====================================

143.84\times 10^{-3}
$$

$$
=0.14384
$$

So

$$
U_{\text{total}}
================

3\frac{0.14384}{0.3}
$$

First divide:

$$
\frac{0.14384}{0.3}=0.47947
$$

Then multiply by 3:

$$
U_{\text{total}}=3(0.47947)
$$

$$
U_{\text{total}}=1.4384\ \mathrm{J}
$$

Therefore,

$$
\boxed{
U_{\text{total}}\approx 1.44\ \mathrm{J}
}
$$

Because all three charges are positive, all three interactions are repulsive, so the energy is positive.

---

## 3. Change in energy when changing the sign of one charge

Now we change the sign of one charge.

Let

$$
q_1=+q
$$

$$
q_2=+q
$$

$$
q_3=-q
$$

The charges are still placed at the corners of an equilateral triangle, so

$$
r_{12}=r_{13}=r_{23}=a
$$

The total energy is

$$
U_{\text{total}}
================

\frac{kq_1q_2}{a}
+
\frac{kq_1q_3}{a}
+
\frac{kq_2q_3}{a}
$$

Substitute the signs:

$$
U_{\text{total}}
================

\frac{k(+q)(+q)}{a}
+
\frac{k(+q)(-q)}{a}
+
\frac{k(+q)(-q)}{a}
$$

So

$$
U_{\text{total}}
================

## \frac{kq^2}{a}

## \frac{kq^2}{a}

\frac{kq^2}{a}
$$

Combine the terms:

$$
U_{\text{total}}
================

-\frac{kq^2}{a}
$$

Now substitute the values:

$$
U_{\text{total}}
================

-\frac{(8.99\times 10^9)(4\times 10^{-6})^2}{0.3}
$$

We already calculated:

$$
(8.99\times 10^9)(4\times 10^{-6})^2=0.14384
$$

So

$$
U_{\text{total}}
================

-\frac{0.14384}{0.3}
$$

$$
U_{\text{total}}=-0.47947\ \mathrm{J}
$$

Therefore,

$$
\boxed{
U_{\text{total}}\approx -0.479\ \mathrm{J}
}
$$

---

### Change in energy

The original energy was

$$
U_{\text{positive}}=1.4384\ \mathrm{J}
$$

After changing the sign of one charge, the energy is

$$
U_{\text{mixed}}=-0.47947\ \mathrm{J}
$$

The change in energy is

$$
\Delta U=U_{\text{mixed}}-U_{\text{positive}}
$$

Substitute:

$$
\Delta U=-0.47947-1.4384
$$

$$
\Delta U=-1.91787\ \mathrm{J}
$$

Therefore,

$$
\boxed{
\Delta U\approx -1.92\ \mathrm{J}
}
$$

The negative sign means the energy decreases when one charge becomes negative.

This happens because opposite charges attract, and attractive interactions have negative potential energy.

---

## 4. Minimum energy configuration numerically

This part needs one important idea.

If the charges are completely free, then there is no simple finite minimum energy.

For example, if opposite charges are allowed to get closer and closer together, then

$$
r\rightarrow 0
$$

For opposite charges,

$$
U=-\frac{kq^2}{r}
$$

As (r) becomes very small,

$$
U\rightarrow -\infty
$$

So without any restrictions, the energy can keep decreasing forever.

Therefore, to find a numerical minimum, we must add a physical restriction.

For example, we can say:

* the charges must stay inside a (1\ \mathrm{m}\times 1\ \mathrm{m}) square,
* the charges cannot be closer than

$$
d_{\min}=0.05\ \mathrm{m}
$$

This avoids the impossible case where two point charges sit exactly on top of each other.

---

### Case A: three positive charges

If

$$
q_1=q_2=q_3=+q
$$

then all interactions are repulsive.

The energy is

$$
U_{\text{total}}
================

kq^2
\left(
\frac{1}{r_{12}}
+
\frac{1}{r_{13}}
+
\frac{1}{r_{23}}
\right)
$$

To make the energy small, the distances should be as large as possible.

Inside a (1\ \mathrm{m}\times 1\ \mathrm{m}) square, a good minimum-energy configuration is to place the charges at three corners of the square:

$$
(0,0),\quad (1,0),\quad (0,1)
$$

Then the distances are

$$
r_{12}=1
$$

$$
r_{13}=1
$$

$$
r_{23}=\sqrt{2}
$$

So

$$
U_{\text{total}}
================

kq^2
\left(
\frac{1}{1}
+
\frac{1}{1}
+
\frac{1}{\sqrt{2}}
\right)
$$

We already know

$$
kq^2=0.14384
$$

So

$$
U_{\text{total}}
================

0.14384
\left(
1+1+\frac{1}{\sqrt{2}}
\right)
$$

Since

$$
\frac{1}{\sqrt{2}}\approx 0.7071
$$

we get

$$
U_{\text{total}}
================

0.14384(2.7071)
$$

$$
U_{\text{total}}\approx 0.389\ \mathrm{J}
$$

Therefore, for three positive charges in this restricted region,

$$
\boxed{
U_{\min}\approx 0.389\ \mathrm{J}
}
$$

A minimum-energy configuration is approximately three charges placed far apart, near three corners of the square.

---

### Case B: two positive charges and one negative charge

Now take

$$
q_1=+q
$$

$$
q_2=+q
$$

$$
q_3=-q
$$

The energy is

$$
U_{\text{total}}
================

## \frac{kq^2}{r_{12}}

## \frac{kq^2}{r_{13}}

\frac{kq^2}{r_{23}}
$$

The positive-positive pair gives positive energy.

The positive-negative pairs give negative energy.

To make the total energy as small as possible, the negative charge should be close to the two positive charges.

But the two positive charges should not be too close to each other, because they repel.

Using the minimum distance

$$
d_{\min}=0.05\ \mathrm{m}
$$

a low-energy configuration is:

$$
q_3=-q \quad \text{at} \quad (0.50,0.50)
$$

$$
q_1=+q \quad \text{at} \quad (0.45,0.50)
$$

$$
q_2=+q \quad \text{at} \quad (0.55,0.50)
$$

Then

$$
r_{13}=0.05\ \mathrm{m}
$$

$$
r_{23}=0.05\ \mathrm{m}
$$

$$
r_{12}=0.10\ \mathrm{m}
$$

The energy becomes

$$
U_{\text{total}}
================

kq^2
\left(
\frac{1}{0.10}
--------------

## \frac{1}{0.05}

\frac{1}{0.05}
\right)
$$

Calculate inside the brackets:

$$
\frac{1}{0.10}=10
$$

$$
\frac{1}{0.05}=20
$$

So

$$
U_{\text{total}}
================

kq^2(10-20-20)
$$

$$
U_{\text{total}}
================

kq^2(-30)
$$

Using

$$
kq^2=0.14384
$$

we get

$$
U_{\text{total}}
================

0.14384(-30)
$$

$$
U_{\text{total}}=-4.3152\ \mathrm{J}
$$

Therefore,

$$
\boxed{
U_{\min}\approx -4.32\ \mathrm{J}
}
$$

for this restricted numerical example.

---

## 5. Interpretation of the stability of the system

The sign of the energy tells us a lot about stability.

---

### If all charges have the same sign

For example,

$$
q_1=q_2=q_3=+q
$$

all interactions are repulsive.

The energy is positive:

$$
U>0
$$

This means the charges do not want to stay close together.

They naturally move apart to reduce the energy.

So a system of three equal positive charges is not stable if the charges are free to move.

The charges will repel each other and spread out.

---

### If one charge has the opposite sign

For example,

$$
q_1=+q
$$

$$
q_2=+q
$$

$$
q_3=-q
$$

then there are attractive interactions.

The positive and negative charges attract each other.

This makes the energy negative:

$$
U<0
$$

A negative energy means the system is more bound than the all-positive case.

However, for ideal point charges, this can also cause a problem.

Opposite charges can get closer and closer, making

$$
U\rightarrow -\infty
$$

So mathematically, the system has no stable finite minimum unless we add extra physical restrictions.

Examples of restrictions could be:

* minimum allowed distance between charges,
* charges placed on fixed supports,
* charges confined to a box,
* quantum mechanical effects at very small distances.

---

## Final answers for Problem 8

The total energy of a three-charge system is

$$
\boxed{
U_{\text{total}}
================

k\left(
\frac{q_1q_2}{r_{12}}
+
\frac{q_1q_3}{r_{13}}
+
\frac{q_2q_3}{r_{23}}
\right)
}
$$

For three equal positive charges in an equilateral triangle of side

$$
a=0.3\ \mathrm{m}
$$

with

$$
q=4\ \mu\mathrm{C}
$$

the energy is

$$
\boxed{
U_{\text{total}}\approx 1.44\ \mathrm{J}
}
$$

If one charge changes sign, the energy becomes

$$
\boxed{
U_{\text{total}}\approx -0.479\ \mathrm{J}
}
$$

The change in energy is

$$
\boxed{
\Delta U\approx -1.92\ \mathrm{J}
}
$$

For a numerical minimum with the restrictions

$$
1\ \mathrm{m}\times 1\ \mathrm{m}\ \text{box}
$$

and

$$
d_{\min}=0.05\ \mathrm{m}
$$

three positive charges have approximately

$$
\boxed{
U_{\min}\approx 0.389\ \mathrm{J}
}
$$

while two positive charges and one negative charge can reach approximately

$$
\boxed{
U_{\min}\approx -4.32\ \mathrm{J}
}
$$

The all-positive system is unstable because the charges repel each other.

The mixed-sign system has lower energy because opposite charges attract, but ideal point charges need extra physical constraints to avoid collapsing together. ✅
