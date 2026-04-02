Of course 🙂 Here is **Problem 10** written in the same simple, step-by-step style as your **Problem 1**.

---

# Problem 10 – Numerical model of a dynamical system

Consider motion in a one-dimensional potential

$$
U(x)=\frac{k}{2}x^2+\lambda x^4
$$

We need to determine:

* the force,
* the equation of motion,
* a numerical solution for selected parameters,
* the effect of initial energy on the type of motion,
* the visualization of $x(t)$ and the phase portrait.

---

## 1. Force

The force is related to the potential energy by

$$
F(x)=-\frac{dU}{dx}
$$

So first we calculate the derivative of

$$
U(x)=\frac{k}{2}x^2+\lambda x^4
$$

Differentiate term by term:

$$
\frac{d}{dx}\left(\frac{k}{2}x^2\right)=kx
$$

$$
\frac{d}{dx}(\lambda x^4)=4\lambda x^3
$$

Therefore,

$$
\frac{dU}{dx}=kx+4\lambda x^3
$$

So the force is

$$
F(x)=-(kx+4\lambda x^3)
$$

Therefore,

$$
F(x)=-kx-4\lambda x^3
$$

---

## 2. Equation of motion

From Newton’s second law,

$$
m\ddot x=F(x)
$$

Substitute the force found above:

$$
m\ddot x=-kx-4\lambda x^3
$$

So the equation of motion is

$$
m\ddot x+kx+4\lambda x^3=0
$$

This is a **nonlinear differential equation** because of the term $x^3$.

Therefore,

$$
m\ddot x+kx+4\lambda x^3=0
$$

---

## 3. Rewrite as a system of first-order equations

For numerical solving, it is easier to introduce the velocity

$$
v=\dot x
$$

Then

$$
\dot x=v
$$

and

$$
\dot v=\ddot x
$$

From the equation of motion,

$$
m\dot v=-kx-4\lambda x^3
$$

so

$$
\dot v=-\frac{k}{m}x-\frac{4\lambda}{m}x^3
$$

Thus the system becomes

$$
\dot x=v
$$

$$
\dot v=-\frac{k}{m}x-\frac{4\lambda}{m}x^3
$$

This is the form used in numerical calculations.

---

## 4. Selected parameters

Let us choose simple parameters:

$$
m=1,\qquad k=1,\qquad \lambda=0.25
$$

Then the potential becomes

$$
U(x)=\frac12 x^2+0.25x^4
$$

The force becomes

$$
F(x)=-x-x^3
$$

because

$$
4\lambda=4\cdot 0.25=1
$$

So the equation of motion is

$$
\ddot x=-x-x^3
$$

or equivalently

$$
\dot x=v
$$

$$
\dot v=-x-x^3
$$

---

## 5. Initial conditions

To solve numerically, we must choose initial conditions.

For example, take

$$
x(0)=1,\qquad v(0)=0
$$

This means:

* the particle starts at position $x=1$,
* the initial velocity is zero.

The initial energy is

$$
E=\frac12 mv^2+U(x)
$$

Since $m=1$, $v(0)=0$, and $x(0)=1$,

$$
E=\frac12\cdot 0^2+\frac12\cdot 1^2+0.25\cdot 1^4
$$

$$
E=0+\frac12+0.25
$$

$$
E=0.75
$$

So the initial energy is

$$
E=0.75
$$

---

## 6. Numerical method

Because the equation

$$
\ddot x=-x-x^3
$$

is nonlinear, it is usually not solved by a simple exact formula.

So we solve it **numerically**.

A basic numerical idea is:

1. choose a small time step $\Delta t$,
2. update position and velocity step by step.

For example, with the Euler method:

$$
x_{n+1}=x_n+v_n\Delta t
$$

$$
v_{n+1}=v_n+\left(-x_n-x_n^3\right)\Delta t
$$

This method is simple, although in practice a better method such as **Runge–Kutta** is more accurate.

---

## 7. Example of numerical evolution

Take:

$$
m=1,\qquad k=1,\qquad \lambda=0.25
$$

with initial conditions

$$
x(0)=1,\qquad v(0)=0
$$

Then:

* the particle starts on the right side,
* the force is negative,
* so it begins to move toward the origin,
* after passing near the center, it slows down on the other side,
* then it turns back.

Thus the motion is **oscillatory**.

But it is not exactly the same as in the ordinary harmonic oscillator, because the quartic term changes the shape of the potential.

The restoring force is stronger for larger $|x|$, so the oscillation is nonlinear.

---

## 8. Effect of initial energy on the motion

The total energy is

$$
E=\frac12 mv^2+\frac{k}{2}x^2+\lambda x^4
$$

Since the potential

$$
U(x)=\frac{k}{2}x^2+\lambda x^4
$$

is always nonnegative and grows strongly for large $|x|$, the particle is trapped in a potential well around $x=0$.

That means the motion remains **bounded**.

### Case 1: Small initial energy

If the energy is small, then $x$ stays near the origin.

Near $x=0$, the quartic term is small, so the potential looks approximately like

$$
U(x)\approx \frac{k}{2}x^2
$$

This is similar to a harmonic oscillator.

So for small energy:

* the motion is close to sinusoidal,
* the phase portrait is close to an ellipse.

---

### Case 2: Larger initial energy

If the energy is larger, the particle moves farther from the origin.

Then the term $\lambda x^4$ becomes important.

So:

* the restoring force becomes stronger,
* the motion becomes more nonlinear,
* the oscillation is no longer perfectly sinusoidal,
* the phase portrait is no longer an ellipse.

---

### Important conclusion

Because the potential increases to $+\infty$ as $|x|\to\infty$, the particle cannot escape.

So for positive $k$ and positive $\lambda$:

* low energy gives nearly harmonic oscillations,
* higher energy gives stronger nonlinear oscillations,
* but the motion is still bounded.

---

## 9. Phase portrait

The phase portrait is the graph of

$$
v(t)=\dot x(t)
$$

versus

$$
x(t)
$$

For this system:

* each trajectory is a closed curve,
* small-energy trajectories are almost elliptical,
* high-energy trajectories are more distorted.

This happens because the system is conservative and the energy stays constant.

The phase curves satisfy

$$
\frac12 mv^2+\frac{k}{2}x^2+\lambda x^4=E
$$

So the phase portrait is determined by the energy level.

---

## 10. Example code for numerical solution

Here is a simple Python example using `solve_ivp`:

```python
import numpy as np
import matplotlib.pyplot as plt
from scipy.integrate import solve_ivp

# parameters
m = 1.0
k = 1.0
lam = 0.25

# system of equations
def system(t, y):
    x, v = y
    dxdt = v
    dvdt = -(k/m)*x - (4*lam/m)*x**3
    return [dxdt, dvdt]

# initial conditions
x0 = 1.0
v0 = 0.0

# time interval
t_span = (0, 20)
t_eval = np.linspace(0, 20, 2000)

# numerical solution
sol = solve_ivp(system, t_span, [x0, v0], t_eval=t_eval)

# plots
plt.figure(figsize=(10,4))
plt.plot(sol.t, sol.y[0])
plt.xlabel('t')
plt.ylabel('x(t)')
plt.title('Position as a function of time')
plt.grid()
plt.show()

plt.figure(figsize=(5,5))
plt.plot(sol.y[0], sol.y[1])
plt.xlabel('x')
plt.ylabel('v')
plt.title('Phase portrait')
plt.grid()
plt.show()
```

---

## 11. Interpretation of the graphs

### Graph of $x(t)$

The graph of $x(t)$ shows oscillations.

For small amplitudes:

* the graph looks similar to a sine wave.

For larger amplitudes:

* the graph becomes less sinusoidal,
* the nonlinear term affects the shape of the oscillation.

---

### Phase portrait

The phase portrait shows how velocity changes with position.

* For small energy, the curve looks almost like an ellipse.
* For larger energy, the curve becomes more stretched and distorted.
* The curve remains closed because the motion is periodic and bounded.

---

## 12. Final answers for Problem 10

The potential is

$$
U(x)=\frac{k}{2}x^2+\lambda x^4
$$

The force is

$$
F(x)=-\frac{dU}{dx}=-kx-4\lambda x^3
$$

The equation of motion is

$$
m\ddot x+kx+4\lambda x^3=0
$$

or as a first-order system,

$$
\dot x=v
$$

$$
\dot v=-\frac{k}{m}x-\frac{4\lambda}{m}x^3
$$

For example, with

$$
m=1,\qquad k=1,\qquad \lambda=0.25,\qquad x(0)=1,\qquad v(0)=0
$$

the motion is oscillatory and bounded.

The effect of initial energy is:

* **small energy** $\rightarrow$ motion close to harmonic,
* **larger energy** $\rightarrow$ stronger nonlinear oscillation,
* the phase portrait changes from an almost ellipse to a more distorted closed curve.

The graph of $x(t)$ shows the oscillation in time, and the phase portrait shows the relation between position and velocity.

---

