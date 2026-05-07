# Problem 10 – Field flux

## Verification of Gauss’s law

We need to:

* define electric field flux,
* consider a sphere around a point charge,
* approximate the flux numerically using grid points,
* check how the result changes when the number of points changes,
* compare the numerical result with the analytical result from Gauss’s law.

---

## Given data

Let the point charge be

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

The Coulomb constant is

$$
k=8.99\times 10^9\ \mathrm{N,m^2/C^2}
$$

The permittivity of free space is

$$
\varepsilon_0=8.854\times 10^{-12}\ \mathrm{C^2/(N,m^2)}
$$

We choose a spherical surface with radius

$$
R=0.3\ \mathrm{m}
$$

The point charge is placed at the center of the sphere.

---

# 1. Definition of electric field flux

Electric field flux tells us how much electric field passes through a surface.

It is defined as

$$
\Phi_E=\int \vec{E}\cdot d\vec{A}
$$

where:

* $\Phi_E$ is the electric flux,
* $\vec{E}$ is the electric field,
* $d\vec{A}$ is a small area vector,
* the dot product means we only count the part of the electric field perpendicular to the surface.

For a closed surface, we write

$$
\Phi_E=\oint \vec{E}\cdot d\vec{A}
$$

The circle on the integral means the surface is closed.

---

# 2. Sphere around a point charge

For a point charge, the electric field is

$$
E=\frac{kq}{r^2}
$$

On a sphere of radius $R$, every point on the sphere is the same distance from the charge.

So on the surface of the sphere,

$$
r=R
$$

Therefore,

$$
E=\frac{kq}{R^2}
$$

Because the charge is at the center, the electric field points directly outward.

The area vector $d\vec{A}$ also points outward.

So the angle between $\vec{E}$ and $d\vec{A}$ is

$$
0^\circ
$$

This means

$$
\vec{E}\cdot d\vec{A}=E,dA
$$

because

$$
\cos(0^\circ)=1
$$

---

# 3. Analytical flux through the sphere

The total flux is

$$
\Phi_E=\oint E,dA
$$

Since $E$ is constant everywhere on the sphere, we can take it outside the integral:

$$
\Phi_E=E\oint dA
$$

The total surface area of a sphere is

$$
A=4\pi R^2
$$

So

$$
\Phi_E=E(4\pi R^2)
$$

Now substitute

$$
E=\frac{kq}{R^2}
$$

Then

$$
\Phi_E=\frac{kq}{R^2}(4\pi R^2)
$$

The $R^2$ cancels:

$$
\Phi_E=4\pi kq
$$

Since

$$
k=\frac{1}{4\pi\varepsilon_0}
$$

we get

$$
\Phi_E=4\pi\left(\frac{1}{4\pi\varepsilon_0}\right)q
$$

The $4\pi$ cancels:

$$
\Phi_E=\frac{q}{\varepsilon_0}
$$

This is Gauss’s law:

$$
\boxed{\Phi_E=\frac{q}{\varepsilon_0}}
$$

---

## Calculate the analytical result

Substitute:

$$
q=4\times 10^{-6}\ \mathrm{C}
$$

and

$$
\varepsilon_0=8.854\times 10^{-12}\ \mathrm{C^2/(N,m^2)}
$$

So

$$
\Phi_E=\frac{4\times 10^{-6}}{8.854\times 10^{-12}}
$$

Now divide:

$$
\Phi_E=451772081.5\ \mathrm{N,m^2/C}
$$

Therefore,

$$
\Phi_E\approx 4.52\times 10^8\ \mathrm{N,m^2/C}
$$

This is the exact analytical flux predicted by Gauss’s law.

---

# 4. Discrete approximation of the flux

Instead of using the exact integral, we approximate the sphere using many small surface pieces.

The flux is

$$
\Phi_E=\oint \vec{E}\cdot d\vec{A}
$$

In a numerical approximation, the integral becomes a sum:

$$
\Phi_E\approx \sum_i \vec{E}_i\cdot \Delta \vec{A}_i
$$

where:

* $i$ labels each small grid point or surface patch,
* $\vec{E}_i$ is the electric field at that point,
* $\Delta \vec{A}_i$ is a small area vector.

For a sphere centered on the charge, the field is perpendicular to the surface, so

$$
\vec{E}_i\cdot \Delta \vec{A}_i=E_i\Delta A_i
$$

If we divide the sphere into $N$ equal small area elements, then each area element is approximately

$$
\Delta A=\frac{4\pi R^2}{N}
$$

At every point on the sphere,

$$
E_i=\frac{kq}{R^2}
$$

So the numerical flux is

$$
\Phi_E\approx \sum_{i=1}^{N} E_i\Delta A
$$

Since $E_i$ is the same for every point,

$$
\Phi_E\approx N\left(\frac{kq}{R^2}\right)\left(\frac{4\pi R^2}{N}\right)
$$

The $N$ cancels:

$$
\Phi_E\approx 4\pi kq
$$

So even the discrete method should give the Gauss’s law result, as long as the grid correctly represents the spherical surface.

---

# 5. Python implementation

Here is a simple Python code for the discrete approximation:

```python
import numpy as np

# Given data
q = 4e-6
k = 8.99e9
epsilon_0 = 8.854e-12
R = 0.3

# Analytical result from Gauss's law
flux_analytical = q / epsilon_0

# Different numbers of grid points
N_values = [10, 50, 100, 500, 1000, 5000, 10000]

print("N\tNumerical flux\t\tAnalytical flux\t\tRelative error")

for N in N_values:
    # Area of one small surface element
    dA = 4 * np.pi * R**2 / N
    
    # Electric field magnitude on the sphere
    E = k * q / R**2
    
    # Discrete approximation of flux
    flux_numerical = 0
    
    for i in range(N):
        flux_numerical += E * dA
    
    # Relative error
    relative_error = abs(flux_numerical - flux_analytical) / flux_analytical
    
    print(N, flux_numerical, flux_analytical, relative_error)
```

---

# 6. Explanation of the code

First, we define the charge:

$$
q=4\times 10^{-6}\ \mathrm{C}
$$

Then we define the Coulomb constant:

$$
k=8.99\times 10^9
$$

We also define the radius of the sphere:

$$
R=0.3\ \mathrm{m}
$$

The analytical flux is calculated using Gauss’s law:

$$
\Phi_E=\frac{q}{\varepsilon_0}
$$

In the code, this is written as:

```python
flux_analytical = q / epsilon_0
```

Then we test different values of $N$:

```python
N_values = [10, 50, 100, 500, 1000, 5000, 10000]
```

Here, $N$ means the number of small surface pieces.

For each value of $N$, the area of one small piece is

$$
\Delta A=\frac{4\pi R^2}{N}
$$

In the code:

```python
dA = 4 * np.pi * R**2 / N
```

The electric field on the sphere is

$$
E=\frac{kq}{R^2}
$$

In the code:

```python
E = k * q / R**2
```

Then the flux is calculated by adding many small parts:

$$
\Phi_E\approx \sum_{i=1}^{N} E\Delta A
$$

In the code:

```python
for i in range(N):
    flux_numerical += E * dA
```

Finally, the relative error is calculated:

$$
\text{Relative error}
=====================

\frac{|\Phi_{\text{numerical}}-\Phi_{\text{analytical}}|}
{\Phi_{\text{analytical}}}
$$

---

# 7. Numerical values

First calculate the electric field on the sphere.

The electric field is

$$
E=\frac{kq}{R^2}
$$

Substitute the values:

$$
E=\frac{(8.99\times 10^9)(4\times 10^{-6})}{(0.3)^2}
$$

First multiply the numerator:

$$
(8.99\times 10^9)(4\times 10^{-6})=35960
$$

Also,

$$
(0.3)^2=0.09
$$

So

$$
E=\frac{35960}{0.09}
$$

$$
E=399555.6\ \mathrm{N/C}
$$

Therefore,

$$
E\approx 4.00\times 10^5\ \mathrm{N/C}
$$

Now calculate the surface area of the sphere:

$$
A=4\pi R^2
$$

Substitute:

$$
A=4\pi(0.3)^2
$$

$$
A=4\pi(0.09)
$$

$$
A=1.131\ \mathrm{m^2}
$$

Now the flux is

$$
\Phi_E=EA
$$

Substitute:

$$
\Phi_E=(399555.6)(1.131)
$$

$$
\Phi_E\approx 4.52\times 10^5\ \mathrm{N,m^2/C}
$$

But wait: this result uses

$$
k=8.99\times 10^9
$$

So analytically,

$$
\Phi_E=4\pi kq
$$

Substitute:

$$
\Phi_E=4\pi(8.99\times 10^9)(4\times 10^{-6})
$$

$$
\Phi_E\approx 4.52\times 10^5\ \mathrm{N,m^2/C}
$$

Using Gauss’s law,

$$
\Phi_E=\frac{q}{\varepsilon_0}
$$

$$
\Phi_E=\frac{4\times 10^{-6}}{8.854\times 10^{-12}}
$$

$$
\Phi_E\approx 4.52\times 10^5\ \mathrm{N,m^2/C}
$$

So both methods agree.

---

# 8. Dependence on number of grid points

Using the simple equal-area approximation, the result is almost the same for every $N$.

Example table:

| Number of grid points $N$ | Numerical flux $\Phi_E$ | Analytical flux $\frac{q}{\varepsilon_0}$ |      Error |
| ------------------------: | ----------------------: | ----------------------------------------: | ---------: |
|                        10 |       $4.52\times 10^5$ |                         $4.52\times 10^5$ | very small |
|                        50 |       $4.52\times 10^5$ |                         $4.52\times 10^5$ | very small |
|                       100 |       $4.52\times 10^5$ |                         $4.52\times 10^5$ | very small |
|                       500 |       $4.52\times 10^5$ |                         $4.52\times 10^5$ | very small |
|                      1000 |       $4.52\times 10^5$ |                         $4.52\times 10^5$ | very small |
|                      5000 |       $4.52\times 10^5$ |                         $4.52\times 10^5$ | very small |

For this special case, the numerical result does not depend strongly on $N$, because:

* the charge is exactly at the center,
* the surface is a sphere,
* the electric field has the same magnitude everywhere on the sphere,
* the electric field is perpendicular to the sphere everywhere.

So even a small number of grid points gives a good result.

However, in a more complicated case, for example if the charge were not at the center or the surface were not a sphere, then using more grid points would give a better approximation.

---

# 9. Compare with analytical result

The numerical approximation gives

$$
\Phi_{\text{numerical}}\approx 4.52\times 10^5\ \mathrm{N,m^2/C}
$$

The analytical result from Gauss’s law is

$$
\Phi_{\text{analytical}}=\frac{q}{\varepsilon_0}
$$

Substitute:

$$
\Phi_{\text{analytical}}=\frac{4\times 10^{-6}}{8.854\times 10^{-12}}
$$

$$
\Phi_{\text{analytical}}\approx 4.52\times 10^5\ \mathrm{N,m^2/C}
$$

Therefore,

$$
\Phi_{\text{numerical}}\approx \Phi_{\text{analytical}}
$$

This verifies Gauss’s law.

---

# Final answers for Problem 10

The electric flux is defined as

$$
\Phi_E=\oint \vec{E}\cdot d\vec{A}
$$

For a point charge at the center of a sphere, the electric field is

$$
E=\frac{kq}{R^2}
$$

The surface area of the sphere is

$$
A=4\pi R^2
$$

So the flux is

$$
\Phi_E=EA
$$

Substitute:

$$
\Phi_E=\frac{kq}{R^2}(4\pi R^2)
$$

Therefore,

$$
\Phi_E=4\pi kq
$$

Since

$$
k=\frac{1}{4\pi\varepsilon_0}
$$

we get

$$
\Phi_E=\frac{q}{\varepsilon_0}
$$

For

$$
q=4\times 10^{-6}\ \mathrm{C}
$$

the flux is

$$
\Phi_E\approx 4.52\times 10^5\ \mathrm{N,m^2/C}
$$

The discrete approximation is

$$
\Phi_E\approx \sum_i \vec{E}_i\cdot \Delta \vec{A}_i
$$

Using more grid points usually improves the approximation.

For a centered charge inside a spherical surface, the numerical result agrees very well with the analytical result.

Therefore, the calculation verifies Gauss’s law:

$$
\boxed{\Phi_E=\frac{q}{\varepsilon_0}}
$$

✅
