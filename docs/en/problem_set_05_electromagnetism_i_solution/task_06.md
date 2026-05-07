# Problem 6 – 2D field map

We need to study the electric field made by **three point charges in a plane**.

We will do five things:

* implement a function for the field vector
* generate a vector field map
* find the equilibrium point numerically
* investigate stability using small displacement
* compare with the case of two charges

---

## System: three charges in a plane

We choose three equal positive charges placed at the corners of an equilateral triangle.

Each charge is

$$
q=1\ \mu\mathrm{C}
$$

Since

$$
1\ \mu\mathrm{C}=10^{-6}\ \mathrm{C}
$$

we write

$$
q=1\times 10^{-6}\ \mathrm{C}
$$

The Coulomb constant is

$$
k=8.99\times 10^9\ \mathrm{N,m^2/C^2}
$$

We place the charges at

$$
(1,0)
$$

$$
\left(-\frac{1}{2},\frac{\sqrt{3}}{2}\right)
$$

$$
\left(-\frac{1}{2},-\frac{\sqrt{3}}{2}\right)
$$

These three points form an equilateral triangle centered at the origin.

So the charges are arranged symmetrically around

$$
(0,0)
$$

---

# 1. Electric field vector function

For one point charge, the electric field at a point ((x,y)) is

$$
\vec E = kq\frac{\vec r}{|\vec r|^3}
$$

where

$$
\vec r = \vec r_{\text{field point}}-\vec r_{\text{charge}}
$$

If the charge is located at

$$
(x_i,y_i)
$$

and the field point is

$$
(x,y)
$$

then

$$
\vec r = (x-x_i,\ y-y_i)
$$

The distance is

$$
r=\sqrt{(x-x_i)^2+(y-y_i)^2}
$$

Therefore, the field from one charge is

$$
\vec E_i
========

kq_i
\frac{(x-x_i,\ y-y_i)}{\left[(x-x_i)^2+(y-y_i)^2\right]^{3/2}}
$$

For three charges, we add the three fields:

$$
\vec E=\vec E_1+\vec E_2+\vec E_3
$$

So,

$$
E_x = \sum_i kq_i\frac{x-x_i}{r_i^3}
$$

and

$$
E_y = \sum_i kq_i\frac{y-y_i}{r_i^3}
$$

---

## Python implementation

```python
import numpy as np

k = 8.99e9

charges = [
    {"q": 1e-6, "pos": np.array([1.0, 0.0])},
    {"q": 1e-6, "pos": np.array([-0.5, np.sqrt(3)/2])},
    {"q": 1e-6, "pos": np.array([-0.5, -np.sqrt(3)/2])}
]

def electric_field(x, y):
    """
    Calculates the electric field vector E(x,y)
    caused by all charges.
    """
    point = np.array([x, y])
    E = np.array([0.0, 0.0])

    for charge in charges:
        q = charge["q"]
        pos = charge["pos"]

        r_vec = point - pos
        r = np.linalg.norm(r_vec)

        # avoid division by zero at the exact charge position
        if r < 1e-12:
            continue

        E += k * q * r_vec / r**3

    return E
```

This function returns

$$
\vec E(x,y)=(E_x,E_y)
$$

---

# 2. Generate a vector field map

To make a field map, we calculate the electric field on many points of a grid.

For example, we can choose

$$
-2 \le x \le 2
$$

and

$$
-2 \le y \le 2
$$

At each grid point, we calculate

$$
\vec E(x,y)
$$

Then we draw arrows showing the direction of the electric field.

---

## Python code for the vector field map

```python
import matplotlib.pyplot as plt

# Create grid
x_values = np.linspace(-2, 2, 25)
y_values = np.linspace(-2, 2, 25)

X, Y = np.meshgrid(x_values, y_values)

Ex = np.zeros_like(X)
Ey = np.zeros_like(Y)

# Calculate electric field at each grid point
for i in range(X.shape[0]):
    for j in range(X.shape[1]):
        E = electric_field(X[i, j], Y[i, j])
        Ex[i, j] = E[0]
        Ey[i, j] = E[1]

# Normalize arrows so the plot is easier to see
E_mag = np.sqrt(Ex**2 + Ey**2)
Ex_norm = Ex / E_mag
Ey_norm = Ey / E_mag

plt.figure(figsize=(7, 7))
plt.quiver(X, Y, Ex_norm, Ey_norm)

# Plot charge positions
for charge in charges:
    pos = charge["pos"]
    plt.scatter(pos[0], pos[1], s=100)

plt.xlabel("x position (m)")
plt.ylabel("y position (m)")
plt.title("Electric Field Map for Three Charges")
plt.axis("equal")
plt.grid(True)
plt.show()
```

The arrows show the direction of the electric field.

Because all charges are positive, the electric field points **away** from each charge.

---

# 3. Find the equilibrium point numerically

An equilibrium point is a point where the net electric field is zero:

$$
\vec E(x,y)=0
$$

This means

$$
E_x(x,y)=0
$$

and

$$
E_y(x,y)=0
$$

Because the charges are arranged symmetrically, we expect the equilibrium point to be at the center of the triangle:

$$
(x,y)=(0,0)
$$

But now we find it numerically.

---

## Numerical method

We define a function whose output is

$$
(E_x,E_y)
$$

Then we use a root-finding method to solve

$$
E_x=0
$$

and

$$
E_y=0
$$

---

## Python code

```python
from scipy.optimize import root

def field_equations(point):
    x, y = point
    E = electric_field(x, y)
    return [E[0], E[1]]

initial_guess = [0.1, 0.1]

solution = root(field_equations, initial_guess)

equilibrium_point = solution.x
E_at_equilibrium = electric_field(equilibrium_point[0], equilibrium_point[1])

print("Equilibrium point:", equilibrium_point)
print("Electric field there:", E_at_equilibrium)
```

The numerical result should be approximately

$$
(x,y)=(0,0)
$$

So,

$$
\boxed{(x_{\text{eq}},y_{\text{eq}})\approx(0,0)}
$$

At this point,

$$
\vec E(0,0)\approx(0,0)
$$

Therefore, a test charge placed exactly at the center feels no net electric force.

---

# 4. Stability of the equilibrium point

Now we investigate what happens if the test charge is moved slightly away from the equilibrium point.

The equilibrium point is

$$
(0,0)
$$

Let us move the test charge slightly in the (x)-direction:

$$
(x,y)=(0.01,0)
$$

Then we calculate the electric field.

---

## Python code for small displacement

```python
small_points = [
    [0.01, 0.0],
    [-0.01, 0.0],
    [0.0, 0.01],
    [0.0, -0.01]
]

for p in small_points:
    E = electric_field(p[0], p[1])
    print("Point:", p, "Electric field:", E)
```

For this symmetric three-charge system, near the center we get approximately

$$
\vec E \approx -C(x,y)
$$

where (C) is a positive constant.

For our values,

$$
C \approx 1.35\times 10^4\ \mathrm{N/(C,m)}
$$

So,

$$
E_x \approx -1.35\times 10^4 x
$$

and

$$
E_y \approx -1.35\times 10^4 y
$$

---

## Meaning of the negative sign

If the charge is displaced slightly to the right,

$$
x>0
$$

then

$$
E_x<0
$$

So the electric field points back to the left.

If the charge is displaced slightly to the left,

$$
x<0
$$

then

$$
E_x>0
$$

So the electric field points back to the right.

Similarly, in the (y)-direction, the field also points back toward the origin.

Therefore, in the 2D plane,

$$
\boxed{\text{the equilibrium point is stable for small in-plane displacement}}
$$

---

## Numerical Jacobian method

A more formal way is to calculate the Jacobian matrix of the electric field:

$$
J=
\begin{bmatrix}
\frac{\partial E_x}{\partial x} & \frac{\partial E_x}{\partial y} \
\frac{\partial E_y}{\partial x} & \frac{\partial E_y}{\partial y}
\end{bmatrix}
$$

At the equilibrium point, this matrix tells us how the field changes for small displacement.

---

## Python code for the Jacobian

```python
def numerical_jacobian(func, point, h=1e-5):
    x, y = point

    E_x_plus = func(x + h, y)
    E_x_minus = func(x - h, y)
    dE_dx = (E_x_plus - E_x_minus) / (2*h)

    E_y_plus = func(x, y + h)
    E_y_minus = func(x, y - h)
    dE_dy = (E_y_plus - E_y_minus) / (2*h)

    J = np.column_stack((dE_dx, dE_dy))
    return J

J = numerical_jacobian(electric_field, equilibrium_point)

print("Jacobian matrix:")
print(J)

eigenvalues, eigenvectors = np.linalg.eig(J)

print("Eigenvalues:")
print(eigenvalues)
```

For this system, the Jacobian is approximately

$$
J\approx
\begin{bmatrix}
-1.35\times 10^4 & 0 \
0 & -1.35\times 10^4
\end{bmatrix}
$$

The eigenvalues are approximately

$$
\lambda_1\approx -1.35\times 10^4
$$

and

$$
\lambda_2\approx -1.35\times 10^4
$$

Both eigenvalues are negative.

So the electric field points back toward the equilibrium point for small displacement in the plane.

Therefore,

$$
\boxed{\text{the equilibrium point is stable in the 2D plane}}
$$

Small note: in full 3D electrostatics, stable equilibrium of charges is not possible without extra constraints. But since this problem is a **2D field map**, we are investigating motion only inside the plane.

---

# 5. Compare with the case of two charges

Now compare this with two equal positive charges.

Place two charges at

$$
(-1,0)
$$

and

$$
(1,0)
$$

Both charges are

$$
q=1\ \mu\mathrm{C}
$$

---

## Two-charge electric field function

```python
charges_two = [
    {"q": 1e-6, "pos": np.array([-1.0, 0.0])},
    {"q": 1e-6, "pos": np.array([1.0, 0.0])}
]

def electric_field_two(x, y):
    point = np.array([x, y])
    E = np.array([0.0, 0.0])

    for charge in charges_two:
        q = charge["q"]
        pos = charge["pos"]

        r_vec = point - pos
        r = np.linalg.norm(r_vec)

        if r < 1e-12:
            continue

        E += k * q * r_vec / r**3

    return E
```

By symmetry, the equilibrium point is at the midpoint:

$$
(x,y)=(0,0)
$$

At this point, the field from the left charge points to the right, and the field from the right charge points to the left.

They cancel each other.

So,

$$
\vec E(0,0)=0
$$

Therefore,

$$
\boxed{(x_{\text{eq}},y_{\text{eq}})=(0,0)}
$$

---

## Stability for two charges

Now check small displacement.

Near the center, the field behaves approximately like

$$
E_x \approx -3.60\times 10^4 x
$$

but

$$
E_y \approx +1.80\times 10^4 y
$$

So in the (x)-direction, the field points back toward the origin.

But in the (y)-direction, the field points away from the origin.

That means the equilibrium is stable in one direction but unstable in another direction.

This is called a **saddle point**.

So for two equal positive charges,

$$
\boxed{\text{the equilibrium point is unstable in the 2D plane}}
$$

---

# Physical comparison

For three equal positive charges arranged as an equilateral triangle:

$$
\boxed{\vec E=0 \text{ at the center}}
$$

and small in-plane displacements produce a restoring electric field.

So in the 2D plane, the equilibrium is stable.

For two equal positive charges:

$$
\boxed{\vec E=0 \text{ at the midpoint}}
$$

but the equilibrium is stable only along the line joining the charges and unstable perpendicular to it.

So the two-charge equilibrium is a saddle point.

---

# Final answers for Problem 6

The electric field due to several point charges in a plane is

$$
\vec E(x,y)=
\sum_i
kq_i
\frac{(x-x_i,\ y-y_i)}
{\left[(x-x_i)^2+(y-y_i)^2\right]^{3/2}}
$$

For the three-charge example with equal positive charges at the corners of an equilateral triangle, the numerical equilibrium point is

$$
\boxed{(x_{\text{eq}},y_{\text{eq}})\approx(0,0)}
$$

At this point,

$$
\boxed{\vec E(0,0)\approx(0,0)}
$$

For small displacement from the center,

$$
\vec E\approx -C(x,y)
$$

where

$$
C\approx 1.35\times 10^4\ \mathrm{N/(C,m)}
$$

So the field points back toward the center.

Therefore, in the 2D plane,

$$
\boxed{\text{the three-charge equilibrium is stable for small displacement}}
$$

For two equal positive charges, the equilibrium point is also at the midpoint:

$$
\boxed{(0,0)}
$$

but it is stable in one direction and unstable in another direction.

Therefore,

$$
\boxed{\text{the two-charge equilibrium is a saddle point and is unstable}}
$$

So the main comparison is:

$$
\boxed{\text{three charges can give a stable-looking 2D center equilibrium}}
$$

while

$$
\boxed{\text{two charges give an unstable saddle equilibrium}}
$$

✅
