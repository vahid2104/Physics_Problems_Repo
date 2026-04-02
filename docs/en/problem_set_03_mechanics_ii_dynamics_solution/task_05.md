Sure 🙂 Here is **Problem 5** written in the same simple, step-by-step style.

---

# Problem 5 – Momentum and one-dimensional head-on collision

Two bodies with masses (m_1) and (m_2) move along the same straight line. The collision is **elastic**.

We want to determine:

* the conservation laws,
* the velocities after the collision,
* the special case (m_1=m_2),
* the limit (m_2\gg m_1),
* the physical interpretation.

---

## 1. Conservation of momentum

In a one-dimensional collision, the total momentum before and after the collision is the same.

If the velocities before collision are (u_1) and (u_2), and the velocities after collision are (v_1) and (v_2), then

$$
m_1 u_1 + m_2 u_2 = m_1 v_1 + m_2 v_2
$$

This is the **conservation of momentum**.

---

## 2. Conservation of kinetic energy

Because the collision is **elastic**, the total kinetic energy is also conserved.

So we have

$$
\frac12 m_1 u_1^2 + \frac12 m_2 u_2^2
=====================================

\frac12 m_1 v_1^2 + \frac12 m_2 v_2^2
$$

We can multiply both sides by (2) to simplify:

$$
m_1 u_1^2 + m_2 u_2^2 = m_1 v_1^2 + m_2 v_2^2
$$

This is the **conservation of kinetic energy**.

---

## 3. Determine the velocities after the collision

We now solve the two equations:

### Momentum equation

$$
m_1 u_1 + m_2 u_2 = m_1 v_1 + m_2 v_2
$$

### Energy equation

$$
m_1 u_1^2 + m_2 u_2^2 = m_1 v_1^2 + m_2 v_2^2
$$

---

## 4. Useful relation for an elastic collision

For a one-dimensional elastic collision, the relative speed of separation equals the relative speed of approach.

So

$$
u_1-u_2 = -(v_1-v_2)
$$

which can also be written as

$$
u_1-u_2 = v_2-v_1
$$

This relation is very useful.

---

## 5. Solve together with momentum conservation

We now use the two equations:

$$
m_1 u_1 + m_2 u_2 = m_1 v_1 + m_2 v_2
$$

and

$$
u_1-u_2 = v_2-v_1
$$

From the second equation:

$$
v_2 = v_1 + u_1 - u_2
$$

Substitute this into the momentum equation:

$$
m_1 u_1 + m_2 u_2 = m_1 v_1 + m_2(v_1+u_1-u_2)
$$

Expand:

$$
m_1 u_1 + m_2 u_2 = (m_1+m_2)v_1 + m_2 u_1 - m_2 u_2
$$

Move terms to the left:

$$
m_1 u_1 - m_2 u_1 + m_2 u_2 + m_2 u_2 = (m_1+m_2)v_1
$$

$$
(m_1-m_2)u_1 + 2m_2 u_2 = (m_1+m_2)v_1
$$

Therefore,

$$
v_1=\frac{m_1-m_2}{m_1+m_2}u_1+\frac{2m_2}{m_1+m_2}u_2
$$

Now use

$$
v_2=v_1+u_1-u_2
$$

Substitute (v_1):

$$
v_2=\frac{m_1-m_2}{m_1+m_2}u_1+\frac{2m_2}{m_1+m_2}u_2+u_1-u_2
$$

Put everything over the common denominator (m_1+m_2):

$$
v_2=
\frac{(m_1-m_2)u_1+2m_2u_2+(m_1+m_2)u_1-(m_1+m_2)u_2}{m_1+m_2}
$$

Simplify the numerator:

For (u_1):

$$
(m_1-m_2)+(m_1+m_2)=2m_1
$$

For (u_2):

$$
2m_2-(m_1+m_2)=m_2-m_1
$$

So

$$
v_2=\frac{2m_1}{m_1+m_2}u_1+\frac{m_2-m_1}{m_1+m_2}u_2
$$

---

## 6. Velocities after the collision

Therefore, the final velocities are

$$
v_1=\frac{m_1-m_2}{m_1+m_2}u_1+\frac{2m_2}{m_1+m_2}u_2
$$

$$
v_2=\frac{2m_1}{m_1+m_2}u_1+\frac{m_2-m_1}{m_1+m_2}u_2
$$

These are the standard formulas for a one-dimensional elastic collision.

---

## 7. Special case: (m_1=m_2)

Now let

$$
m_1=m_2=m
$$

Substitute into the formulas.

### For (v_1):

$$
v_1=\frac{m-m}{m+m}u_1+\frac{2m}{m+m}u_2
$$

$$
v_1=0\cdot u_1+1\cdot u_2
$$

$$
v_1=u_2
$$

### For (v_2):

$$
v_2=\frac{2m}{m+m}u_1+\frac{m-m}{m+m}u_2
$$

$$
v_2=1\cdot u_1+0\cdot u_2
$$

$$
v_2=u_1
$$

Therefore, when the masses are equal, the two bodies **exchange velocities**.

---

## 8. Interpretation for equal masses

So if two equal masses collide elastically in one dimension:

* body 1 leaves with the initial velocity of body 2,
* body 2 leaves with the initial velocity of body 1.

This is exactly what happens in an ideal collision of billiard balls.

### Example

If body 2 is initially at rest, so that

$$
u_2=0
$$

then

$$
v_1=0,\qquad v_2=u_1
$$

So the first body stops, and the second body moves away with the original velocity of the first body.

---

## 9. Limit case: (m_2\gg m_1)

Now consider the case where the second mass is much larger than the first one:

$$
m_2\gg m_1
$$

We examine the formulas approximately.

---

### Velocity of body 1

We have

$$
v_1=\frac{m_1-m_2}{m_1+m_2}u_1+\frac{2m_2}{m_1+m_2}u_2
$$

If (m_2) is much larger than (m_1), then

$$
m_1+m_2 \approx m_2
$$

and

$$
m_1-m_2 \approx -m_2
$$

So

$$
\frac{m_1-m_2}{m_1+m_2}\approx -1
]

and

$$
\frac{2m_2}{m_1+m_2}\approx 2
$$

Thus

$$
v_1 \approx -u_1 + 2u_2
$$

---

### Velocity of body 2

Now

$$
v_2=\frac{2m_1}{m_1+m_2}u_1+\frac{m_2-m_1}{m_1+m_2}u_2
$$

If (m_2\gg m_1), then

$$
\frac{2m_1}{m_1+m_2}\approx 0
$$

and

$$
\frac{m_2-m_1}{m_1+m_2}\approx 1
$$

So

$$
v_2\approx u_2
$$

Therefore, the heavy body keeps almost the same velocity.

---

## 10. Interpretation for (m_2\gg m_1)

So in this limit:

$$
v_1 \approx 2u_2-u_1
$$

$$
v_2 \approx u_2
$$

This means:

* the heavy body is almost unaffected by the collision,
* the light body changes its velocity strongly.

---

### Important subcase: heavy body initially at rest

If the heavy body is initially at rest, then

$$
u_2=0
$$

So

$$
v_1\approx -u_1
$$

$$
v_2\approx 0
$$

This means the light body bounces back with almost the same speed, while the heavy body remains almost at rest.

This is like a small ball hitting a rigid wall.

---

## 11. Physical meaning of the results

Let us summarize the physical meaning.

### Elastic collision

In an elastic collision:

* total momentum is conserved,
* total kinetic energy is conserved.

That is why the bodies rebound without losing kinetic energy.

---

### Equal masses

When

$$
m_1=m_2
$$

the bodies exchange velocities.

This is a very symmetric situation.

---

### One mass much larger than the other

When

$$
m_2\gg m_1
$$

the heavy body behaves almost like an immovable object.

The light body reflects back, almost as if it hit a wall.

---

## Final answers for Problem 5

### Conservation of momentum

$$
m_1 u_1 + m_2 u_2 = m_1 v_1 + m_2 v_2
$$

### Conservation of kinetic energy

$$
\frac12 m_1 u_1^2 + \frac12 m_2 u_2^2
=====================================

\frac12 m_1 v_1^2 + \frac12 m_2 v_2^2
$$

### Velocities after the collision

$$
v_1=\frac{m_1-m_2}{m_1+m_2}u_1+\frac{2m_2}{m_1+m_2}u_2
$$

$$
v_2=\frac{2m_1}{m_1+m_2}u_1+\frac{m_2-m_1}{m_1+m_2}u_2
$$

### Case (m_1=m_2)

$$
v_1=u_2,\qquad v_2=u_1
$$

So the bodies exchange velocities.

### Limit (m_2\gg m_1)

$$
v_1\approx 2u_2-u_1,\qquad v_2\approx u_2
$$

If additionally (u_2=0), then

$$
v_1\approx -u_1,\qquad v_2\approx 0
$$

So the light body bounces back, and the heavy body remains almost unchanged.

---

If you want, I can also make this into a **shorter “clean notebook solution” version** without so many words, just like a final homework write-up.
