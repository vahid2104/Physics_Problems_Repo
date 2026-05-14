# Problem 6 – Rod on metal rails in a magnetic field

We have a conducting rod sliding on two conducting rails.

The rails are separated by distance (L).

The rod moves along the rails with velocity (v).

A magnetic field (\vec B) is perpendicular to the plane of the rails.

Because the rod moves in the magnetic field, an induced EMF and current appear in the circuit.

This current creates a magnetic force which opposes the motion.

This is called **magnetic braking**.

---

## Given data

The mass of the rod is

[
m=0.20\ \mathrm{kg}
]

The distance between the rails is

[
L=0.30\ \mathrm{m}
]

The magnetic field is

[
B=0.80\ \mathrm{T}
]

The total resistance of the circuit is

[
R=0.50\ \Omega
]

The angle of the incline is

[
\alpha=25^\circ
]

The gravitational acceleration is

[
g=9.81\ \mathrm{m/s^2}
]

---

# 1. Motional EMF (\mathcal{E}(v)) and current (I(v))

When a rod of length (L) moves with velocity (v) perpendicular to a magnetic field (B), the motional EMF is

[
\mathcal{E}=BLv
]

Here:

[
B=0.80\ \mathrm{T}
]

[
L=0.30\ \mathrm{m}
]

So,

[
\mathcal{E}(v)=0.80\cdot 0.30\cdot v
]

[
\mathcal{E}(v)=0.24v
]

Therefore,

[
\boxed{\mathcal{E}(v)=0.24v\ \mathrm{V}}
]

---

The current is found using Ohm’s law:

[
I=\frac{\mathcal{E}}{R}
]

Substitute:

[
I(v)=\frac{BLv}{R}
]

Now put the values:

[
I(v)=\frac{0.24v}{0.50}
]

[
I(v)=0.48v
]

Therefore,

[
\boxed{I(v)=0.48v\ \mathrm{A}}
]

So if the rod moves faster, both the EMF and current become larger.

---

# 2. Magnetic braking force

The current-carrying rod is inside a magnetic field.

A current-carrying conductor in a magnetic field experiences a magnetic force:

[
F_B=ILB
]

Substitute the current:

[
I=\frac{BLv}{R}
]

So,

[
F_B=\left(\frac{BLv}{R}\right)LB
]

Multiply:

[
F_B=\frac{B^2L^2}{R}v
]

Therefore,

[
\boxed{F_B=\frac{B^2L^2}{R}v}
]

This force is opposite to the motion of the rod.

So we write it as a braking force:

[
\boxed{F_{\text{brake}}=-\frac{B^2L^2}{R}v}
]

The minus sign means the force acts against the velocity.

---

Now calculate the coefficient:

[
\frac{B^2L^2}{R}
================

\frac{(0.80)^2(0.30)^2}{0.50}
]

First:

[
(0.80)^2=0.64
]

[
(0.30)^2=0.09
]

So,

[
\frac{B^2L^2}{R}
================

\frac{0.64\cdot 0.09}{0.50}
]

[
\frac{B^2L^2}{R}
================

\frac{0.0576}{0.50}
]

[
\frac{B^2L^2}{R}=0.1152
]

Therefore,

[
\boxed{F_B=0.1152v\ \mathrm{N}}
]

and as a braking force:

[
\boxed{F_{\text{brake}}=-0.1152v\ \mathrm{N}}
]

---

# 3. Equation of motion along the incline

Along the incline, gravity pulls the rod downward.

The component of gravitational force along the incline is

[
F_g=mg\sin\alpha
]

The magnetic braking force acts upward, opposite to the motion:

[
F_B=\frac{B^2L^2}{R}v
]

Using Newton’s second law:

[
ma=F_{\text{net}}
]

Since

[
a=\frac{dv}{dt}
]

we write:

[
m\frac{dv}{dt}=mg\sin\alpha-\frac{B^2L^2}{R}v
]

Therefore,

[
\boxed{
m\frac{dv}{dt}=mg\sin\alpha-\frac{B^2L^2}{R}v
}
]

---

Now divide everything by (m):

[
\frac{dv}{dt}=g\sin\alpha-\frac{B^2L^2}{mR}v
]

This has the form:

[
\frac{dv}{dt}=a_0-\gamma v
]

where

[
a_0=g\sin\alpha
]

and

[
\gamma=\frac{B^2L^2}{mR}
]

This is motion with **damping proportional to velocity**.

---

Now calculate (a_0):

[
a_0=g\sin 25^\circ
]

[
a_0=9.81\cdot \sin 25^\circ
]

[
\sin 25^\circ\approx 0.4226
]

So,

[
a_0=9.81\cdot 0.4226
]

[
a_0\approx 4.145\ \mathrm{m/s^2}
]

Now calculate (\gamma):

[
\gamma=\frac{B^2L^2}{mR}
]

[
\gamma=\frac{(0.80)^2(0.30)^2}{(0.20)(0.50)}
]

[
\gamma=\frac{0.0576}{0.10}
]

[
\gamma=0.576\ \mathrm{s^{-1}}
]

So the equation becomes:

[
\boxed{
\frac{dv}{dt}=4.145-0.576v
}
]

This means:

* gravity tries to accelerate the rod,
* magnetic braking tries to slow it down,
* the braking becomes stronger when (v) becomes larger.

---

# 4. Terminal velocity (v_\infty)

Terminal velocity means the rod stops accelerating.

So,

[
\frac{dv}{dt}=0
]

From the equation:

[
\frac{dv}{dt}=g\sin\alpha-\frac{B^2L^2}{mR}v
]

At terminal velocity:

[
0=g\sin\alpha-\frac{B^2L^2}{mR}v_\infty
]

Move the second term:

[
\frac{B^2L^2}{mR}v_\infty=g\sin\alpha
]

Solve for (v_\infty):

[
v_\infty=\frac{mgR\sin\alpha}{B^2L^2}
]

Therefore,

[
\boxed{
v_\infty=\frac{mgR\sin\alpha}{B^2L^2}
}
]

---

Now substitute the values:

[
v_\infty=
\frac{(0.20)(9.81)(0.50)\sin 25^\circ}{(0.80)^2(0.30)^2}
]

First calculate the numerator:

[
(0.20)(9.81)=1.962
]

[
1.962\cdot 0.50=0.981
]

[
0.981\cdot \sin 25^\circ=0.981\cdot 0.4226
]

[
0.981\cdot 0.4226\approx 0.4145
]

Now calculate the denominator:

[
(0.80)^2(0.30)^2=0.64\cdot 0.09
]

[
0.64\cdot 0.09=0.0576
]

So,

[
v_\infty=\frac{0.4145}{0.0576}
]

[
v_\infty\approx 7.20\ \mathrm{m/s}
]

Therefore,

[
\boxed{v_\infty\approx 7.20\ \mathrm{m/s}}
]

---

## Current at terminal velocity

We already found:

[
I(v)=0.48v
]

At terminal velocity:

[
I_\infty=0.48\cdot 7.20
]

[
I_\infty\approx 3.46\ \mathrm{A}
]

So,

[
\boxed{I_\infty\approx 3.46\ \mathrm{A}}
]

---

## EMF at terminal velocity

We also found:

[
\mathcal{E}(v)=0.24v
]

At terminal velocity:

[
\mathcal{E}_\infty=0.24\cdot 7.20
]

[
\mathcal{E}_\infty\approx 1.73\ \mathrm{V}
]

Therefore,

[
\boxed{\mathcal{E}_\infty\approx 1.73\ \mathrm{V}}
]

---

# 5. Power balance

The gravitational force along the incline is

[
F_g=mg\sin\alpha
]

Power is force times velocity:

[
P=Fv
]

So the gravitational power is

[
P_g=mg\sin\alpha\cdot v
]

The electrical power converted into heat is Joule heating:

[
P_J=I^2R
]

We need to show that in steady state:

[
mg\sin\alpha\cdot v=I^2R
]

---

From the current formula:

[
I=\frac{BLv}{R}
]

So,

[
I^2R=\left(\frac{BLv}{R}\right)^2R
]

[
I^2R=\frac{B^2L^2v^2}{R^2}R
]

Cancel one (R):

[
I^2R=\frac{B^2L^2}{R}v^2
]

Now look at the magnetic braking force:

[
F_B=\frac{B^2L^2}{R}v
]

The power removed by the magnetic braking force is

[
P_B=F_Bv
]

[
P_B=\left(\frac{B^2L^2}{R}v\right)v
]

[
P_B=\frac{B^2L^2}{R}v^2
]

So,

[
P_B=I^2R
]

This means the mechanical energy lost because of magnetic braking becomes heat in the resistor.

---

At steady state, the velocity is constant.

So acceleration is zero:

[
\frac{dv}{dt}=0
]

That means forces are balanced:

[
mg\sin\alpha=F_B
]

Multiply both sides by (v):

[
mg\sin\alpha\cdot v=F_Bv
]

But we showed that

[
F_Bv=I^2R
]

Therefore,

[
\boxed{
mg\sin\alpha\cdot v=I^2R
}
]

So in steady motion:

[
\boxed{\text{gravitational power}=\text{Joule heat power}}
]

The gravitational potential energy is converted into electrical energy and then into heat.

---

## Numerical check at terminal velocity

At terminal velocity:

[
v_\infty\approx 7.20\ \mathrm{m/s}
]

The gravitational force along the incline is

[
mg\sin\alpha=(0.20)(9.81)\sin 25^\circ
]

[
mg\sin\alpha=1.962\cdot 0.4226
]

[
mg\sin\alpha\approx 0.829\ \mathrm{N}
]

So gravitational power is

[
P_g=mg\sin\alpha\cdot v_\infty
]

[
P_g=0.829\cdot 7.20
]

[
P_g\approx 5.97\ \mathrm{W}
]

Now Joule power:

[
I_\infty\approx 3.46\ \mathrm{A}
]

[
P_J=I_\infty^2R
]

[
P_J=(3.46)^2(0.50)
]

[
P_J\approx 5.99\ \mathrm{W}
]

Small difference is only because of rounding.

Therefore,

[
\boxed{P_g\approx P_J\approx 6.0\ \mathrm{W}}
]

---

# Physical interpretation

At the beginning, the rod starts moving down the incline because of gravity.

As it moves, it cuts magnetic field lines.

Because of this, an EMF is induced:

[
\mathcal{E}=BLv
]

This EMF creates current:

[
I=\frac{BLv}{R}
]

The current in the magnetic field creates a force opposite to the motion:

[
F_B=\frac{B^2L^2}{R}v
]

As the rod becomes faster, the braking force becomes stronger.

Eventually:

[
mg\sin\alpha=F_B
]

At this moment, acceleration becomes zero and the rod moves with constant terminal velocity.

---

# Final answers for Problem 6

The motional EMF is

[
\boxed{\mathcal{E}(v)=BLv}
]

For the given values:

[
\boxed{\mathcal{E}(v)=0.24v\ \mathrm{V}}
]

The current is

[
\boxed{I(v)=\frac{BLv}{R}}
]

For the given values:

[
\boxed{I(v)=0.48v\ \mathrm{A}}
]

The magnetic braking force is

[
\boxed{F_B=\frac{B^2L^2}{R}v}
]

For the given values:

[
\boxed{F_B=0.1152v\ \mathrm{N}}
]

The equation of motion is

[
\boxed{
m\frac{dv}{dt}=mg\sin\alpha-\frac{B^2L^2}{R}v
}
]

or

[
\boxed{
\frac{dv}{dt}=g\sin\alpha-\frac{B^2L^2}{mR}v
}
]

For the given values:

[
\boxed{
\frac{dv}{dt}=4.145-0.576v
}
]

The terminal velocity is

[
\boxed{
v_\infty=\frac{mgR\sin\alpha}{B^2L^2}
}
]

Numerically:

[
\boxed{
v_\infty\approx 7.20\ \mathrm{m/s}
}
]

At terminal velocity:

[
\boxed{
\mathcal{E}_\infty\approx 1.73\ \mathrm{V}
}
]

[
\boxed{
I_\infty\approx 3.46\ \mathrm{A}
}
]

In steady state, the power balance is

[
\boxed{
mg\sin\alpha\cdot v=I^2R
}
]

So gravitational energy is converted into Joule heat in the circuit. ✅
