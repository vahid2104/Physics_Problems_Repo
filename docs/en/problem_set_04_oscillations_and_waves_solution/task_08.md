
---

# Problem 8 – Two coupled springs (two degrees of freedom)

Two masses (m_1) and (m_2) are connected to fixed walls by three springs with constants (k_1), (k_2), and (k_3).

We denote by

* (x_1(t)) the displacement of mass (m_1) from equilibrium,
* (x_2(t)) the displacement of mass (m_2) from equilibrium.

We want to determine:

1. the equations of motion,
2. the natural frequencies,
3. the normal modes,
4. a numerical solution for arbitrary initial conditions,
5. the energy exchange between the masses.

---

## 1. Equations of motion

Let us write the force acting on each mass.

---

### 1.1 Force on mass (m_1)

Mass (m_1) is attached:

* to the left wall by spring (k_1),
* to mass (m_2) by spring (k_2).

#### Force from spring (k_1)

If mass (m_1) is displaced by (x_1), then spring (k_1) is stretched or compressed by (x_1).

So the restoring force is

$$
F_{k_1}=-k_1 x_1
$$

#### Force from spring (k_2)

The middle spring depends on the relative displacement of the masses.

Its extension is

$$
x_2-x_1
$$

So the force exerted by spring (k_2) on mass (m_1) is

$$
F_{k_2 \to m_1}=k_2(x_2-x_1)
$$

Therefore, the total force on (m_1) is

$$
m_1 \ddot{x}_1=-k_1 x_1+k_2(x_2-x_1)
$$

Simplify:

$$
m_1 \ddot{x}_1=-(k_1+k_2)x_1+k_2 x_2
$$

So the first equation of motion is

$$
m_1 \ddot{x}_1+(k_1+k_2)x_1-k_2 x_2=0
$$

---

### 1.2 Force on mass (m_2)

Mass (m_2) is attached:

* to mass (m_1) by spring (k_2),
* to the right wall by spring (k_3).

#### Force from spring (k_3)

If mass (m_2) moves by (x_2), the restoring force from the right spring is

$$
F_{k_3}=-k_3 x_2
$$

#### Force from spring (k_2)

Again, the extension of the middle spring is

$$
x_2-x_1
$$

The force on mass (m_2) is opposite to that on (m_1), so

$$
F_{k_2 \to m_2}=-k_2(x_2-x_1)=k_2(x_1-x_2)
$$

Therefore,

$$
m_2 \ddot{x}_2=-k_3 x_2+k_2(x_1-x_2)
$$

Simplify:

$$
m_2 \ddot{x}_2=k_2 x_1-(k_2+k_3)x_2
$$

So the second equation of motion is

$$
m_2 \ddot{x}_2-k_2 x_1+(k_2+k_3)x_2=0
$$

---

## 2. Final form of the equations of motion

Therefore, the system is

$$
m_1 \ddot{x}_1+(k_1+k_2)x_1-k_2 x_2=0
$$

$$
m_2 \ddot{x}_2-k_2 x_1+(k_2+k_3)x_2=0
$$

This is a system of **two coupled second-order differential equations**.

---

## 3. Determine the natural frequencies

To find the natural frequencies, we look for oscillatory solutions of the form

$$
x_1(t)=A_1 \cos(\omega t)
$$

$$
x_2(t)=A_2 \cos(\omega t)
$$

It is often easier to use the equivalent form

$$
x_1(t)=A_1 e^{i\omega t}, \qquad x_2(t)=A_2 e^{i\omega t}
$$

Then

$$
\ddot{x}_1=-\omega^2 x_1, \qquad \ddot{x}_2=-\omega^2 x_2
$$

Substitute into the equations of motion:

$$
-m_1\omega^2 A_1+(k_1+k_2)A_1-k_2A_2=0
$$

$$
-k_2A_1+(k_2+k_3)A_2-m_2\omega^2 A_2=0
$$

So we get the algebraic system

$$
\bigl((k_1+k_2)-m_1\omega^2\bigr)A_1-k_2A_2=0
$$

$$
-k_2A_1+\bigl((k_2+k_3)-m_2\omega^2\bigr)A_2=0
$$

---

### 3.1 Matrix form

This can be written as

$$
\begin{pmatrix}
(k_1+k_2)-m_1\omega^2 & -k_2 \
-k_2 & (k_2+k_3)-m_2\omega^2
\end{pmatrix}
\begin{pmatrix}
A_1 \ A_2
\end{pmatrix}
=============

\begin{pmatrix}
0 \ 0
\end{pmatrix}
$$

For a nonzero solution, the determinant must be zero:

$$
\begin{vmatrix}
(k_1+k_2)-m_1\omega^2 & -k_2 \
-k_2 & (k_2+k_3)-m_2\omega^2
\end{vmatrix}
=0
$$

So

$$
\bigl((k_1+k_2)-m_1\omega^2\bigr)\bigl((k_2+k_3)-m_2\omega^2\bigr)-k_2^2=0
$$

---

### 3.2 Characteristic equation

Expand this:

$$
m_1m_2\omega^4-\Bigl[m_2(k_1+k_2)+m_1(k_2+k_3)\Bigr]\omega^2+\Bigl[(k_1+k_2)(k_2+k_3)-k_2^2\Bigr]=0
$$

This is a quadratic equation in (\omega^2).

Therefore,

$$
\omega_{1,2}^2=
\frac{
m_2(k_1+k_2)+m_1(k_2+k_3)
\pm
\sqrt{
\Bigl[m_2(k_1+k_2)+m_1(k_2+k_3)\Bigr]^2
-4m_1m_2\Bigl[(k_1+k_2)(k_2+k_3)-k_2^2\Bigr]
}
}{
2m_1m_2
}
$$

So the natural frequencies are

$$
\omega_1=\sqrt{\omega_1^2}, \qquad \omega_2=\sqrt{\omega_2^2}
$$

---

## 4. Find the normal modes

For each natural frequency, we substitute back into

$$
\bigl((k_1+k_2)-m_1\omega^2\bigr)A_1-k_2A_2=0
$$

From this,

$$
k_2A_2=\bigl((k_1+k_2)-m_1\omega^2\bigr)A_1
$$

So the amplitude ratio is

$$
\frac{A_2}{A_1}=\frac{(k_1+k_2)-m_1\omega^2}{k_2}
$$

Thus, for each frequency (\omega_n), the normal mode has the form

$$
\mathbf{v}^{(n)}=
\begin{pmatrix}
1 \
\dfrac{(k_1+k_2)-m_1\omega_n^2}{k_2}
\end{pmatrix}
\qquad n=1,2
$$

These vectors tell us how the two masses move relative to each other.

---

## 5. Simple symmetric example

To make the result easier to understand, let us choose a simple case:

$$
m_1=m_2=m
$$

$$
k_1=k_2=k_3=k
$$

Then the equations become

$$
m\ddot{x}_1+2kx_1-kx_2=0
$$

$$
m\ddot{x}_2-kx_1+2kx_2=0
$$

---

### 5.1 Natural frequencies in the symmetric case

The determinant condition becomes

$$
\begin{vmatrix}
2k-m\omega^2 & -k \
-k & 2k-m\omega^2
\end{vmatrix}
=0
$$

So

$$
(2k-m\omega^2)^2-k^2=0
$$

This gives

$$
2k-m\omega^2=\pm k
$$

So there are two cases.

#### First case

$$
2k-m\omega^2=k
$$

Hence

$$
m\omega^2=k
$$

$$
\omega_1=\sqrt{\frac{k}{m}}
$$

#### Second case

$$
2k-m\omega^2=-k
$$

Hence

$$
m\omega^2=3k
$$

$$
\omega_2=\sqrt{\frac{3k}{m}}
$$

Therefore, for the symmetric system,

$$
\omega_1=\sqrt{\frac{k}{m}}, \qquad \omega_2=\sqrt{\frac{3k}{m}}
$$

---

### 5.2 Normal modes in the symmetric case

#### Mode 1: (\omega_1=\sqrt{k/m})

Substitute into

$$
(2k-m\omega^2)A_1-kA_2=0
$$

Since (m\omega_1^2=k),

$$
(2k-k)A_1-kA_2=0
$$

$$
kA_1-kA_2=0
$$

$$
A_1=A_2
$$

So the first normal mode is

$$
\mathbf{v}^{(1)}=
\begin{pmatrix}
1\
1
\end{pmatrix}
$$

This means both masses move **in the same direction together**.

---

#### Mode 2: (\omega_2=\sqrt{3k/m})

Now (m\omega_2^2=3k), so

$$
(2k-3k)A_1-kA_2=0
$$

$$
-kA_1-kA_2=0
$$

$$
A_2=-A_1
$$

So the second normal mode is

$$
\mathbf{v}^{(2)}=
\begin{pmatrix}
1\
-1
\end{pmatrix}
$$

This means the masses move **in opposite directions**.

---

## 6. Numerical solution for arbitrary initial conditions

Now let us solve numerically for a specific set of initial conditions.

We choose the simple numerical example

$$
m_1=m_2=1
$$

$$
k_1=k_2=k_3=1
$$

and initial conditions

$$
x_1(0)=0.2,\qquad x_2(0)=0
$$

$$
\dot{x}_1(0)=0,\qquad \dot{x}_2(0)=0
$$

For these values, from the previous section,

$$
\omega_1=1
$$

$$
\omega_2=\sqrt{3}
$$

The normal modes are

$$
\mathbf{v}^{(1)}=
\begin{pmatrix}
1\
1
\end{pmatrix},
\qquad
\mathbf{v}^{(2)}=
\begin{pmatrix}
1\
-1
\end{pmatrix}
$$

---

### 6.1 Write the general solution

The general motion is a combination of the two modes:

$$
\begin{pmatrix}
x_1(t)\
x_2(t)
\end{pmatrix}
=============

C_1
\begin{pmatrix}
1\
1
\end{pmatrix}
\cos(\omega_1 t)
+
C_2
\begin{pmatrix}
1\
-1
\end{pmatrix}
\cos(\omega_2 t)
$$

Since the initial velocities are zero, cosine terms are enough.

So

$$
x_1(t)=C_1\cos t+C_2\cos(\sqrt{3},t)
$$

$$
x_2(t)=C_1\cos t-C_2\cos(\sqrt{3},t)
$$

---

### 6.2 Apply the initial conditions

At (t=0),

$$
x_1(0)=C_1+C_2=0.2
$$

$$
x_2(0)=C_1-C_2=0
$$

Add the equations:

$$
2C_1=0.2
$$

$$
C_1=0.1
$$

Subtract the equations:

$$
2C_2=0.2
$$

$$
C_2=0.1
$$

Therefore,

$$
x_1(t)=0.1\cos t+0.1\cos(\sqrt{3},t)
$$

$$
x_2(t)=0.1\cos t-0.1\cos(\sqrt{3},t)
$$

This is the numerical motion for the chosen initial conditions.

---

## 7. Identify the energy exchange between the masses

Now let us understand the physics.

The total mechanical energy of the system is conserved:

$$
E=
\frac12 m_1\dot{x}_1^2+\frac12 m_2\dot{x}_2^2
+\frac12 k_1x_1^2
+\frac12 k_2(x_2-x_1)^2
+\frac12 k_3x_2^2
$$

This total energy remains constant if there is no damping.

---

### 7.1 Energy of each mass

To talk about energy exchange between the masses, we can assign half of the middle spring energy to each side.

Then

$$
E_1=
\frac12 m_1\dot{x}_1^2
+\frac12 k_1x_1^2
+\frac14 k_2(x_2-x_1)^2
$$

$$
E_2=
\frac12 m_2\dot{x}_2^2
+\frac12 k_3x_2^2
+\frac14 k_2(x_2-x_1)^2
$$

and

$$
E=E_1+E_2
$$

So:

* (E_1) changes with time,
* (E_2) changes with time,
* but the total (E) stays constant.

---

### 7.2 Physical meaning

Because the masses are coupled by spring (k_2),

* one mass can give energy to the other,
* then the other can give energy back.

So the amplitudes appear to “share” energy.

In the motion

$$
x_1(t)=0.1\cos t+0.1\cos(\sqrt{3},t)
$$

$$
x_2(t)=0.1\cos t-0.1\cos(\sqrt{3},t)
$$

the two normal modes interfere with each other.

That interference causes the motion to shift back and forth between the masses.

So sometimes:

* mass (m_1) has larger motion,
* later mass (m_2) has larger motion.

That is the **energy exchange**.

---

## 8. Interpretation of the two normal modes

It is useful to understand the two modes physically.

### First mode: in-phase motion

$$
\mathbf{v}^{(1)}=
\begin{pmatrix}
1\
1
\end{pmatrix}
$$

Both masses move together.

Since the middle spring changes length only a little, this mode has the **lower frequency**.

---

### Second mode: opposite-phase motion

$$
\mathbf{v}^{(2)}=
\begin{pmatrix}
1\
-1
\end{pmatrix}
$$

The masses move in opposite directions.

Now the middle spring stretches and compresses much more, so the restoring force is stronger.

Therefore this mode has the **higher frequency**.

---

## Final answers for Problem 8

The equations of motion are

$$
m_1 \ddot{x}_1+(k_1+k_2)x_1-k_2 x_2=0
$$

$$
m_2 \ddot{x}_2-k_2 x_1+(k_2+k_3)x_2=0
$$

The natural frequencies are obtained from

$$
\bigl((k_1+k_2)-m_1\omega^2\bigr)\bigl((k_2+k_3)-m_2\omega^2\bigr)-k_2^2=0
$$

or equivalently

$$
m_1m_2\omega^4-\Bigl[m_2(k_1+k_2)+m_1(k_2+k_3)\Bigr]\omega^2+\Bigl[(k_1+k_2)(k_2+k_3)-k_2^2\Bigr]=0
$$

The normal modes are

$$
\mathbf{v}^{(n)}=
\begin{pmatrix}
1 \
\dfrac{(k_1+k_2)-m_1\omega_n^2}{k_2}
\end{pmatrix},
\qquad n=1,2
$$

For the simple case

$$
m_1=m_2=1,\qquad k_1=k_2=k_3=1
$$

we get

$$
\omega_1=1,\qquad \omega_2=\sqrt{3}
$$

with normal modes

$$
\begin{pmatrix}
1\
1
\end{pmatrix}
\qquad \text{and} \qquad
\begin{pmatrix}
1\
-1
\end{pmatrix}
$$

For initial conditions

$$
x_1(0)=0.2,\quad x_2(0)=0,\quad \dot{x}_1(0)=0,\quad \dot{x}_2(0)=0
$$

the motion is

$$
x_1(t)=0.1\cos t+0.1\cos(\sqrt{3},t)
$$

$$
x_2(t)=0.1\cos t-0.1\cos(\sqrt{3},t)
$$

The total energy is conserved, but energy moves back and forth between the two masses through the coupling spring (k_2).

---


