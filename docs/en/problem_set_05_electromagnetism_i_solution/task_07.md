# Problem 7 – Motion in a central field

For the electric field

$$
\vec E(r)=k\frac{Q}{r^2}\hat r
$$

we need to:

* write the equation of motion of a charged particle,
* consider radial motion,
* implement the RK4 method,
* investigate positive and negative energy,
* and compare with the gravitational analogy.

---

## Given field

The electric field is

$$
\vec E(r)=k\frac{Q}{r^2}\hat r
$$

where

$$
k=8.99\times 10^9\ \mathrm{N,m^2/C^2}
$$

and

$$
Q
$$

is the source charge placed at the origin.

The vector

$$
\hat r
$$

means the radial direction.

So the electric field points:

* outward if (Q>0),
* inward if (Q<0).

---

# 1. Equation of motion of the particle

Suppose a particle has charge

$$
q
$$

and mass

$$
m
$$

The electric force on the particle is

$$
\vec F=q\vec E
$$

Substitute the electric field:

$$
\vec F=q\left(k\frac{Q}{r^2}\hat r\right)
$$

So

$$
\vec F=k\frac{qQ}{r^2}\hat r
$$

Using Newton’s second law,

$$
\vec F=m\vec a
$$

we get

$$
m\vec a=k\frac{qQ}{r^2}\hat r
$$

Therefore,

$$
\vec a=\frac{kqQ}{mr^2}\hat r
$$

So the equation of motion is

$$
m\ddot{\vec r}=k\frac{qQ}{r^2}\hat r
$$

or

$$
\ddot{\vec r}=\frac{kqQ}{mr^2}\hat r
$$

---

## Important sign of the force

The quantity

$$
qQ
$$

decides whether the force is repulsive or attractive.

If

$$
qQ>0
$$

then the charges have the same sign.

So the force is repulsive.

If

$$
qQ<0
$$

then the charges have opposite signs.

So the force is attractive.

---

# 2. Case of radial motion

Radial motion means the particle moves only along the line joining it to the source charge.

So the position is described only by

$$
r(t)
$$

There is no angular motion.

That means

$$
\theta=\text{constant}
$$

and the angular momentum is zero:

$$
L=0
$$

The acceleration becomes only radial:

$$
\ddot r=\frac{kqQ}{mr^2}
$$

So the radial equation of motion is

$$
m\ddot r=k\frac{qQ}{r^2}
$$

or

$$
\ddot r=\frac{kqQ}{mr^2}
$$

---

## Define a useful constant

Let

$$
\alpha=\frac{kqQ}{m}
$$

Then the radial equation becomes

$$
\ddot r=\frac{\alpha}{r^2}
$$

This is simpler to use in numerical calculations.

If

$$
\alpha>0
$$

the motion is repulsive.

If

$$
\alpha<0
$$

the motion is attractive.

---

# 3. First-order system for RK4

The RK4 method works best with first-order differential equations.

But our equation is second order:

$$
\ddot r=\frac{\alpha}{r^2}
$$

So we introduce velocity:

$$
v=\dot r
$$

Then we write the system as:

$$
\frac{dr}{dt}=v
$$

and

$$
\frac{dv}{dt}=\frac{\alpha}{r^2}
$$

Therefore, the first-order system is

$$
\boxed{
\begin{aligned}
\dot r &= v \
\dot v &= \frac{\alpha}{r^2}
\end{aligned}
}
$$

This is the system we solve using RK4.

---

# 4. Energy of the particle

The electric potential energy of charge (q) in the field of charge (Q) is

$$
U(r)=k\frac{qQ}{r}
$$

The kinetic energy is

$$
K=\frac12 mv^2
$$

So the total mechanical energy is

$$
E=K+U
$$

Therefore,

$$
E=\frac12 mv^2+k\frac{qQ}{r}
$$

Using

$$
\alpha=\frac{kqQ}{m}
$$

we can also write energy per unit mass as

$$
\varepsilon=\frac{E}{m}
$$

So

$$
\varepsilon=\frac12 v^2+\frac{kqQ}{mr}
$$

Since

$$
\alpha=\frac{kqQ}{m}
$$

we get

$$
\varepsilon=\frac12 v^2+\frac{\alpha}{r}
$$

---

## Energy formula

So the energy per unit mass is

$$
\boxed{
\varepsilon=\frac12 v^2+\frac{\alpha}{r}
}
$$

This energy should remain constant during the motion if there are no losses.

That means we can use energy conservation to check whether the RK4 simulation is accurate.

---

# 5. Positive and negative energy

Now we investigate two cases:

$$
\varepsilon>0
$$

and

$$
\varepsilon<0
$$

The meaning depends strongly on whether the force is attractive or repulsive.

---

## Case A: Repulsive electric field

For repulsion,

$$
qQ>0
$$

so

$$
\alpha>0
$$

The potential energy is

$$
U(r)=k\frac{qQ}{r}
$$

Since (qQ>0),

$$
U(r)>0
$$

So the energy is

$$
E=\frac12 mv^2+k\frac{qQ}{r}
$$

Both terms are positive:

$$
\frac12 mv^2>0
$$

and

$$
k\frac{qQ}{r}>0
$$

Therefore,

$$
E>0
$$

So for repulsive electric motion, the total energy is normally positive.

The particle is pushed away from the source charge.

---

## Physical meaning

If the particle starts near the source charge, it experiences a strong repulsive force.

As it moves away, its potential energy decreases.

The decrease in potential energy becomes kinetic energy.

So the particle speeds up as it moves outward.

At very large distance,

$$
r\to \infty
$$

the potential energy becomes

$$
U(r)\to 0
$$

So the final energy is mostly kinetic:

$$
E\approx \frac12 mv_\infty^2
$$

---

## Case B: Attractive electric field

For attraction,

$$
qQ<0
$$

so

$$
\alpha<0
$$

The potential energy is

$$
U(r)=k\frac{qQ}{r}
$$

Since (qQ<0),

$$
U(r)<0
$$

So the total energy is

$$
E=\frac12 mv^2-\frac{k|qQ|}{r}
$$

or

$$
E=\frac12 mv^2+\frac{kqQ}{r}
$$

where (qQ<0).

Now the energy can be:

* positive,
* zero,
* or negative.

---

# 6. Negative energy for attraction

If

$$
E<0
$$

then the particle does not have enough kinetic energy to escape to infinity.

This is called a bound state.

For radial motion, this means the particle moves inward and can fall toward the center.

In an ideal point-charge model, as

$$
r\to 0
$$

the attractive potential energy becomes

$$
U(r)\to -\infty
$$

So the speed can become very large.

This is a limitation of the ideal point-charge model.

Real systems usually need extra physics near very small distances.

---

## Condition for negative energy

For attractive motion,

$$
E=\frac12 mv^2-\frac{k|qQ|}{r}
$$

Negative energy means

$$
\frac12 mv^2-\frac{k|qQ|}{r}<0
$$

Move the potential term to the other side:

$$
\frac12 mv^2<\frac{k|qQ|}{r}
$$

So

$$
v^2<\frac{2k|qQ|}{mr}
$$

Therefore,

$$
v<\sqrt{\frac{2k|qQ|}{mr}}
$$

This speed is the escape speed.

So if

$$
v<v_{\text{esc}}
$$

then

$$
E<0
$$

and the particle is bound.

---

# 7. Positive energy for attraction

If

$$
E>0
$$

then the particle has enough kinetic energy to escape.

At infinity,

$$
r\to \infty
$$

the potential energy becomes

$$
U(r)\to 0
$$

So the total energy becomes kinetic energy:

$$
E=\frac12 mv_\infty^2
$$

Since (E>0), the final velocity is not zero.

Therefore, the particle escapes to infinity with nonzero final speed.

---

## Condition for positive energy

For attractive motion,

$$
E=\frac12 mv^2-\frac{k|qQ|}{r}
$$

Positive energy means

$$
\frac12 mv^2-\frac{k|qQ|}{r}>0
$$

So

$$
\frac12 mv^2>\frac{k|qQ|}{r}
$$

Therefore,

$$
v>\sqrt{\frac{2k|qQ|}{mr}}
$$

So if

$$
v>v_{\text{esc}}
$$

the particle escapes.

---

# 8. Zero energy

The boundary case is

$$
E=0
$$

Then

$$
\frac12 mv^2=\frac{k|qQ|}{r}
$$

So

$$
v=\sqrt{\frac{2k|qQ|}{mr}}
$$

This is exactly the escape speed:

$$
v_{\text{esc}}=\sqrt{\frac{2k|qQ|}{mr}}
$$

If the particle has this speed, it can just escape to infinity, but its final speed at infinity becomes zero.

So:

$$
E<0
$$

means bound motion.

$$
E=0
$$

means just enough energy to escape.

$$
E>0
$$

means escape with leftover speed.

---

# 9. RK4 method

We solve the system:

$$
\dot r=v
$$

$$
\dot v=\frac{\alpha}{r^2}
$$

Let the state vector be

$$
y=
\begin{pmatrix}
r \
v
\end{pmatrix}
$$

Then

$$
\frac{dy}{dt}
=============

# f(t,y)

\begin{pmatrix}
v \
\alpha/r^2
\end{pmatrix}
$$

---

## RK4 formulas

For a time step

$$
h
$$

the RK4 method is:

$$
k_1=f(t_n,y_n)
$$

$$
k_2=f\left(t_n+\frac h2,\ y_n+\frac h2 k_1\right)
$$

$$
k_3=f\left(t_n+\frac h2,\ y_n+\frac h2 k_2\right)
$$

$$
k_4=f(t_n+h,\ y_n+hk_3)
$$

Then

$$
y_{n+1}=y_n+\frac h6(k_1+2k_2+2k_3+k_4)
$$

This gives the new position and velocity.

---

# 10. RK4 implementation in Python

Here is a simple RK4 implementation for radial motion.

```python
import numpy as np
import matplotlib.pyplot as plt

# Constants
k = 8.99e9          # Coulomb constant
Q = 1e-6            # source charge, C
q = -1e-6           # moving particle charge, C
m = 1e-3            # particle mass, kg

# alpha = k q Q / m
alpha = k * q * Q / m

# Time settings
h = 0.001           # time step
t_max = 2.0
N = int(t_max / h)

# Initial conditions
r0 = 1.0            # initial radius, m
v0 = 1.0            # initial radial velocity, m/s

# Arrays
t = np.zeros(N)
r = np.zeros(N)
v = np.zeros(N)
energy = np.zeros(N)

# Initial values
r[0] = r0
v[0] = v0

def f(y):
    r, v = y
    
    drdt = v
    dvdt = alpha / r**2
    
    return np.array([drdt, dvdt])

def total_energy(r, v):
    return 0.5 * m * v**2 + k * q * Q / r

# RK4 loop
for n in range(N - 1):
    y = np.array([r[n], v[n]])
    
    k1 = f(y)
    k2 = f(y + 0.5 * h * k1)
    k3 = f(y + 0.5 * h * k2)
    k4 = f(y + h * k3)
    
    y_next = y + (h / 6) * (k1 + 2*k2 + 2*k3 + k4)
    
    r[n+1] = y_next[0]
    v[n+1] = y_next[1]
    t[n+1] = t[n] + h
    
    # Stop if particle gets too close to the origin
    if r[n+1] <= 0.01:
        r = r[:n+2]
        v = v[:n+2]
        t = t[:n+2]
        energy = energy[:n+2]
        break

# Calculate energy
for n in range(len(t)):
    energy[n] = total_energy(r[n], v[n])

# Plot r(t)
plt.figure()
plt.plot(t, r)
plt.xlabel("time t")
plt.ylabel("radius r")
plt.title("Radial motion in central electric field")
plt.grid()
plt.show()

# Plot v(t)
plt.figure()
plt.plot(t, v)
plt.xlabel("time t")
plt.ylabel("radial velocity v")
plt.title("Velocity versus time")
plt.grid()
plt.show()

# Plot energy
plt.figure()
plt.plot(t, energy)
plt.xlabel("time t")
plt.ylabel("total energy E")
plt.title("Energy conservation check")
plt.grid()
plt.show()
```

---

# 11. Explanation of the code

The constant

```python
alpha = k * q * Q / m
```

represents

$$
\alpha=\frac{kqQ}{m}
$$

The function

```python
def f(y):
```

returns the derivatives:

$$
\dot r=v
$$

and

$$
\dot v=\frac{\alpha}{r^2}
$$

The RK4 method updates both (r) and (v) at each time step.

The energy is calculated using

```python
0.5 * m * v**2 + k * q * Q / r
```

which represents

$$
E=\frac12 mv^2+k\frac{qQ}{r}
$$

If the numerical method is accurate, the energy graph should stay almost constant.

Small changes happen because of numerical error.

---

# 12. Example: negative energy case

For attraction, choose opposite signs:

$$
Q>0
$$

and

$$
q<0
$$

So

$$
qQ<0
$$

Example:

$$
Q=1\times 10^{-6}\ \mathrm C
$$

$$
q=-1\times 10^{-6}\ \mathrm C
$$

$$
m=1\times 10^{-3}\ \mathrm{kg}
$$

$$
r_0=1\ \mathrm m
$$

$$
v_0=1\ \mathrm{m/s}
$$

The initial energy is

$$
E=\frac12 mv_0^2+k\frac{qQ}{r_0}
$$

Substitute:

$$
E=\frac12(10^{-3})(1)^2+(8.99\times 10^9)\frac{(1\times 10^{-6})(-1\times 10^{-6})}{1}
$$

First term:

$$
\frac12(10^{-3})(1)^2=5\times 10^{-4}\ \mathrm J
$$

Second term:

$$
(8.99\times 10^9)(-1\times 10^{-12})=-8.99\times 10^{-3}\ \mathrm J
$$

So

$$
E=5\times 10^{-4}-8.99\times 10^{-3}
$$

$$
E=-8.49\times 10^{-3}\ \mathrm J
$$

Therefore,

$$
E<0
$$

This is a negative-energy case.

The particle is attracted toward the center.

---

# 13. Example: positive energy case

Use the same charges and mass:

$$
Q=1\times 10^{-6}\ \mathrm C
$$

$$
q=-1\times 10^{-6}\ \mathrm C
$$

$$
m=1\times 10^{-3}\ \mathrm{kg}
$$

$$
r_0=1\ \mathrm m
$$

but choose larger initial speed:

$$
v_0=5\ \mathrm{m/s}
$$

The energy is

$$
E=\frac12mv_0^2+k\frac{qQ}{r_0}
$$

Substitute:

$$
E=\frac12(10^{-3})(5)^2-8.99\times 10^{-3}
$$

Since

$$
5^2=25
$$

we get

$$
\frac12(10^{-3})(25)=0.0125\ \mathrm J
$$

So

$$
E=0.0125-0.00899
$$

$$
E=0.00351\ \mathrm J
$$

Therefore,

$$
E>0
$$

This is a positive-energy case.

The particle has enough energy to escape from the attractive center.

---

# 14. Escape speed

For attractive motion, the escape speed is

$$
v_{\text{esc}}=\sqrt{\frac{2k|qQ|}{mr}}
$$

Using the same data:

$$
k=8.99\times 10^9
$$

$$
|qQ|=10^{-12}
$$

$$
m=10^{-3}
$$

$$
r=1
$$

we get

$$
v_{\text{esc}}=\sqrt{\frac{2(8.99\times 10^9)(10^{-12})}{10^{-3}(1)}}
$$

Simplify the numerator:

$$
2(8.99\times 10^9)(10^{-12})=1.798\times 10^{-2}
$$

Then

$$
v_{\text{esc}}=\sqrt{\frac{1.798\times 10^{-2}}{10^{-3}}}
$$

$$
v_{\text{esc}}=\sqrt{17.98}
$$

$$
v_{\text{esc}}\approx 4.24\ \mathrm{m/s}
$$

So:

* if (v_0<4.24\ \mathrm{m/s}), then (E<0),
* if (v_0=4.24\ \mathrm{m/s}), then (E=0),
* if (v_0>4.24\ \mathrm{m/s}), then (E>0).

For example:

$$
v_0=1\ \mathrm{m/s}
$$

gives negative energy.

But

$$
v_0=5\ \mathrm{m/s}
$$

gives positive energy.

---

# 15. Comparison with gravitational analogy

The gravitational force between two masses is

$$
F=-G\frac{Mm}{r^2}\hat r
$$

The negative sign means gravity is always attractive.

The gravitational potential energy is

$$
U_g(r)=-G\frac{Mm}{r}
$$

For electric charges, the force is

$$
F_e=k\frac{qQ}{r^2}\hat r
$$

and the potential energy is

$$
U_e(r)=k\frac{qQ}{r}
$$

---

## Main similarity

Both electric and gravitational central fields have an inverse-square form:

$$
F\propto \frac{1}{r^2}
$$

Both potentials have the form:

$$
U\propto \frac{1}{r}
$$

So mathematically, the equations are very similar.

---

## Main difference

Gravity is always attractive:

$$
U_g(r)=-G\frac{Mm}{r}
$$

But the electric force can be attractive or repulsive.

For electricity:

$$
qQ<0
$$

means attraction.

$$
qQ>0
$$

means repulsion.

So electric motion can behave like gravity only when the charges have opposite signs.

---

# 16. Electric case versus gravitational case

For gravity:

$$
E=\frac12mv^2-G\frac{Mm}{r}
$$

For attractive electric motion:

$$
E=\frac12mv^2-k\frac{|qQ|}{r}
$$

These have the same form.

So attractive electric motion is mathematically analogous to gravitational motion.

---

## Escape speed comparison

For gravity, the escape speed is

$$
v_{\text{esc}}=\sqrt{\frac{2GM}{r}}
$$

For attractive electric motion, the escape speed is

$$
v_{\text{esc}}=\sqrt{\frac{2k|qQ|}{mr}}
$$

They look very similar.

The difference is that gravity depends on masses, while the electric case depends on charges and the mass of the moving particle.

---

# 17. Summary of positive and negative energy

For attractive central fields:

$$
E<0
$$

means the particle is bound.

$$
E=0
$$

means the particle just escapes.

$$
E>0
$$

means the particle escapes with nonzero final speed.

For repulsive electric fields:

$$
qQ>0
$$

the force pushes the particle away.

The energy is usually positive because the potential energy is positive.

---

# Final answers for Problem 7

The electric force on the particle is

$$
\vec F=q\vec E
$$

so

$$
\vec F=k\frac{qQ}{r^2}\hat r
$$

Using Newton’s second law,

$$
m\ddot{\vec r}=k\frac{qQ}{r^2}\hat r
$$

Therefore, the equation of motion is

$$
\boxed{
\ddot{\vec r}=\frac{kqQ}{mr^2}\hat r
}
$$

For radial motion,

$$
\boxed{
\ddot r=\frac{kqQ}{mr^2}
}
$$

Using

$$
\alpha=\frac{kqQ}{m}
$$

we write

$$
\boxed{
\dot r=v
}
$$

and

$$
\boxed{
\dot v=\frac{\alpha}{r^2}
}
$$

The total energy is

$$
\boxed{
E=\frac12mv^2+k\frac{qQ}{r}
}
$$

For attractive motion, (qQ<0):

$$
E<0
$$

means bound motion.

$$
E=0
$$

means just enough energy to escape.

$$
E>0
$$

means escape motion.

The RK4 method can be used to solve the system numerically by updating (r) and (v) step by step.

The gravitational analogy is strong because both fields are inverse-square central fields. The difference is that gravity is always attractive, while the electric force can be attractive or repulsive depending on the signs of the charges. ✅
