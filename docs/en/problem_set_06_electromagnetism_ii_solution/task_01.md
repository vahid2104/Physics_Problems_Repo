# Problem 1 – Lorentz force

For a charged particle moving in a magnetic field, we need to calculate:

* the Lorentz force acting on the charge,
* the equation of motion,
* the magnitude of the force,
* whether the magnetic force does work,
* the radius of the circular trajectory,
* and how the radius changes when the magnetic field is doubled.

---

## Given data

The magnetic field is

$$
\vec B=(0,0,1)\ \mathrm{T}
$$

The velocity is

$$
\vec v=(2,3,0)\ \mathrm{m/s}
$$

The charge is

$$
q=1\ \mathrm{mC}
$$

Since

$$
1\ \mathrm{mC}=10^{-3}\ \mathrm{C}
$$

we write

$$
q=1\times 10^{-3}\ \mathrm{C}
$$

The mass is

$$
m=0.01\ \mathrm{kg}
$$

---

# 1. Lorentz force acting on the charge

For a charge moving in a magnetic field, the Lorentz force is

$$
\vec F=q(\vec v\times \vec B)
$$

Here, there is only magnetic force because no electric field is given.

We have

$$
\vec v=(2,3,0)
$$

and

$$
\vec B=(0,0,1)
$$

Now calculate the cross product:

$$
\vec v\times \vec B=
\begin{vmatrix}
\vec i & \vec j & \vec k \
2 & 3 & 0 \
0 & 0 & 1
\end{vmatrix}
$$

Using the cross product formula:

$$
\vec v\times \vec B=
(v_yB_z-v_zB_y,\ v_zB_x-v_xB_z,\ v_xB_y-v_yB_x)
$$

Substitute the values:

$$
\vec v\times \vec B=
(3\cdot1-0\cdot0,\ 0\cdot0-2\cdot1,\ 2\cdot0-3\cdot0)
$$

So

$$
\vec v\times \vec B=(3,-2,0)
$$

Now multiply by the charge:

$$
\vec F=q(\vec v\times \vec B)
$$

$$
\vec F=(1\times10^{-3})(3,-2,0)
$$

Therefore,

$$
\vec F=(3\times10^{-3},-2\times10^{-3},0)\ \mathrm{N}
$$

So,

$$
\boxed{\vec F=(0.003,-0.002,0)\ \mathrm{N}}
$$

---

# 2. Equation of motion

Newton’s second law is

$$
\vec F=m\vec a
$$

For magnetic force,

$$
m\frac{d\vec v}{dt}=q(\vec v\times \vec B)
$$

The magnetic field is

$$
\vec B=(0,0,B)
$$

where

$$
B=1\ \mathrm{T}
$$

Let the velocity be

$$
\vec v=(v_x,v_y,v_z)
$$

Then

$$
\vec v\times \vec B=(v_yB,-v_xB,0)
$$

So the equations of motion are

$$
m\frac{dv_x}{dt}=qBv_y
$$

$$
m\frac{dv_y}{dt}=-qBv_x
$$

$$
m\frac{dv_z}{dt}=0
$$

Divide by (m):

$$
\frac{dv_x}{dt}=\frac{qB}{m}v_y
$$

$$
\frac{dv_y}{dt}=-\frac{qB}{m}v_x
$$

$$
\frac{dv_z}{dt}=0
$$

We define the angular frequency:

$$
\omega=\frac{qB}{m}
$$

Substitute the values:

$$
\omega=\frac{(1\times10^{-3})(1)}{0.01}
$$

$$
\omega=0.1\ \mathrm{rad/s}
$$

So,

$$
\omega=0.1\ \mathrm{rad/s}
$$

---

## Initial conditions

At (t=0), the particle is at

$$
(x_0,y_0,z_0)=(0,0,0)
$$

The initial velocity is

$$
\vec v(0)=(2,3,0)
$$

So,

$$
v_x(0)=2
$$

$$
v_y(0)=3
$$

$$
v_z(0)=0
$$

---

## Velocity as a function of time

The solutions for velocity are

$$
v_x(t)=v_{x0}\cos(\omega t)+v_{y0}\sin(\omega t)
$$

$$
v_y(t)=v_{y0}\cos(\omega t)-v_{x0}\sin(\omega t)
$$

Substitute

$$
v_{x0}=2,\quad v_{y0}=3,\quad \omega=0.1
$$

So,

$$
v_x(t)=2\cos(0.1t)+3\sin(0.1t)
$$

and

$$
v_y(t)=3\cos(0.1t)-2\sin(0.1t)
$$

Also,

$$
v_z(t)=0
$$

Therefore,

$$
\boxed{\vec v(t)=
(2\cos(0.1t)+3\sin(0.1t),\ 3\cos(0.1t)-2\sin(0.1t),\ 0)}
$$

---

## Position as a function of time

Velocity is the derivative of position:

$$
v_x=\frac{dx}{dt}
$$

$$
v_y=\frac{dy}{dt}
$$

So we integrate velocity to get position.

---

### Finding (x(t))

$$
x(t)=\int v_x(t),dt
$$

$$
x(t)=\int [2\cos(0.1t)+3\sin(0.1t)],dt
$$

Using

$$
\int \cos(0.1t),dt=10\sin(0.1t)
$$

and

$$
\int \sin(0.1t),dt=-10\cos(0.1t)
$$

we get

$$
x(t)=20\sin(0.1t)-30\cos(0.1t)+C_1
$$

At (t=0),

$$
x(0)=0
$$

Substitute:

$$
0=20\sin(0)-30\cos(0)+C_1
$$

$$
0=0-30+C_1
$$

So,

$$
C_1=30
$$

Therefore,

$$
x(t)=20\sin(0.1t)-30\cos(0.1t)+30
$$

or

$$
\boxed{x(t)=20\sin(0.1t)+30[1-\cos(0.1t)]}
$$

---

### Finding (y(t))

$$
y(t)=\int v_y(t),dt
$$

$$
y(t)=\int [3\cos(0.1t)-2\sin(0.1t)],dt
$$

So,

$$
y(t)=30\sin(0.1t)+20\cos(0.1t)+C_2
$$

At (t=0),

$$
y(0)=0
$$

Substitute:

$$
0=30\sin(0)+20\cos(0)+C_2
$$

$$
0=0+20+C_2
$$

So,

$$
C_2=-20
$$

Therefore,

$$
y(t)=30\sin(0.1t)+20\cos(0.1t)-20
$$

or

$$
\boxed{y(t)=30\sin(0.1t)-20[1-\cos(0.1t)]}
$$

---

### Finding (z(t))

Since

$$
v_z=0
$$

we have

$$
z(t)=0
$$

Therefore,

$$
\boxed{z(t)=0}
$$

---

## Final equation of motion

The position of the particle is

$$
\boxed{
\vec r(t)=
\left(
20\sin(0.1t)+30[1-\cos(0.1t)],
\ 30\sin(0.1t)-20[1-\cos(0.1t)],
\ 0
\right)
}
$$

This motion is circular motion in the (xy)-plane.

---

# 3. Magnitude of the Lorentz force

We found

$$
\vec F=(0.003,-0.002,0)\ \mathrm{N}
$$

The magnitude is

$$
|\vec F|=\sqrt{F_x^2+F_y^2+F_z^2}
$$

Substitute:

$$
|\vec F|=\sqrt{(0.003)^2+(-0.002)^2+0^2}
$$

$$
|\vec F|=\sqrt{9\times10^{-6}+4\times10^{-6}}
$$

$$
|\vec F|=\sqrt{13\times10^{-6}}
$$

$$
|\vec F|=0.0036055\ \mathrm{N}
$$

Therefore,

$$
\boxed{|\vec F|\approx 3.61\times10^{-3}\ \mathrm{N}}
$$

We can also calculate it using

$$
|\vec F|=qvB\sin\theta
$$

Here, (\vec v) is in the (xy)-plane and (\vec B) is along the (z)-axis, so the angle is

$$
\theta=90^\circ
$$

Thus,

$$
\sin 90^\circ=1
$$

The speed is

$$
v=\sqrt{2^2+3^2}
$$

$$
v=\sqrt{13}
$$

$$
v\approx 3.606\ \mathrm{m/s}
$$

Now,

$$
|\vec F|=(1\times10^{-3})(3.606)(1)
$$

$$
|\vec F|\approx 3.606\times10^{-3}\ \mathrm{N}
$$

Same result ✅

---

# 4. Does the magnetic force do work?

Work is given by

$$
W=\vec F\cdot \vec s
$$

or, in power form,

$$
P=\vec F\cdot \vec v
$$

The magnetic force is

$$
\vec F=q(\vec v\times \vec B)
$$

The cross product (\vec v\times \vec B) is always perpendicular to (\vec v).

That means

$$
\vec F\perp \vec v
$$

So,

$$
\vec F\cdot \vec v=0
$$

Therefore, the magnetic force does no work:

$$
\boxed{W=0}
$$

The magnetic force can change the direction of velocity, but it cannot change the speed of the particle.

So the kinetic energy remains constant.

---

# 5. Radius of the trajectory for (m=0.01\ \mathrm{kg})

For circular motion in a magnetic field, the magnetic force provides the centripetal force:

$$
qvB=\frac{mv^2}{r}
$$

Cancel one (v):

$$
qB=\frac{mv}{r}
$$

Solve for (r):

$$
r=\frac{mv}{qB}
$$

Now calculate the speed:

$$
v=\sqrt{v_x^2+v_y^2+v_z^2}
$$

$$
v=\sqrt{2^2+3^2+0^2}
$$

$$
v=\sqrt{13}
$$

$$
v\approx 3.606\ \mathrm{m/s}
$$

Now substitute into the radius formula:

$$
r=\frac{(0.01)(3.606)}{(1\times10^{-3})(1)}
$$

First multiply the numerator:

$$
(0.01)(3.606)=0.03606
$$

The denominator is

$$
(1\times10^{-3})(1)=0.001
$$

So,

$$
r=\frac{0.03606}{0.001}
$$

$$
r=36.06\ \mathrm{m}
$$

Therefore,

$$
\boxed{r\approx 36.1\ \mathrm{m}}
$$

---

# 6. How will (r) change when (B) is doubled?

The radius is

$$
r=\frac{mv}{qB}
$$

Here, (m), (v), and (q) stay constant.

So,

$$
r\propto \frac{1}{B}
$$

This means the radius is inversely proportional to the magnetic field.

If (B) is doubled:

$$
B_{\text{new}}=2B
$$

Then

$$
r_{\text{new}}=\frac{mv}{q(2B)}
$$

$$
r_{\text{new}}=\frac{1}{2}\frac{mv}{qB}
$$

So,

$$
r_{\text{new}}=\frac{r}{2}
$$

Since

$$
r\approx 36.1\ \mathrm{m}
$$

we get

$$
r_{\text{new}}\approx \frac{36.1}{2}
$$

$$
r_{\text{new}}\approx 18.05\ \mathrm{m}
$$

Therefore,

$$
\boxed{r_{\text{new}}\approx 18.0\ \mathrm{m}}
$$

So if the magnetic field is doubled, the radius becomes two times smaller.

---

# Final answers for Problem 1

The Lorentz force is

$$
\boxed{\vec F=(0.003,-0.002,0)\ \mathrm{N}}
$$

or

$$
\boxed{\vec F=(3\times10^{-3},-2\times10^{-3},0)\ \mathrm{N}}
$$

The magnitude of the force is

$$
\boxed{|\vec F|\approx 3.61\times10^{-3}\ \mathrm{N}}
$$

The angular frequency is

$$
\boxed{\omega=0.1\ \mathrm{rad/s}}
$$

The velocity as a function of time is

$$
\boxed{
\vec v(t)=
(2\cos(0.1t)+3\sin(0.1t),\ 3\cos(0.1t)-2\sin(0.1t),\ 0)
}
$$

The position as a function of time is

$$
\boxed{
\vec r(t)=
\left(
20\sin(0.1t)+30[1-\cos(0.1t)],
\ 30\sin(0.1t)-20[1-\cos(0.1t)],
\ 0
\right)
}
$$

The magnetic force does no work:

$$
\boxed{W=0}
$$

The radius of the trajectory is

$$
\boxed{r\approx 36.1\ \mathrm{m}}
$$

If the magnetic field is doubled, the radius becomes half:

$$
\boxed{r_{\text{new}}\approx 18.0\ \mathrm{m}}
$$

So the particle moves in a circular path in the (xy)-plane, with constant speed and changing direction. ✅
