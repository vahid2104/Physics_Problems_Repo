# Problem 4 – Motion of a particle in a uniform field

We are given a charged particle moving in a uniform electric field.

The data are:

$$
m=0.02\ \mathrm{kg}
$$

$$
q=1\ \mathrm{mC}
$$

$$
\vec E=(30,100)\ \mathrm{N/C}
$$

$$
\vec v(0)=(20,0)\ \mathrm{m/s}
$$

$$
\vec r(0)=(0,0)
$$

We need to:

* write and solve the equations of motion,
* draw the trajectory,
* calculate the time when the vertical velocity becomes (50\ \mathrm{m/s}),
* calculate the kinetic energy after (t=0.05\ \mathrm{s}),
* check the energy balance.

---

## Given data

The mass is

$$
m=0.02\ \mathrm{kg}
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

The electric field is

$$
\vec E=(30,100)\ \mathrm{N/C}
$$

This means

$$
E_x=30\ \mathrm{N/C}
$$

and

$$
E_y=100\ \mathrm{N/C}
$$

The initial velocity is

$$
\vec v(0)=(20,0)\ \mathrm{m/s}
$$

So

$$
v_x(0)=20\ \mathrm{m/s}
$$

and

$$
v_y(0)=0\ \mathrm{m/s}
$$

The initial position is

$$
\vec r(0)=(0,0)
$$

So

$$
x(0)=0
$$

and

$$
y(0)=0
$$

---

# 1. Equations of motion and analytical solution

The electric force on a charge in an electric field is

$$
\vec F=q\vec E
$$

Substitute the values:

$$
\vec F=(1\times 10^{-3})(30,100)
$$

So

$$
\vec F=(0.03,0.10)\ \mathrm{N}
$$

Using Newton’s second law,

$$
\vec F=m\vec a
$$

so

$$
\vec a=\frac{\vec F}{m}
$$

Substitute:

$$
\vec a=\frac{(0.03,0.10)}{0.02}
$$

Calculate each component:

$$
a_x=\frac{0.03}{0.02}=1.5\ \mathrm{m/s^2}
$$

$$
a_y=\frac{0.10}{0.02}=5\ \mathrm{m/s^2}
$$

Therefore,

$$
\vec a=(1.5,5)\ \mathrm{m/s^2}
$$

Because the electric field is uniform, the acceleration is constant.

---

## Velocity as a function of time

For constant acceleration,

$$
v_x(t)=v_x(0)+a_xt
$$

Substitute the values:

$$
v_x(t)=20+1.5t
$$

So

$$
\boxed{v_x(t)=20+1.5t}
$$

For the vertical velocity,

$$
v_y(t)=v_y(0)+a_yt
$$

Substitute:

$$
v_y(t)=0+5t
$$

So

$$
\boxed{v_y(t)=5t}
$$

Therefore, the velocity vector is

$$
\boxed{\vec v(t)=(20+1.5t,\ 5t)}
$$

---

## Position as a function of time

For constant acceleration,

$$
x(t)=x(0)+v_x(0)t+\frac{1}{2}a_xt^2
$$

Substitute:

$$
x(t)=0+20t+\frac{1}{2}(1.5)t^2
$$

Since

$$
\frac{1}{2}(1.5)=0.75
$$

we get

$$
\boxed{x(t)=20t+0.75t^2}
$$

For the vertical position,

$$
y(t)=y(0)+v_y(0)t+\frac{1}{2}a_yt^2
$$

Substitute:

$$
y(t)=0+0t+\frac{1}{2}(5)t^2
$$

Since

$$
\frac{1}{2}(5)=2.5
$$

we get

$$
\boxed{y(t)=2.5t^2}
$$

Therefore, the position vector is

$$
\boxed{\vec r(t)=(20t+0.75t^2,\ 2.5t^2)}
$$

---

# 2. Motion trajectory

The trajectory is the path of the particle in the (x-y) plane.

We found:

$$
x(t)=20t+0.75t^2
$$

and

$$
y(t)=2.5t^2
$$

The particle starts at

$$
(0,0)
$$

It initially moves mostly in the positive (x)-direction because

$$
v_x(0)=20\ \mathrm{m/s}
$$

and

$$
v_y(0)=0
$$

But the electric field has a positive (y)-component, so the particle accelerates upward.

It also has a positive (x)-acceleration, so it speeds up slightly in the (x)-direction too.

The trajectory bends upward like this:

```text
y
↑
|
|                         *
|                    *
|               *
|          *
|      *
|   *
| *
|________________________________→ x
```

So the particle follows a curved path upward and to the right.

---

## Some points on the trajectory

Using

$$
x(t)=20t+0.75t^2
$$

and

$$
y(t)=2.5t^2
$$

we can calculate a few points.

At

$$
t=0
$$

$$
x=0,\qquad y=0
$$

At

$$
t=1\ \mathrm{s}
$$

$$
x=20(1)+0.75(1)^2
$$

$$
x=20.75\ \mathrm{m}
$$

$$
y=2.5(1)^2
$$

$$
y=2.5\ \mathrm{m}
$$

At

$$
t=2\ \mathrm{s}
$$

$$
x=20(2)+0.75(2)^2
$$

$$
x=40+3
$$

$$
x=43\ \mathrm{m}
$$

$$
y=2.5(2)^2
$$

$$
y=10\ \mathrm{m}
$$

At

$$
t=3\ \mathrm{s}
$$

$$
x=20(3)+0.75(3)^2
$$

$$
x=60+6.75
$$

$$
x=66.75\ \mathrm{m}
$$

$$
y=2.5(3)^2
$$

$$
y=22.5\ \mathrm{m}
$$

So the path goes through approximately:

$$
(0,0)
$$

$$
(20.75,2.5)
$$

$$
(43,10)
$$

$$
(66.75,22.5)
$$

---

# 3. Time to reach a vertical velocity of (50\ \mathrm{m/s})

We already found the vertical velocity:

$$
v_y(t)=5t
$$

We want the time when

$$
v_y=50\ \mathrm{m/s}
$$

So

$$
50=5t
$$

Divide both sides by (5):

$$
t=\frac{50}{5}
$$

$$
t=10\ \mathrm{s}
$$

Therefore,

$$
\boxed{t=10\ \mathrm{s}}
$$

The particle reaches a vertical velocity of (50\ \mathrm{m/s}) after

$$
10\ \mathrm{s}
$$

---

# 4. Kinetic energy after (t=0.05\ \mathrm{s})

The kinetic energy is

$$
K=\frac{1}{2}mv^2
$$

where

$$
v^2=v_x^2+v_y^2
$$

First calculate the velocity components at

$$
t=0.05\ \mathrm{s}
$$

We have

$$
v_x(t)=20+1.5t
$$

Substitute:

$$
v_x(0.05)=20+1.5(0.05)
$$

$$
v_x(0.05)=20+0.075
$$

$$
v_x(0.05)=20.075\ \mathrm{m/s}
$$

Now for the vertical velocity:

$$
v_y(t)=5t
$$

Substitute:

$$
v_y(0.05)=5(0.05)
$$

$$
v_y(0.05)=0.25\ \mathrm{m/s}
$$

So after (0.05\ \mathrm{s}),

$$
\vec v(0.05)=(20.075,\ 0.25)\ \mathrm{m/s}
$$

Now calculate (v^2):

$$
v^2=(20.075)^2+(0.25)^2
$$

Calculate each part:

$$
(20.075)^2=403.005625
$$

$$
(0.25)^2=0.0625
$$

So

$$
v^2=403.005625+0.0625
$$

$$
v^2=403.068125
$$

Now calculate kinetic energy:

$$
K=\frac{1}{2}(0.02)(403.068125)
$$

Since

$$
\frac{1}{2}(0.02)=0.01
$$

we get

$$
K=0.01(403.068125)
$$

$$
K=4.03068125\ \mathrm{J}
$$

Therefore,

$$
\boxed{K(0.05)\approx 4.03\ \mathrm{J}}
$$

---

# 5. Check consistency with the energy balance

The work-energy theorem says:

$$
\Delta K=W
$$

This means the change in kinetic energy should equal the work done by the electric field.

The work done by a uniform electric field is

$$
W=q\vec E\cdot \Delta \vec r
$$

Since the particle starts from the origin,

$$
\Delta \vec r=\vec r(t)
$$

At

$$
t=0.05\ \mathrm{s}
$$

we calculate the position.

We have

$$
x(t)=20t+0.75t^2
$$

Substitute:

$$
x(0.05)=20(0.05)+0.75(0.05)^2
$$

First,

$$
20(0.05)=1
$$

and

$$
(0.05)^2=0.0025
$$

So

$$
0.75(0.0025)=0.001875
$$

Therefore,

$$
x(0.05)=1+0.001875
$$

$$
x(0.05)=1.001875\ \mathrm{m}
$$

Now calculate (y):

$$
y(t)=2.5t^2
$$

Substitute:

$$
y(0.05)=2.5(0.05)^2
$$

$$
y(0.05)=2.5(0.0025)
$$

$$
y(0.05)=0.00625\ \mathrm{m}
$$

So

$$
\vec r(0.05)=(1.001875,\ 0.00625)\ \mathrm{m}
$$

Now calculate the work done by the electric field:

$$
W=q\vec E\cdot \vec r
$$

The dot product is

$$
\vec E\cdot \vec r=E_xx+E_yy
$$

So

$$
\vec E\cdot \vec r=30(1.001875)+100(0.00625)
$$

Calculate each part:

$$
30(1.001875)=30.05625
$$

and

$$
100(0.00625)=0.625
$$

So

$$
\vec E\cdot \vec r=30.05625+0.625
$$

$$
\vec E\cdot \vec r=30.68125
$$

Now multiply by the charge:

$$
W=(1\times 10^{-3})(30.68125)
$$

$$
W=0.03068125\ \mathrm{J}
$$

Therefore,

$$
\boxed{W=0.03068125\ \mathrm{J}}
$$

---

## Change in kinetic energy

The initial kinetic energy is

$$
K(0)=\frac{1}{2}mv_0^2
$$

Initially,

$$
v_0=20\ \mathrm{m/s}
$$

So

$$
K(0)=\frac{1}{2}(0.02)(20)^2
$$

Since

$$
20^2=400
$$

we get

$$
K(0)=0.01(400)
$$

$$
K(0)=4.00\ \mathrm{J}
$$

We already found

$$
K(0.05)=4.03068125\ \mathrm{J}
$$

So the change in kinetic energy is

$$
\Delta K=K(0.05)-K(0)
$$

$$
\Delta K=4.03068125-4.00
$$

$$
\Delta K=0.03068125\ \mathrm{J}
$$

Therefore,

$$
\boxed{\Delta K=0.03068125\ \mathrm{J}}
$$

This is exactly equal to the work done by the electric field:

$$
\Delta K=W
$$

$$
0.03068125=0.03068125
$$

So the energy balance is correct. ✅

---

# Final answers for Problem 4

The electric force is

$$
\vec F=q\vec E=(0.03,0.10)\ \mathrm{N}
$$

The acceleration is

$$
\vec a=(1.5,5)\ \mathrm{m/s^2}
$$

The velocity is

$$
\boxed{\vec v(t)=(20+1.5t,\ 5t)}
$$

The position is

$$
\boxed{\vec r(t)=(20t+0.75t^2,\ 2.5t^2)}
$$

The trajectory bends upward and to the right.

The time to reach

$$
v_y=50\ \mathrm{m/s}
$$

is

$$
\boxed{t=10\ \mathrm{s}}
$$

The kinetic energy after

$$
t=0.05\ \mathrm{s}
$$

is

$$
\boxed{K(0.05)\approx 4.03\ \mathrm{J}}
$$

The work done by the electric field after

$$
t=0.05\ \mathrm{s}
$$

is

$$
\boxed{W=0.03068125\ \mathrm{J}}
$$

The change in kinetic energy is

$$
\boxed{\Delta K=0.03068125\ \mathrm{J}}
$$

Therefore,

$$
\boxed{\Delta K=W}
$$

So the result is consistent with the energy balance. ✅
