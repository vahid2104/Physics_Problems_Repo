# Problem 3 – Field at a point from a system of charges

Two point charges are given:

* charge (+q) at point ((-a,0)),
* charge (+2q) at point ((a,0)).

We need to determine:

* the electric field at ((0,y)),
* the electric field at ((x,0)),
* the general electric field at ((x,y)),
* the conditions for (E_x=0), (E_y=0), and (\vec E=0),
* the numerical value of the field for given data,
* the limit (y\gg a),
* whether a zero-field point exists on the (y)-axis.

---

## 1. Basic formula for electric field

The electric field created by a point charge is given by Coulomb’s law:

genui{"math_block_widget_always_prefetch_v2":{"content":"\vec E = k\frac{Q}{r^2}\hat r"}}

where

[
k=\frac{1}{4\pi\varepsilon_0}
]

and approximately

[
k=8.99\times 10^9\ \mathrm{N,m^2/C^2}
]

A more useful vector form is

[
\vec E=kQ\frac{\vec r-\vec r_Q}{|\vec r-\vec r_Q|^3}
]

Here:

* (\vec r) is the point where we calculate the field,
* (\vec r_Q) is the position of the charge,
* (\vec r-\vec r_Q) is the vector from the charge to the field point.

Because electric fields add as vectors, the total field is

[
\vec E=\vec E_1+\vec E_2
]

---

# 2. General field (\vec E(x,y))

Let the field point be

[
P=(x,y)
]

The first charge is

[
+q \quad \text{at} \quad (-a,0)
]

The vector from (+q) to (P) is

[
\vec r_1=(x,y)-(-a,0)
]

[
\vec r_1=(x+a,y)
]

Its length is

[
r_1=\sqrt{(x+a)^2+y^2}
]

So the field from the first charge is

[
\vec E_1=kq\frac{(x+a,y)}{\left[(x+a)^2+y^2\right]^{3/2}}
]

The second charge is

[
+2q \quad \text{at} \quad (a,0)
]

The vector from (+2q) to (P) is

[
\vec r_2=(x,y)-(a,0)
]

[
\vec r_2=(x-a,y)
]

Its length is

[
r_2=\sqrt{(x-a)^2+y^2}
]

So the field from the second charge is

[
\vec E_2=k(2q)\frac{(x-a,y)}{\left[(x-a)^2+y^2\right]^{3/2}}
]

Therefore, the total electric field is

[
\vec E(x,y)=
kq\frac{(x+a,y)}{\left[(x+a)^2+y^2\right]^{3/2}}
+
2kq\frac{(x-a,y)}{\left[(x-a)^2+y^2\right]^{3/2}}
]

So

[
\boxed{
\vec E(x,y)=
kq
\left[
\frac{(x+a,y)}{\left[(x+a)^2+y^2\right]^{3/2}}
+
2\frac{(x-a,y)}{\left[(x-a)^2+y^2\right]^{3/2}}
\right]
}
]

Now write it using components.

The (x)-component is

[
\boxed{
E_x=
kq
\left[
\frac{x+a}{\left[(x+a)^2+y^2\right]^{3/2}}
+
2\frac{x-a}{\left[(x-a)^2+y^2\right]^{3/2}}
\right]
}
]

The (y)-component is

[
\boxed{
E_y=
kq
\left[
\frac{y}{\left[(x+a)^2+y^2\right]^{3/2}}
+
2\frac{y}{\left[(x-a)^2+y^2\right]^{3/2}}
\right]
}
]

or

[
\boxed{
E_y=
kq,y
\left[
\frac{1}{\left[(x+a)^2+y^2\right]^{3/2}}
+
\frac{2}{\left[(x-a)^2+y^2\right]^{3/2}}
\right]
}
]

---

# 3. Field on the (y)-axis: (\vec E(0,y))

Now take

[
x=0
]

Substitute into the general expression.

For the first charge,

[
x+a=a
]

For the second charge,

[
x-a=-a
]

Also,

[
(a)^2+y^2=(-a)^2+y^2=a^2+y^2
]

So both charges are the same distance from the point ((0,y)).

The field becomes

[
\vec E(0,y)=
kq\frac{(a,y)}{(a^2+y^2)^{3/2}}
+
2kq\frac{(-a,y)}{(a^2+y^2)^{3/2}}
]

Factor out the common part:

[
\vec E(0,y)=
\frac{kq}{(a^2+y^2)^{3/2}}
\left[(a,y)+2(-a,y)\right]
]

Now simplify the vector inside the brackets:

[
(a,y)+2(-a,y)=(a,y)+(-2a,2y)
]

[
(a,y)+2(-a,y)=(-a,3y)
]

Therefore,

[
\boxed{
\vec E(0,y)=
\frac{kq}{(a^2+y^2)^{3/2}}(-a,3y)
}
]

So the components are

[
\boxed{
E_x(0,y)=
-\frac{kqa}{(a^2+y^2)^{3/2}}
}
]

and

[
\boxed{
E_y(0,y)=
\frac{3kqy}{(a^2+y^2)^{3/2}}
}
]

### Meaning

On the (y)-axis:

* the (x)-component is negative,
* the field points partly to the left,
* the (y)-component points upward if (y>0),
* the (y)-component points downward if (y<0).

The field is not purely vertical because the charges are unequal.

---

# 4. Field on the (x)-axis: (\vec E(x,0))

Now take

[
y=0
]

The general field becomes

[
\vec E(x,0)=
kq\frac{(x+a,0)}{|x+a|^3}
+
2kq\frac{(x-a,0)}{|x-a|^3}
]

Therefore,

[
\boxed{
\vec E(x,0)=
kq
\left[
\frac{x+a}{|x+a|^3}
+
2\frac{x-a}{|x-a|^3}
\right]\hat i
}
]

The (y)-component is zero:

[
\boxed{
E_y(x,0)=0
}
]

The (x)-component is

[
\boxed{
E_x(x,0)=
kq
\left[
\frac{x+a}{|x+a|^3}
+
2\frac{x-a}{|x-a|^3}
\right]
}
]

This formula is valid everywhere on the (x)-axis except at the charge positions:

[
x=-a
]

and

[
x=a
]

because the electric field is infinite at the position of a point charge.

---

# 5. Condition for (E_x=0)

From the general formula,

[
E_x=
kq
\left[
\frac{x+a}{\left[(x+a)^2+y^2\right]^{3/2}}
+
2\frac{x-a}{\left[(x-a)^2+y^2\right]^{3/2}}
\right]
]

To have

[
E_x=0
]

we need

[
\frac{x+a}{\left[(x+a)^2+y^2\right]^{3/2}}
+
2\frac{x-a}{\left[(x-a)^2+y^2\right]^{3/2}}
=0
]

Therefore, the condition is

[
\boxed{
\frac{x+a}{\left[(x+a)^2+y^2\right]^{3/2}}
+
2\frac{x-a}{\left[(x-a)^2+y^2\right]^{3/2}}
=0
}
]

This gives all points where the horizontal component of the electric field is zero.

---

# 6. Condition for (E_y=0)

From the general formula,

[
E_y=
kq,y
\left[
\frac{1}{\left[(x+a)^2+y^2\right]^{3/2}}
+
\frac{2}{\left[(x-a)^2+y^2\right]^{3/2}}
\right]
]

For (E_y=0), we need

[
kq,y
\left[
\frac{1}{\left[(x+a)^2+y^2\right]^{3/2}}
+
\frac{2}{\left[(x-a)^2+y^2\right]^{3/2}}
\right]=0
]

Now notice something important.

The bracket is always positive because all distances are positive and both charges are positive.

So the only way to make (E_y=0) is

[
y=0
]

Therefore,

[
\boxed{
E_y=0 \quad \Longleftrightarrow \quad y=0
}
]

except at the charge positions themselves, where the field is not defined.

So the vertical component is zero only on the (x)-axis.

---

# 7. Condition for zero field (\vec E=0)

For the full electric field to be zero, both components must be zero:

[
E_x=0
]

and

[
E_y=0
]

From the previous part, (E_y=0) requires

[
y=0
]

So any zero-field point must lie on the (x)-axis.

Now we study the field on the (x)-axis.

On the (x)-axis,

[
E_x(x,0)=
kq
\left[
\frac{x+a}{|x+a|^3}
+
2\frac{x-a}{|x-a|^3}
\right]
]

We check three regions.

---

## Region 1: (x<-a)

This is to the left of both charges.

Both positive charges push a positive test charge to the left.

So both fields point in the negative (x)-direction.

Therefore, they cannot cancel.

So there is no zero field for

[
x<-a
]

---

## Region 2: (x>a)

This is to the right of both charges.

Both positive charges push a positive test charge to the right.

So both fields point in the positive (x)-direction.

Therefore, they cannot cancel.

So there is no zero field for

[
x>a
]

---

## Region 3: (-a<x<a)

This is between the two charges.

Here:

* the field from (+q) points to the right,
* the field from (+2q) points to the left.

So cancellation is possible.

Between the charges,

[
x+a>0
]

and

[
x-a<0
]

So

[
E_x=
kq
\left[
\frac{1}{(x+a)^2}
-----------------

\frac{2}{(a-x)^2}
\right]
]

Set this equal to zero:

[
\frac{1}{(x+a)^2}
-----------------

\frac{2}{(a-x)^2}=0
]

So

[
\frac{1}{(x+a)^2}
=================

\frac{2}{(a-x)^2}
]

Cross multiply:

[
(a-x)^2=2(x+a)^2
]

Take the positive square root, because distances are positive:

[
a-x=\sqrt{2}(x+a)
]

Now solve for (x):

[
a-x=\sqrt{2}x+\sqrt{2}a
]

Move the (x)-terms to one side:

[
-x-\sqrt{2}x=\sqrt{2}a-a
]

[
-(1+\sqrt{2})x=(\sqrt{2}-1)a
]

So

[
x=
-\frac{\sqrt{2}-1}{1+\sqrt{2}}a
]

This can also be written as

[
x=a\frac{1-\sqrt{2}}{1+\sqrt{2}}
]

Therefore,

[
\boxed{
x_0=a\frac{1-\sqrt{2}}{1+\sqrt{2}}
}
]

Numerically,

[
\frac{1-\sqrt{2}}{1+\sqrt{2}}\approx -0.1716
]

So

[
\boxed{
x_0\approx -0.1716a
}
]

The zero-field point is

[
\boxed{
(x,y)=\left(a\frac{1-\sqrt{2}}{1+\sqrt{2}},0\right)
}
]

This point is between the two charges, but closer to the smaller charge (+q). That makes sense because the charge (+2q) is stronger, so the cancellation point must be farther from (+2q) and closer to (+q).

---

# 8. Numerical calculation for (a=0.2,\mathrm{m}), (y=0.3,\mathrm{m}), (q=2,\mu\mathrm{C})

Because the problem gives (y), we calculate the field on the (y)-axis:

[
\vec E(0,y)=
\frac{kq}{(a^2+y^2)^{3/2}}(-a,3y)
]

Given:

[
a=0.2\ \mathrm{m}
]

[
y=0.3\ \mathrm{m}
]

[
q=2,\mu\mathrm{C}=2\times 10^{-6}\ \mathrm{C}
]

[
k=8.99\times 10^9\ \mathrm{N,m^2/C^2}
]

First calculate the denominator:

[
(a^2+y^2)^{3/2}
===============

(0.2^2+0.3^2)^{3/2}
]

[
(0.2^2+0.3^2)^{3/2}
===================

(0.04+0.09)^{3/2}
]

[
(0.13)^{3/2}
]

[
(0.13)^{3/2}\approx 0.04687
]

Now calculate the factor:

[
\frac{kq}{(a^2+y^2)^{3/2}}
==========================

\frac{(8.99\times 10^9)(2\times 10^{-6})}{0.04687}
]

[
\frac{kq}{(a^2+y^2)^{3/2}}
\approx 3.835\times 10^5
]

Now the vector part is

[
(-a,3y)=(-0.2,0.9)
]

Therefore,

[
\vec E(0,0.3)
\approx
(3.835\times 10^5)(-0.2,0.9)
]

So

[
E_x\approx -7.67\times 10^4\ \mathrm{N/C}
]

and

[
E_y\approx 3.45\times 10^5\ \mathrm{N/C}
]

Therefore,

[
\boxed{
\vec E(0,0.3)
\approx
(-7.67\times 10^4,\ 3.45\times 10^5)\ \mathrm{N/C}
}
]

The magnitude is

[
|\vec E|=
\sqrt{E_x^2+E_y^2}
]

[
|\vec E|
\approx
3.54\times 10^5\ \mathrm{N/C}
]

So

[
\boxed{
|\vec E|\approx 3.54\times 10^5\ \mathrm{N/C}
}
]

---

# 9. Limit (y\gg a)

Now investigate the field on the (y)-axis when (y) is much larger than (a).

We use

[
\vec E(0,y)=
\frac{kq}{(a^2+y^2)^{3/2}}(-a,3y)
]

If

[
y\gg a
]

then

[
a^2+y^2\approx y^2
]

Therefore,

[
(a^2+y^2)^{3/2}\approx (y^2)^{3/2}
]

[
(a^2+y^2)^{3/2}\approx y^3
]

So

[
\vec E(0,y)\approx
\frac{kq}{y^3}(-a,3y)
]

Separate the components:

[
E_x\approx -\frac{kqa}{y^3}
]

and

[
E_y\approx \frac{3kq}{y^2}
]

Therefore,

[
\boxed{
\vec E(0,y)\approx
\left(
-\frac{kqa}{y^3},
\frac{3kq}{y^2}
\right)
}
]

The main term is the vertical term:

[
\boxed{
E_y\approx \frac{3kq}{y^2}
}
]

The horizontal term is smaller:

[
\boxed{
E_x\approx -\frac{kqa}{y^3}
}
]

### Physical meaning

Far away on the (y)-axis, the two charges look almost like one combined charge.

The total charge is

[
q+2q=3q
]

So far away, the field looks approximately like the field of a single charge (3q) located near the origin:

[
\boxed{
\vec E(0,y)\approx \frac{3kq}{y^2}\hat j
}
]

There is still a small negative (x)-component because the bigger charge (+2q) is on the right side, so the field leans slightly to the left.

---

# 10. Does a point of zero field exist on the (y)-axis?

On the (y)-axis,

[
\vec E(0,y)=
\frac{kq}{(a^2+y^2)^{3/2}}(-a,3y)
]

For the field to be zero, both components must be zero.

The (x)-component is

[
E_x(0,y)=
-\frac{kqa}{(a^2+y^2)^{3/2}}
]

This is never zero if

[
q\neq 0
]

and

[
a\neq 0
]

Therefore, the field on the (y)-axis can never be zero.

So the answer is

[
\boxed{
\text{No, there is no zero-field point on the } y\text{-axis.}
}
]

The reason is simple: the two charges are unequal. Their horizontal components do not cancel on the (y)-axis. The stronger charge (+2q) creates a larger horizontal component than the smaller charge (+q), so the total field always has a leftward component.

---

# Final answers for Problem 3

The general field is

[
\boxed{
\vec E(x,y)=
kq
\left[
\frac{(x+a,y)}{\left[(x+a)^2+y^2\right]^{3/2}}
+
2\frac{(x-a,y)}{\left[(x-a)^2+y^2\right]^{3/2}}
\right]
}
]

On the (y)-axis,

[
\boxed{
\vec E(0,y)=
\frac{kq}{(a^2+y^2)^{3/2}}(-a,3y)
}
]

On the (x)-axis,

[
\boxed{
\vec E(x,0)=
kq
\left[
\frac{x+a}{|x+a|^3}
+
2\frac{x-a}{|x-a|^3}
\right]\hat i
}
]

The condition for (E_x=0) is

[
\boxed{
\frac{x+a}{\left[(x+a)^2+y^2\right]^{3/2}}
+
2\frac{x-a}{\left[(x-a)^2+y^2\right]^{3/2}}
=0
}
]

The condition for (E_y=0) is

[
\boxed{
y=0
}
]

The zero-field point is

[
\boxed{
(x,y)=\left(a\frac{1-\sqrt{2}}{1+\sqrt{2}},0\right)
}
]

or approximately

[
\boxed{
(x,y)\approx (-0.1716a,0)
}
]

For

[
a=0.2\ \mathrm{m},\qquad y=0.3\ \mathrm{m},\qquad q=2,\mu\mathrm{C}
]

the field at ((0,0.3)) is

[
\boxed{
\vec E(0,0.3)
\approx
(-7.67\times 10^4,\ 3.45\times 10^5)\ \mathrm{N/C}
}
]

and its magnitude is

[
\boxed{
|\vec E|\approx 3.54\times 10^5\ \mathrm{N/C}
}
]

For

[
y\gg a
]

the field on the (y)-axis becomes approximately

[
\boxed{
\vec E(0,y)\approx
\left(
-\frac{kqa}{y^3},
\frac{3kq}{y^2}
\right)
}
]

The dominant far-away behavior is

[
\boxed{
\vec E(0,y)\approx \frac{3kq}{y^2}\hat j
}
]

Finally,

[
\boxed{
\text{No zero-field point exists on the } y\text{-axis.}
}
]
