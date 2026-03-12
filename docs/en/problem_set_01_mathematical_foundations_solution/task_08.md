# Problem 8 – First-order differential equation

Given:

$$
\frac{dy}{dt}=-ky
$$

We need to determine:

- the solution of the differential equation,
- and how the solution behaves for different values of parameter \(k\) and different initial conditions \(y(0)\).

---

## 1. Solve the differential equation

We start with

$$
\frac{dy}{dt}=-ky
$$

This is a **separable differential equation**, so we separate the variables \(y\) and \(t\):

$$
\frac{dy}{y}=-k\,dt
$$

Now integrate both sides:

$$
\int \frac{1}{y}\,dy=\int -k\,dt
$$

This gives

$$
\ln|y|=-kt+C
$$

where \(C\) is the constant of integration.

Now exponentiate both sides:

$$
|y|=e^{-kt+C}
$$

Using the property \(e^{a+b}=e^a e^b\), we get

$$
|y|=e^C e^{-kt}
$$

Since \(e^C\) is just a positive constant, we can write a new arbitrary constant \(C_1\):

$$
y=C_1 e^{-kt}
$$

Therefore, the **general solution** is

$$
y(t)=C e^{-kt}
$$

where \(C\) is an arbitrary constant.

---

## 2. Solution for a given initial condition \( y(0)=y_0 \)

Suppose the initial value is

$$
y(0)=y_0
$$

Substitute \(t=0\) into the general solution:

$$
y(0)=C e^{-k\cdot 0}
$$

$$
y(0)=C e^0=C
$$

So:

$$
C=y_0
$$

Therefore, the solution satisfying the initial condition \(y(0)=y_0\) is

$$
y(t)=y_0 e^{-kt}
$$

---

## 3. Check that the solution is correct

We can verify by differentiation.

Given

$$
y(t)=y_0 e^{-kt}
$$

differentiate with respect to \(t\):

$$
\frac{dy}{dt}=y_0(-k)e^{-kt}
$$

$$
\frac{dy}{dt}=-k y_0 e^{-kt}
$$

Since

$$
y(t)=y_0 e^{-kt}
$$

we get

$$
\frac{dy}{dt}=-k y
$$

So the solution is correct.

---

## 4. Behavior of the solution for different values of \( k \)

The solution is

$$
y(t)=y_0 e^{-kt}
$$

Its behavior depends on the sign and value of \(k\).

### Case 1: \( k>0 \)

Then \(e^{-kt}\) decreases as \(t\) increases.

So the solution **decays exponentially** to zero.

That means:

$$
\lim_{t\to\infty} y(t)=0
$$

if \(k>0\).

A larger value of \(k\) means **faster decay**.

---

### Case 2: \( k=0 \)

Then the equation becomes

$$
\frac{dy}{dt}=0
$$

So the solution is constant:

$$
y(t)=y_0
$$

---

### Case 3: \( k<0 \)

Then \(-k>0\), so \(e^{-kt}=e^{|k|t}\) grows exponentially.

Thus the solution **increases exponentially in magnitude**.

If \(y_0>0\), it grows upward.

If \(y_0<0\), it decreases downward with increasing magnitude.

---

## 5. Influence of the initial condition \( y(0)=y_0 \)

The parameter \(y_0\) determines the starting value of the solution at \(t=0\):

$$
y(0)=y_0
$$

So:

- if \(y_0>0\), the graph starts above the \(t\)-axis,
- if \(y_0<0\), the graph starts below the \(t\)-axis,
- if \(y_0=0\), then

$$
y(t)=0
$$

for all \(t\).

Thus \(y_0\) changes the vertical scale and sign of the solution.

---

## 6. Interpretation of the equation

The equation

$$
\frac{dy}{dt}=-ky
$$

means that the rate of change of \(y\) is proportional to \(y\) itself, but with opposite sign.

So:

- when \(y\) is positive and \(k>0\), the function decreases,
- when \(y\) is negative and \(k>0\), the function increases toward zero,
- the farther \(y\) is from zero, the faster the change.

This is a standard model of **exponential decay**, for example:

- radioactive decay,
- cooling,
- discharge of a capacitor,
- population decrease in simple models.

---

## 7. What to show in the HTML/JS visualization

In the application, it is useful to let the user change:

- the parameter \(k\),
- the initial condition \(y_0=y(0)\).

Then plot the function

$$
y(t)=y_0 e^{-kt}
$$

for a chosen interval of time, for example

$$
t\in[0,5]
$$

### What should be visible in the graph

- For larger positive \(k\), the curve falls faster.
- For smaller positive \(k\), the decay is slower.
- For \(k=0\), the graph is a horizontal line.
- For negative \(k\), the graph grows exponentially.
- Changing \(y_0\) changes the starting point of the graph.

---

## Final answers for Problem 8

The **general solution** of

$$
\frac{dy}{dt}=-ky
$$

is

$$
y(t)=C e^{-kt}
$$

If the initial condition is

$$
y(0)=y_0
$$

then the solution is

$$
y(t)=y_0 e^{-kt}
$$

Behavior of the solution:

- if \(k>0\), the solution decays to zero,
- if \(k=0\), the solution is constant,
- if \(k<0\), the solution grows exponentially.

The parameter \(y_0\) determines the initial value of the solution:

$$
y(0)=y_0
$$