# Problem 2 – Coulomb’s force

Two point charges are given:

$$
q_1=3\ \mu\mathrm{C}
$$

$$
q_2=-5\ \mu\mathrm{C}
$$

They are located at:

$$
\vec r_1=(0,0)
$$

$$
\vec r_2=(0.4,0.3)\ \mathrm{m}
$$

We need to determine:

* the force vector acting on $q_2$,
* the magnitude of this force,
* the potential energy of the system,
* the work required to separate the charges to a distance of $2\ \mathrm{m}$.

---

## 1. Convert the charges to SI units

The charges are given in microcoulombs.

We know that

$$
1\ \mu\mathrm{C}=10^{-6}\ \mathrm{C}
$$

So

$$
q_1=3\cdot 10^{-6}\ \mathrm{C}
$$

and

$$
q_2=-5\cdot 10^{-6}\ \mathrm{C}
$$

---

## 2. Find the vector from $q_1$ to $q_2$

The position of $q_1$ is

$$
\vec r_1=(0,0)
$$

The position of $q_2$ is

$$
\vec r_2=(0.4,0.3)
$$

The vector from $q_1$ to $q_2$ is

$$
\vec r_{12}=\vec r_2-\vec r_1
$$

Substitute the values:

$$
\vec r_{12}=(0.4,0.3)-(0,0)
$$

$$
\vec r_{12}=(0.4,0.3)\ \mathrm{m}
$$

---

## 3. Calculate the distance between the charges

The distance is the magnitude of the vector $\vec r_{12}$:

$$
r=|\vec r_{12}|
$$

So

$$
r=\sqrt{0.4^2+0.3^2}
$$

$$
r=\sqrt{0.16+0.09}
$$

$$
r=\sqrt{0.25}
$$

$$
r=0.5\ \mathrm{m}
$$

Therefore, the charges are separated by

$$
r=0.5\ \mathrm{m}
$$

---

## 4. Unit vector from $q_1$ to $q_2$

The unit vector in the direction from $q_1$ to $q_2$ is

$$
\hat r_{12}=\frac{\vec r_{12}}{|\vec r_{12}|}
$$

Substitute the values:

$$
\hat r_{12}=\frac{(0.4,0.3)}{0.5}
$$

$$
\hat r_{12}=(0.8,0.6)
$$

This vector gives only the direction.

---

## 5. Force acting on $q_2$

Coulomb’s law says that the magnitude of the electric force between two point charges is:

genui{"math_block_widget_always_prefetch_v2":{"content":"F=k\frac{|q_1q_2|}{r^2}"}}

where

$$
k=8.99\cdot 10^9\ \mathrm{N,m^2/C^2}
$$

Because $q_1$ is positive and $q_2$ is negative, the charges attract each other.

That means the force on $q_2$ points **toward $q_1$**.

Since $\hat r_{12}$ points from $q_1$ to $q_2$, the force on $q_2$ points in the opposite direction:

$$
\vec F_2=-F\hat r_{12}
$$

Now calculate the magnitude first:

$$
F=k\frac{|q_1q_2|}{r^2}
$$

Substitute the values:

$$
F=8.99\cdot 10^9
\frac{|(3\cdot 10^{-6})(-5\cdot 10^{-6})|}{(0.5)^2}
$$

First multiply the charges:

$$
|(3\cdot 10^{-6})(-5\cdot 10^{-6})|
=15\cdot 10^{-12}
$$

So

$$
F=8.99\cdot 10^9\frac{15\cdot 10^{-12}}{0.25}
$$

Calculate the numerator:

$$
8.99\cdot 10^9\cdot 15\cdot 10^{-12}
=0.13485
$$

Now divide by $0.25$:

$$
F=\frac{0.13485}{0.25}
$$

$$
F=0.5394\ \mathrm{N}
$$

So the magnitude of the force is

$$
F\approx 0.539\ \mathrm{N}
$$

Now use the direction:

$$
\vec F_2=-F(0.8,0.6)
$$

$$
\vec F_2=-0.5394(0.8,0.6)
$$

Therefore,

$$
\vec F_2=(-0.43152,-0.32364)\ \mathrm{N}
$$

So approximately,

$$
\boxed{\vec F_2=(-0.432,-0.324)\ \mathrm{N}}
$$

This makes sense because $q_2$ is located in the first quadrant, and the force pulls it back toward the origin.

---

## 6. Magnitude of the force

We already calculated the magnitude:

$$
|\vec F_2|=0.5394\ \mathrm{N}
$$

Therefore,

$$
\boxed{|\vec F_2|\approx 0.539\ \mathrm{N}}
$$

We can also check it from the vector components:

$$
|\vec F_2|=\sqrt{(-0.43152)^2+(-0.32364)^2}
$$

$$
|\vec F_2|\approx 0.539\ \mathrm{N}
$$

---

## 7. Potential energy of the system

The electric potential energy of two point charges is:

U=k\frac{q_1q_2}{r}

Substitute the values:

$$
U=8.99\cdot 10^9
\frac{(3\cdot 10^{-6})(-5\cdot 10^{-6})}{0.5}
$$

Multiply the charges:

$$
(3\cdot 10^{-6})(-5\cdot 10^{-6})
=-15\cdot 10^{-12}
$$

So

$$
U=8.99\cdot 10^9
\frac{-15\cdot 10^{-12}}{0.5}
$$

Calculate the numerator:

$$
8.99\cdot 10^9\cdot (-15\cdot 10^{-12})
=-0.13485
$$

Now divide by $0.5$:

$$
U=\frac{-0.13485}{0.5}
$$

$$
U=-0.2697\ \mathrm{J}
$$

Therefore,

$$
\boxed{U=-0.270\ \mathrm{J}}
$$

The potential energy is negative because the charges have opposite signs, so they attract each other.

---

## 8. Work required to separate the charges to $2\ \mathrm{m}$

We want to move the charges from the initial distance

$$
r_i=0.5\ \mathrm{m}
$$

to the final distance

$$
r_f=2\ \mathrm{m}
$$

The work required by an external force is equal to the change in potential energy:

$$
W_{\text{ext}}=\Delta U
$$

So

$$
W_{\text{ext}}=U_f-U_i
$$

We already know:

$$
U_i=-0.2697\ \mathrm{J}
$$

Now calculate the final potential energy:

$$
U_f=k\frac{q_1q_2}{r_f}
$$

Substitute the values:

$$
U_f=8.99\cdot 10^9
\frac{(3\cdot 10^{-6})(-5\cdot 10^{-6})}{2}
$$

We already calculated:

$$
8.99\cdot 10^9(3\cdot 10^{-6})(-5\cdot 10^{-6})
=-0.13485
$$

So

$$
U_f=\frac{-0.13485}{2}
$$

$$
U_f=-0.067425\ \mathrm{J}
$$

Now calculate the change in potential energy:

$$
W_{\text{ext}}=U_f-U_i
$$

$$
W_{\text{ext}}=-0.067425-(-0.2697)
$$

$$
W_{\text{ext}}=-0.067425+0.2697
$$

$$
W_{\text{ext}}=0.202275\ \mathrm{J}
$$

Therefore,

$$
\boxed{W_{\text{ext}}\approx 0.202\ \mathrm{J}}
$$

This work is positive because we must pull the opposite charges apart against their attractive force.

---

# Final answers for Problem 2

The distance between the charges is

$$
r=0.5\ \mathrm{m}
$$

The force vector acting on $q_2$ is

$$
\boxed{\vec F_2=(-0.432,-0.324)\ \mathrm{N}}
$$

The magnitude of the force is

$$
\boxed{|\vec F_2|=0.539\ \mathrm{N}}
$$

The potential energy of the system is

$$
\boxed{U=-0.270\ \mathrm{J}}
$$

The work required to separate the charges to a distance of $2\ \mathrm{m}$ is

$$
\boxed{W_{\text{ext}}=0.202\ \mathrm{J}}
$$

Because the charges have opposite signs, the force is attractive. Therefore, the force on $q_2$ points from $q_2$ back toward $q_1$, which is why both components of the force vector are negative.
