# Problem 9 – Harmonic oscillator

Given:

$$
\frac{d^2 x}{dt^2}+\omega^2 x=0
$$

We need to determine:

- the general solution,
- the solution for given initial conditions,
- and the functions \(x(t)\), \(x'(t)\), \(x''(t)\) for selected parameters and initial conditions.

---

## 1. Solve the differential equation

We start with

$$
\frac{d^2 x}{dt^2}+\omega^2 x=0
$$

This is a linear second-order differential equation with constant coefficients.

We look for a solution in the exponential form

$$
x(t)=e^{rt}
$$

Then

$$
x'(t)=re^{rt}, \qquad x''(t)=r^2 e^{rt}
$$

Substitute into the equation:

$$
r^2 e^{rt}+\omega^2 e^{rt}=0
$$

Factor out \(e^{rt}\neq 0\):

$$
e^{rt}(r^2+\omega^2)=0
$$

So the characteristic equation is

$$
r^2+\omega^2=0
$$

Hence

$$
r=\pm i\omega
$$

The general real solution corresponding to these roots is

$$
x(t)=C_1\cos(\omega t)+C_2\sin(\omega t)
$$

Therefore, the **general solution** is

$$
x(t)=C_1\cos(\omega t)+C_2\sin(\omega t)
$$

---

## 2. First derivative \( x'(t) \)

Differentiate the general solution:

$$
x(t)=C_1\cos(\omega t)+C_2\sin(\omega t)
$$

Using the chain rule:

$$
\frac{d}{dt}\cos(\omega t)=-\omega\sin(\omega t)
$$

$$
\frac{d}{dt}\sin(\omega t)=\omega\cos(\omega t)
$$

Therefore:

$$
x'(t)=-C_1\omega\sin(\omega t)+C_2\omega\cos(\omega t)
$$

---

## 3. Second derivative \( x''(t) \)

Differentiate \(x'(t)\) once again:

$$
x'(t)=-C_1\omega\sin(\omega t)+C_2\omega\cos(\omega t)
$$

So:

$$
x''(t)=-C_1\omega^2\cos(\omega t)-C_2\omega^2\sin(\omega t)
$$

Factor out \(-\omega^2\):

$$
x''(t)=-\omega^2\left(C_1\cos(\omega t)+C_2\sin(\omega t)\right)
$$

Since

$$
x(t)=C_1\cos(\omega t)+C_2\sin(\omega t)
$$

we get

$$
x''(t)=-\omega^2 x(t)
$$

which confirms the differential equation.

---

## 4. Solution for given initial conditions

Let the initial conditions be

$$
x(0)=x_0, \qquad x'(0)=v_0
$$

We now determine the constants \(C_1\) and \(C_2\).

### From \( x(0)=x_0 \)

Substitute \(t=0\) into the general solution:

$$
x(0)=C_1\cos 0+C_2\sin 0
$$

Since

$$
\cos 0=1,\qquad \sin 0=0
$$

we get

$$
x(0)=C_1
$$

Thus:

$$
C_1=x_0
$$

---

### From \( x'(0)=v_0 \)

Use

$$
x'(t)=-C_1\omega\sin(\omega t)+C_2\omega\cos(\omega t)
$$

Substitute \(t=0\):

$$
x'(0)=-C_1\omega\sin 0+C_2\omega\cos 0
$$

So

$$
x'(0)=C_2\omega
$$

Thus:

$$
C_2=\frac{v_0}{\omega}
$$

---

## 5. Final solution for the initial conditions

Substitute \(C_1=x_0\) and \(C_2=\dfrac{v_0}{\omega}\) into the general solution:

$$
x(t)=x_0\cos(\omega t)+\frac{v_0}{\omega}\sin(\omega t)
$$

Differentiate to get velocity:

$$
x'(t)=-x_0\omega\sin(\omega t)+v_0\cos(\omega t)
$$

Differentiate once more to get acceleration:

$$
x''(t)=-x_0\omega^2\cos(\omega t)-v_0\omega\sin(\omega t)
$$

or equivalently,

$$
x''(t)=-\omega^2 x(t)
$$

---

## 6. Interpretation of the solution

The solution

$$
x(t)=x_0\cos(\omega t)+\frac{v_0}{\omega}\sin(\omega t)
$$

describes an oscillatory motion.

Important properties:

- the motion is periodic,
- the angular frequency is \( \omega \),
- the period is

$$
T=\frac{2\pi}{\omega}
$$

A larger \( \omega \) means faster oscillation and a shorter period.

The acceleration is always directed opposite to the displacement:

$$
x''(t)=-\omega^2 x(t)
$$

This is why the motion is called **harmonic oscillation**.

---

## 7. Alternative amplitude-phase form

Sometimes the solution is written as

$$
x(t)=A\cos(\omega t+\varphi)
$$

where:

- \(A\) is the amplitude,
- \(\varphi\) is the phase shift.

This form is equivalent to

$$
x(t)=C_1\cos(\omega t)+C_2\sin(\omega t)
$$

because the two constants can be combined into amplitude and phase.

---

## 8. What to show in the HTML/JS visualization

In the application, it is useful to let the user change:

- the frequency parameter \( \omega \),
- the initial position \( x_0=x(0) \),
- the initial velocity \( v_0=x'(0) \).

Then plot the three functions:

$$
x(t)=x_0\cos(\omega t)+\frac{v_0}{\omega}\sin(\omega t)
$$

$$
x'(t)=-x_0\omega\sin(\omega t)+v_0\cos(\omega t)
$$

$$
x''(t)=-\omega^2 x(t)
$$

### What should be visible in the graph

- \(x(t)\) is the position,
- \(x'(t)\) is the velocity,
- \(x''(t)\) is the acceleration,
- changing \( \omega \) changes the period,
- changing \(x_0\) changes the starting displacement,
- changing \(v_0\) changes the starting slope of the motion.

---

## Final answers for Problem 9

The **general solution** of

$$
\frac{d^2 x}{dt^2}+\omega^2 x=0
$$

is

$$
x(t)=C_1\cos(\omega t)+C_2\sin(\omega t)
$$

For the initial conditions

$$
x(0)=x_0,\qquad x'(0)=v_0
$$

the solution is

$$
x(t)=x_0\cos(\omega t)+\frac{v_0}{\omega}\sin(\omega t)
$$

The first derivative is

$$
x'(t)=-x_0\omega\sin(\omega t)+v_0\cos(\omega t)
$$

The second derivative is

$$
x''(t)=-x_0\omega^2\cos(\omega t)-v_0\omega\sin(\omega t)
$$

or equivalently

$$
x''(t)=-\omega^2 x(t)
$$

The period of the oscillation is

$$
T=\frac{2\pi}{\omega}
$$