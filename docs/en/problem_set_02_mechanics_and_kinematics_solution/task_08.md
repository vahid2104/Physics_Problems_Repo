# Problem 8 – Relative motion

Given:

$$
\vec v_A=(3,1), \qquad \vec v_B=(1,-2)
$$

We need to determine:

* the relative velocity ( \vec v_{A/B} ),
* the direction of the relative motion,
* how the motion looks in:

  * the reference frame attached to the origin,
  * the reference frame attached to body A,
  * the reference frame attached to body B.

---

## 1. Relative velocity ( \vec v_{A/B} )

The velocity of A relative to B is defined by

$$
\vec v_{A/B}=\vec v_A-\vec v_B
$$

Substitute the given vectors:

$$
\vec v_{A/B}=(3,1)-(1,-2)
$$

Now subtract component by component:

$$
\vec v_{A/B}=(3-1,;1-(-2))
$$

$$
\vec v_{A/B}=(2,3)
$$

Therefore:

$$
\vec v_{A/B}=(2,3)
$$

---

## 2. Direction of the relative motion

The direction of the relative motion is the direction of the vector

$$
\vec v_{A/B}=(2,3)
$$

This means:

* in the (x)-direction, A moves (2) units faster than B,
* in the (y)-direction, A moves (3) units faster than B.

So the relative motion points:

* to the right,
* upward.

If we want the angle with the positive (x)-axis, we use

$$
\tan\theta=\frac{3}{2}
$$

Hence

$$
\theta=\arctan\left(\frac{3}{2}\right)
$$

Approximation:

$$
\theta \approx 56.3^\circ
$$

Therefore, the relative motion of A with respect to B is in the direction

$$
(2,3)
$$

or equivalently at an angle

$$
56.3^\circ
$$

above the positive (x)-axis.

---

## 3. Motion in the reference frame attached to the origin

In the fixed coordinate system, both bodies move with their given velocities.

### Body A

$$
\vec v_A=(3,1)
$$

So A moves:

* (3) units to the right per unit time,
* (1) unit upward per unit time.

Its trajectory is a straight line.

If A starts at the origin, then its position is

$$
\vec r_A(t)=(3t,t)
$$

---

### Body B

$$
\vec v_B=(1,-2)
$$

So B moves:

* (1) unit to the right per unit time,
* (2) units downward per unit time.

Its trajectory is also a straight line.

If B starts at the origin, then its position is

$$
\vec r_B(t)=(t,-2t)
$$

---

## 4. Motion in the reference frame attached to body A

In A’s frame, body A is at rest.

So:

$$
\vec v_{A/A}=(0,0)
$$

Body B moves relative to A with velocity

$$
\vec v_{B/A}=\vec v_B-\vec v_A
$$

Substitute:

$$
\vec v_{B/A}=(1,-2)-(3,1)
$$

$$
\vec v_{B/A}=(-2,-3)
$$

Therefore:

* A is stationary,
* B moves with velocity

$$
\vec v_{B/A}=(-2,-3)
$$

This means B moves:

* to the left,
* downward.

If B starts from the same point as A, then in A’s frame:

$$
\vec r_{B/A}(t)=(-2t,-3t)
$$

---

## 5. Motion in the reference frame attached to body B

In B’s frame, body B is at rest.

So:

$$
\vec v_{B/B}=(0,0)
$$

Body A moves relative to B with velocity

$$
\vec v_{A/B}=\vec v_A-\vec v_B
$$

We already computed this:

$$
\vec v_{A/B}=(2,3)
$$

Therefore:

* B is stationary,
* A moves with velocity

$$
\vec v_{A/B}=(2,3)
$$

This means A moves:

* to the right,
* upward.

If A starts from the same point as B, then in B’s frame:

$$
\vec r_{A/B}(t)=(2t,3t)
$$

---

## 6. Geometric interpretation

The important idea is:

* in the origin frame, both A and B move,
* in A’s frame, A is fixed and B moves with velocity ( (-2,-3) ),
* in B’s frame, B is fixed and A moves with velocity ( (2,3) ).

So the relative motion is simply described by the vector difference of velocities.

---

## 7. What should be shown in a graph or HTML animation

A good visualization should contain:

### In the origin frame

* vector ( \vec v_A=(3,1) ),
* vector ( \vec v_B=(1,-2) ),
* straight-line trajectories of A and B.

### In the frame of A

* A fixed at one point,
* B moving along a straight line with velocity ( (-2,-3) ).

### In the frame of B

* B fixed at one point,
* A moving along a straight line with velocity ( (2,3) ).

---

## Final answers for Problem 8

The relative velocity of A with respect to B is

$$
\vec v_{A/B}=(2,3)
$$

The direction of the relative motion is along the vector

$$
(2,3)
$$

with angle

$$
\theta=\arctan\left(\frac{3}{2}\right)\approx 56.3^\circ
$$

above the positive (x)-axis.

In the different reference frames:

### Origin frame

$$
\vec v_A=(3,1), \qquad \vec v_B=(1,-2)
$$

### Frame attached to A

$$
\vec v_{A/A}=(0,0), \qquad \vec v_{B/A}=(-2,-3)
$$

### Frame attached to B

$$
\vec v_{B/B}=(0,0), \qquad \vec v_{A/B}=(2,3)
$$

---

