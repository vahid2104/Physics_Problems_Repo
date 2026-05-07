# Problem 1 – Potential and energy

For a point charge

$$
q=4\ \mu\mathrm{C}
$$

we need to calculate:

* the electric potential at (r=0.3\ \mathrm{m}),
* the potential difference between (0.3\ \mathrm{m}) and (0.6\ \mathrm{m}),
* the work done to move a test charge (q_0=2\ \mu\mathrm{C}),
* the electric field intensity using the derivative of the potential,
* and compare the result with Coulomb’s law.

---

## Given data

The charge is

$$
q=4\ \mu\mathrm{C}
$$

Since

$$
1\ \mu\mathrm{C}=10^{-6}\ \mathrm{C}
$$

we write

$$
q=4\times 10^{-6}\ \mathrm{C}
$$

The test charge is

$$
q_0=2\ \mu\mathrm{C}
$$

so

$$
q_0=2\times 10^{-6}\ \mathrm{C}
$$

The Coulomb constant is

$$
k=8.99\times 10^9\ \mathrm{N,m^2/C^2}
$$

---

## 1. Electric potential at (r=0.3\ \mathrm{m})

The electric potential due to a point charge is

$$
V(r)=\frac{kq}{r}
$$

Substitute the values:

$$
V(0.3)=\frac{(8.99\times 10^9)(4\times 10^{-6})}{0.3}
$$

First multiply the numerator:

$$
(8.99\times 10^9)(4\times 10^{-6})
$$

$$
=35.96\times 10^3
$$

$$
=35960
$$

So

$$
V(0.3)=\frac{35960}{0.3}
$$

$$
V(0.3)=119866.7\ \mathrm{V}
$$

Therefore,

$$
V(0.3)\approx 1.20\times 10^5\ \mathrm{V}
$$

---

## 2. Potential difference between (0.3\ \mathrm{m}) and (0.6\ \mathrm{m})

First calculate the potential at

$$
r=0.6\ \mathrm{m}
$$

Using

$$
V(r)=\frac{kq}{r}
$$

we get

$$
V(0.6)=\frac{(8.99\times 10^9)(4\times 10^{-6})}{0.6}
$$

We already found the numerator:

$$
(8.99\times 10^9)(4\times 10^{-6})=35960
$$

So

$$
V(0.6)=\frac{35960}{0.6}
$$

$$
V(0.6)=59933.3\ \mathrm{V}
$$

Therefore,

$$
V(0.6)\approx 5.99\times 10^4\ \mathrm{V}
$$

Now the potential difference from (0.3\ \mathrm{m}) to (0.6\ \mathrm{m}) is

$$
\Delta V=V(0.6)-V(0.3)
$$

Substitute:

$$
\Delta V=59933.3-119866.7
$$

$$
\Delta V=-59933.4\ \mathrm{V}
$$

Therefore,

$$
\Delta V\approx -5.99\times 10^4\ \mathrm{V}
$$

The negative sign means the potential decreases when we move farther away from the positive charge.

The magnitude of the potential difference is

$$
|\Delta V|\approx 5.99\times 10^4\ \mathrm{V}
$$

---

## 3. Work done to move the test charge

The change in electric potential energy is

$$
\Delta U=q_0\Delta V
$$

Substitute the values:

$$
\Delta U=(2\times 10^{-6})(-59933.4)
$$

$$
\Delta U=-0.1198668\ \mathrm{J}
$$

Therefore,

$$
\Delta U\approx -0.120\ \mathrm{J}
$$

This means the potential energy decreases by about

$$
0.120\ \mathrm{J}
$$

when the test charge moves from (0.3\ \mathrm{m}) to (0.6\ \mathrm{m}).

---

### Work done by the electric field

The work done by the electric field is

$$
W_{\text{field}}=-\Delta U
$$

So

$$
W_{\text{field}}=-(-0.1198668)
$$

$$
W_{\text{field}}=0.1198668\ \mathrm{J}
$$

Therefore,

$$
W_{\text{field}}\approx 0.120\ \mathrm{J}
$$

So the electric field does positive work because the positive test charge naturally moves away from the positive source charge.

---

### Work done by an external force

If an external force moves the charge slowly from (0.3\ \mathrm{m}) to (0.6\ \mathrm{m}), then

$$
W_{\text{external}}=\Delta U
$$

So

$$
W_{\text{external}}\approx -0.120\ \mathrm{J}
$$

The negative sign means the external force removes energy from the charge-field system.

---

## 4. Electric field intensity from the derivative of potential

The electric field is related to the electric potential by

$$
E=-\frac{dV}{dr}
$$

The potential is

$$
V(r)=\frac{kq}{r}
$$

This can also be written as

$$
V(r)=kq r^{-1}
$$

Now differentiate:

$$
\frac{dV}{dr}=kq(-1)r^{-2}
$$

So

$$
\frac{dV}{dr}=-\frac{kq}{r^2}
$$

Using

$$
E=-\frac{dV}{dr}
$$

we get

$$
E=-\left(-\frac{kq}{r^2}\right)
$$

Therefore,

$$
E=\frac{kq}{r^2}
$$

Now calculate the electric field at

$$
r=0.3\ \mathrm{m}
$$

$$
E(0.3)=\frac{(8.99\times 10^9)(4\times 10^{-6})}{(0.3)^2}
$$

Since

$$
(0.3)^2=0.09
$$

we get

$$
E(0.3)=\frac{35960}{0.09}
$$

$$
E(0.3)=399555.6\ \mathrm{N/C}
$$

Therefore,

$$
E(0.3)\approx 4.00\times 10^5\ \mathrm{N/C}
$$

Because the source charge is positive, the electric field points outward, away from the charge.

---

## 5. Compare with Coulomb’s law

According to Coulomb’s law, the force on a test charge is

$$
F=\frac{kqq_0}{r^2}
$$

But electric field is force per unit charge:

$$
E=\frac{F}{q_0}
$$

Substitute Coulomb’s law into this formula:

$$
E=\frac{1}{q_0}\frac{kqq_0}{r^2}
$$

The (q_0) cancels:

$$
E=\frac{kq}{r^2}
$$

This is exactly the same result we got from the derivative of the potential:

$$
E=-\frac{dV}{dr}=\frac{kq}{r^2}
$$

Therefore, the derivative method and Coulomb’s law give the same electric field.

---

## Final answers for Problem 1

The electric potential at (r=0.3\ \mathrm{m}) is

$$
V(0.3)\approx 1.20\times 10^5\ \mathrm{V}
$$

The electric potential at (r=0.6\ \mathrm{m}) is

$$
V(0.6)\approx 5.99\times 10^4\ \mathrm{V}
$$

The potential difference from (0.3\ \mathrm{m}) to (0.6\ \mathrm{m}) is

$$
\Delta V\approx -5.99\times 10^4\ \mathrm{V}
$$

The change in potential energy of the test charge is

$$
\Delta U\approx -0.120\ \mathrm{J}
$$

The work done by the electric field is

$$
W_{\text{field}}\approx 0.120\ \mathrm{J}
$$

The electric field intensity at (r=0.3\ \mathrm{m}) is

$$
E(0.3)\approx 4.00\times 10^5\ \mathrm{N/C}
$$

The electric field found from the derivative of the potential is

$$
E=\frac{kq}{r^2}
$$

This agrees with Coulomb’s law. ✅
