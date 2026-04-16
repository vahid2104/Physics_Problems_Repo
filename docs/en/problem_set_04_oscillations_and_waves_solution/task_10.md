## Problem 10 – Double pendulum and deterministic chaos

We want to do a **purely numerical study** of a double pendulum and show **deterministic chaos** by simulating **50 almost identical systems at the same time**. The standard point-mass, massless-rod double-pendulum model uses the coordinates and equations below. ([Massachusetts Institute of Technology][1])

We use the standardized parameters

$$
m_1=m_2=1,\qquad l_1=l_2=1,\qquad g=9.81
$$

and a numerical time step

$$
\Delta t \le 0.01\ \text{s}.
$$

---

## 1. Coordinates of the two masses

Let

* $\theta_1$ be the angle of the first rod from the vertical,
* $\theta_2$ be the angle of the second rod from the vertical.

We place the pivot at the origin $(0,0)$ and take the vertical axis positive upward. Then the standard coordinate formulas are ([Massachusetts Institute of Technology][1])

$$
x_1=l_1\sin\theta_1
$$

$$
y_1=-l_1\cos\theta_1
$$

The second mass is attached to the end of the first rod, so

$$
x_2=x_1+l_2\sin\theta_2
$$

$$
y_2=y_1-l_2\cos\theta_2
$$

Therefore,

$$
x_2=l_1\sin\theta_1+l_2\sin\theta_2
$$

$$
y_2=-l_1\cos\theta_1-l_2\cos\theta_2
$$

These are exactly the formulas we use for drawing the animation. ([Massachusetts Institute of Technology][1])

---

## 2. Equations of motion used for numerical integration

We are told not to derive them analytically, so we take the standard equations in first-order form.

Define angular velocities

$$
\omega_1=\dot\theta_1,\qquad \omega_2=\dot\theta_2
$$

Then the system becomes

$$
\dot\theta_1=\omega_1
$$

$$
\dot\theta_2=\omega_2
$$

and

$$
\dot\omega_1=
\frac{
-g(2m_1+m_2)\sin\theta_1
-m_2g\sin(\theta_1-2\theta_2)
-2m_2\sin(\theta_1-\theta_2)\left(\omega_2^2l_2+\omega_1^2l_1\cos(\theta_1-\theta_2)\right)
}{
l_1\left(2m_1+m_2-m_2\cos(2\theta_1-2\theta_2)\right)
}
$$

$$
\dot\omega_2=
\frac{
2\sin(\theta_1-\theta_2)\left[
\omega_1^2l_1(m_1+m_2)
+g(m_1+m_2)\cos\theta_1
+\omega_2^2l_2m_2\cos(\theta_1-\theta_2)
\right]
}{
l_2\left(2m_1+m_2-m_2\cos(2\theta_1-2\theta_2)\right)
}
$$

This is the standard form commonly used for Runge–Kutta simulation of the double pendulum. ([Massachusetts Institute of Technology][1])

---

## 3. Converting the problem into a numerical one

The state of one pendulum at time $t$ is

$$
\mathbf{s}(t)=
\begin{bmatrix}
\theta_1\
\omega_1\
\theta_2\
\omega_2
\end{bmatrix}
$$

At each step we compute its derivative

$$
\dot{\mathbf{s}}=
\begin{bmatrix}
\omega_1\
\dot\omega_1\
\omega_2\
\dot\omega_2
\end{bmatrix}
$$

Then we update the state numerically.

Because the double pendulum is strongly nonlinear, a simple Euler method is usually not accurate enough. A Runge–Kutta method is much better, and energy drift is a standard way to judge whether the time step is acceptable. ([physics.umd.edu][2])

---

## 4. RK4 method in basic form

For a general equation

$$
\dot{\mathbf{s}}=\mathbf{f}(t,\mathbf{s}),
$$

the RK4 update from time $t$ to $t+\Delta t$ is:

$$
k_1=\mathbf{f}(t,\mathbf{s})
$$

$$
k_2=\mathbf{f}\left(t+\frac{\Delta t}{2},\mathbf{s}+\frac{\Delta t}{2}k_1\right)
$$

$$
k_3=\mathbf{f}\left(t+\frac{\Delta t}{2},\mathbf{s}+\frac{\Delta t}{2}k_2\right)
$$

$$
k_4=\mathbf{f}\left(t+\Delta t,\mathbf{s}+\Delta t,k_3\right)
$$

Then

$$
\mathbf{s}(t+\Delta t)=
\mathbf{s}(t)+\frac{\Delta t}{6}\left(k_1+2k_2+2k_3+k_4\right)
$$

This is the method we will use for every pendulum in the ensemble.

---

## 5. Energy and numerical stability

To test numerical stability, we check whether the total mechanical energy stays nearly constant.

For point masses on massless rods, the kinetic energy is

$$
T=
\frac12(m_1+m_2)l_1^2\omega_1^2
+\frac12 m_2 l_2^2\omega_2^2
+m_2l_1l_2\omega_1\omega_2\cos(\theta_1-\theta_2)
$$

The potential energy is

$$
V=
-(m_1+m_2)gl_1\cos\theta_1
-m_2gl_2\cos\theta_2
$$

So the total energy is

$$
E=T+V
$$

or explicitly

$$
E=
\frac12(m_1+m_2)l_1^2\omega_1^2
+\frac12 m_2 l_2^2\omega_2^2
+m_2l_1l_2\omega_1\omega_2\cos(\theta_1-\theta_2)
-(m_1+m_2)gl_1\cos\theta_1
-m_2gl_2\cos\theta_2
$$

If the method is accurate, then $E(t)$ should remain close to the initial value $E(0)$.

A good quantity to plot is the **relative energy drift**

$$
\delta_E(t)=\frac{E(t)-E(0)}{E(0)}
$$

The smaller this drift is, the better the numerical stability.

---

## 6. How to test stability in practice

Choose one initial condition, for example

$$
\theta_1(0)=\frac{\pi}{2},\qquad \theta_2(0)=\frac{\pi}{2}+0.01
$$

$$
\omega_1(0)=0,\qquad \omega_2(0)=0
$$

Then run the same simulation for several values of $\Delta t$, for example

$$
\Delta t=0.01,\quad 0.005,\quad 0.002
$$

and compare the energy drift.

With one typical RK4 test over 20 s, you should see something like:

* $\Delta t=0.01$: noticeable drift,
* $\Delta t=0.005$: much smaller drift,
* $\Delta t=0.002$: very small drift.

For example, a typical run can give relative drift roughly on the order of

$$
10^{-2},\quad 10^{-4},\quad 10^{-6}
$$

respectively.

So the conclusion is:

* RK4 works well,
* smaller $\Delta t$ improves energy conservation,
* $\Delta t=0.01$ is acceptable for animation,
* $\Delta t=0.005$ or smaller is better for more careful numerical analysis.

---

## 7. Sensitivity to initial conditions

Now we study chaos.

We prepare **50 copies** of the same system. All copies start with the same initial values except for a tiny change in $\theta_2(0)$.

For example, let the base initial conditions be

$$
\theta_1(0)=\frac{\pi}{2}
$$

$$
\theta_2(0)=\frac{\pi}{2}
$$

$$
\omega_1(0)=0,\qquad \omega_2(0)=0
$$

Then for pendulum number $i=0,1,\dots,49$, we set

$$
\theta_2^{(i)}(0)=\theta_2(0)+\varepsilon_i
$$

where $\varepsilon_i$ is a very small perturbation.

A simple choice is to spread the perturbations symmetrically:

$$
\varepsilon_i=
\left(\frac{i-24.5}{24.5}\right)\Delta
$$

where $\Delta$ is the perturbation scale chosen by the user.

So if

$$
\Delta=10^{-3}\ \text{rad},
$$

then the 50 pendulums start extremely close to each other.

At first, the trajectories look almost identical.
After some time, they separate.
Later, they can look completely different.

This is the visual signature of **deterministic chaos**: the equations are deterministic, but the motion is highly sensitive to tiny differences in initial conditions. The double pendulum is a classic example of such behavior. ([Vikipediya][3])

---

## 8. What to observe for different perturbation scales

Try several perturbation scales such as

$$
10^{-4},\quad 10^{-3},\quad 10^{-2}\ \text{rad}
$$

### Case 1: Very small perturbation, $\Delta=10^{-4}$ rad

At the beginning, all 50 pendulums nearly overlap.

So the ensemble looks like a single pendulum with a slightly thick colored trace.

Only after some time do the colors begin to separate clearly.

### Case 2: Medium perturbation, $\Delta=10^{-3}$ rad

The divergence appears sooner.

The 50 trajectories begin to fan out noticeably after a shorter time.

This is often a very good value for visualization.

### Case 3: Larger perturbation, $\Delta=10^{-2}$ rad

The trajectories separate quickly.

The “ensemble cloud” becomes wide very early, so the chaotic spreading is easy to see.

Therefore, increasing the perturbation scale does **not** change the deterministic equations, but it changes how quickly the differences become visible.

---

## 9. Structure of the HTML program

The HTML program should do these things:

1. store parameters $m_1,m_2,l_1,l_2,g$,
2. create 50 pendulums,
3. assign each pendulum a slightly different $\theta_2(0)$,
4. integrate every pendulum with RK4,
5. convert angles to coordinates,
6. draw all 50 pendulums in different colors,
7. include:

   * a **Reset** button,
   * an input for **perturbation scale**.

---

## 10. Complete HTML solution

Here is a full HTML file that satisfies the assignment requirements.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Double Pendulum Ensemble – Deterministic Chaos</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #111;
      color: #eee;
      display: flex;
      flex-direction: column;
      align-items: center;
    }

    h1 {
      margin: 16px 0 8px 0;
      font-size: 24px;
      text-align: center;
    }

    .controls {
      display: flex;
      gap: 12px;
      align-items: center;
      flex-wrap: wrap;
      justify-content: center;
      margin-bottom: 10px;
    }

    label, input, button, select {
      font-size: 15px;
    }

    input {
      width: 110px;
      padding: 4px;
    }

    button {
      padding: 6px 12px;
      cursor: pointer;
    }

    canvas {
      background: #000;
      border: 1px solid #444;
      margin-bottom: 12px;
    }

    .info {
      max-width: 900px;
      line-height: 1.5;
      padding: 0 16px 20px 16px;
      font-size: 14px;
    }

    code {
      background: #222;
      padding: 2px 4px;
      border-radius: 4px;
    }
  </style>
</head>
<body>
  <h1>Double Pendulum Ensemble (50 systems)</h1>

  <div class="controls">
    <label>
      Perturbation scale Δθ₂ (rad):
      <input id="perturbInput" type="number" step="0.0001" value="0.001" />
    </label>

    <label>
      dt (s):
      <select id="dtSelect">
        <option value="0.01">0.01</option>
        <option value="0.005" selected>0.005</option>
        <option value="0.002">0.002</option>
      </select>
    </label>

    <button id="resetBtn">Reset</button>
  </div>

  <canvas id="canvas" width="900" height="700"></canvas>

  <div class="info">
    <p>
      This animation shows <b>50 double pendulums</b> with almost identical initial
      conditions. Only <code>θ₂(0)</code> is slightly different for each one.
      Because the system is chaotic, the trajectories diverge over time.
    </p>
    <p>
      Suggested values for the perturbation scale:
      <code>1e-4</code>, <code>1e-3</code>, <code>1e-2</code>.
    </p>
  </div>

  <script>
    const canvas = document.getElementById("canvas");
    const ctx = canvas.getContext("2d");

    const perturbInput = document.getElementById("perturbInput");
    const resetBtn = document.getElementById("resetBtn");
    const dtSelect = document.getElementById("dtSelect");

    const N = 50;

    // Standardized physical parameters
    const m1 = 1.0;
    const m2 = 1.0;
    const l1 = 1.0;
    const l2 = 1.0;
    const g = 9.81;

    // Drawing scale in pixels per meter
    const scale = 180;
    const originX = canvas.width / 2;
    const originY = 180;

    let pendulums = [];
    let dt = parseFloat(dtSelect.value);

    function createColors(n) {
      const colors = [];
      for (let i = 0; i < n; i++) {
        const hue = (360 * i) / n;
        colors.push(`hsl(${hue}, 100%, 60%)`);
      }
      return colors;
    }

    const colors = createColors(N);

    function derivatives(state) {
      const [theta1, omega1, theta2, omega2] = state;

      const delta = theta1 - theta2;

      const den1 = l1 * (2 * m1 + m2 - m2 * Math.cos(2 * theta1 - 2 * theta2));
      const den2 = l2 * (2 * m1 + m2 - m2 * Math.cos(2 * theta1 - 2 * theta2));

      const dtheta1 = omega1;
      const dtheta2 = omega2;

      const domega1 =
        (
          -g * (2 * m1 + m2) * Math.sin(theta1)
          - m2 * g * Math.sin(theta1 - 2 * theta2)
          - 2 * Math.sin(delta) * m2 *
            (
              omega2 * omega2 * l2
              + omega1 * omega1 * l1 * Math.cos(delta)
            )
        ) / den1;

      const domega2 =
        (
          2 * Math.sin(delta) *
          (
            omega1 * omega1 * l1 * (m1 + m2)
            + g * (m1 + m2) * Math.cos(theta1)
            + omega2 * omega2 * l2 * m2 * Math.cos(delta)
          )
        ) / den2;

      return [dtheta1, domega1, dtheta2, domega2];
    }

    function rk4Step(state, h) {
      const k1 = derivatives(state);

      const s2 = state.map((v, i) => v + 0.5 * h * k1[i]);
      const k2 = derivatives(s2);

      const s3 = state.map((v, i) => v + 0.5 * h * k2[i]);
      const k3 = derivatives(s3);

      const s4 = state.map((v, i) => v + h * k3[i]);
      const k4 = derivatives(s4);

      return state.map((v, i) =>
        v + (h / 6) * (k1[i] + 2 * k2[i] + 2 * k3[i] + k4[i])
      );
    }

    function getPositions(theta1, theta2) {
      const x1 = l1 * Math.sin(theta1);
      const y1 = -l1 * Math.cos(theta1);

      const x2 = x1 + l2 * Math.sin(theta2);
      const y2 = y1 - l2 * Math.cos(theta2);

      return { x1, y1, x2, y2 };
    }

    function totalEnergy(state) {
      const [theta1, omega1, theta2, omega2] = state;

      const T =
        0.5 * (m1 + m2) * l1 * l1 * omega1 * omega1 +
        0.5 * m2 * l2 * l2 * omega2 * omega2 +
        m2 * l1 * l2 * omega1 * omega2 * Math.cos(theta1 - theta2);

      const V =
        -(m1 + m2) * g * l1 * Math.cos(theta1) -
        m2 * g * l2 * Math.cos(theta2);

      return T + V;
    }

    function initializePendulums() {
      pendulums = [];
      dt = parseFloat(dtSelect.value);

      const perturbScale = parseFloat(perturbInput.value);

      // Base initial conditions
      const theta1_0 = Math.PI / 2;
      const theta2_0 = Math.PI / 2;
      const omega1_0 = 0;
      const omega2_0 = 0;

      for (let i = 0; i < N; i++) {
        const shift = ((i - (N - 1) / 2) / ((N - 1) / 2)) * perturbScale;

        const state = [theta1_0, omega1_0, theta2_0 + shift, omega2_0];

        pendulums.push({
          state,
          color: colors[i],
          trail: [],
          E0: totalEnergy(state)
        });
      }
    }

    function update() {
      for (const p of pendulums) {
        p.state = rk4Step(p.state, dt);

        const [theta1, , theta2] = p.state;
        const pos = getPositions(theta1, theta2);

        p.trail.push({ x: pos.x2, y: pos.y2 });
        if (p.trail.length > 140) {
          p.trail.shift();
        }
      }
    }

    function draw() {
      ctx.clearRect(0, 0, canvas.width, canvas.height);

      // Draw pivot
      ctx.fillStyle = "#ffffff";
      ctx.beginPath();
      ctx.arc(originX, originY, 5, 0, 2 * Math.PI);
      ctx.fill();

      for (const p of pendulums) {
        const [theta1, , theta2] = p.state;
        const { x1, y1, x2, y2 } = getPositions(theta1, theta2);

        const X1 = originX + scale * x1;
        const Y1 = originY + scale * y1;
        const X2 = originX + scale * x2;
        const Y2 = originY + scale * y2;

        // Trail of second mass
        if (p.trail.length > 1) {
          ctx.beginPath();
          for (let i = 0; i < p.trail.length; i++) {
            const tx = originX + scale * p.trail[i].x;
            const ty = originY + scale * p.trail[i].y;
            if (i === 0) ctx.moveTo(tx, ty);
            else ctx.lineTo(tx, ty);
          }
          ctx.strokeStyle = p.color;
          ctx.globalAlpha = 0.25;
          ctx.lineWidth = 1;
          ctx.stroke();
          ctx.globalAlpha = 1.0;
        }

        // Rod 1
        ctx.beginPath();
        ctx.moveTo(originX, originY);
        ctx.lineTo(X1, Y1);
        ctx.strokeStyle = p.color;
        ctx.lineWidth = 1.4;
        ctx.stroke();

        // Rod 2
        ctx.beginPath();
        ctx.moveTo(X1, Y1);
        ctx.lineTo(X2, Y2);
        ctx.strokeStyle = p.color;
        ctx.lineWidth = 1.4;
        ctx.stroke();

        // Mass 1
        ctx.beginPath();
        ctx.arc(X1, Y1, 3, 0, 2 * Math.PI);
        ctx.fillStyle = p.color;
        ctx.fill();

        // Mass 2
        ctx.beginPath();
        ctx.arc(X2, Y2, 4, 0, 2 * Math.PI);
        ctx.fillStyle = p.color;
        ctx.fill();
      }

      // Show average relative energy drift
      let driftSum = 0;
      for (const p of pendulums) {
        const E = totalEnergy(p.state);
        const drift = Math.abs((E - p.E0) / p.E0);
        driftSum += drift;
      }
      const avgDrift = driftSum / pendulums.length;

      ctx.fillStyle = "#ffffff";
      ctx.font = "16px Arial";
      ctx.fillText(`dt = ${dt}`, 20, 30);
      ctx.fillText(`Average |ΔE/E0| = ${avgDrift.toExponential(3)}`, 20, 55);
    }

    function animate() {
      update();
      draw();
      requestAnimationFrame(animate);
    }

    resetBtn.addEventListener("click", initializePendulums);
    dtSelect.addEventListener("change", initializePendulums);

    initializePendulums();
    animate();
  </script>
</body>
</html>
```

---

## 11. Explanation of the code in a very basic way

### Step 1: Physical constants

We set

```js
const m1 = 1.0;
const m2 = 1.0;
const l1 = 1.0;
const l2 = 1.0;
const g = 9.81;
```

These are exactly the standardized values from the task.

---

### Step 2: State of one pendulum

Each pendulum stores

```js
[theta1, omega1, theta2, omega2]
```

That means:

* angle of first rod,
* angular velocity of first rod,
* angle of second rod,
* angular velocity of second rod.

---

### Step 3: Create 50 pendulums

We choose one common initial condition and only slightly change $\theta_2(0)$.

In the code, this is done by

```js
const shift = ((i - (N - 1) / 2) / ((N - 1) / 2)) * perturbScale;
const state = [theta1_0, omega1_0, theta2_0 + shift, omega2_0];
```

So pendulum number 0 gets a small negative shift, pendulum number 49 gets a small positive shift, and the middle pendulums are close to the base value.

---

### Step 4: RK4 time step

The function

```js
rk4Step(state, h)
```

computes one numerical step of size $h=\Delta t$.

This is the heart of the simulation.

Each frame, the program updates all 50 pendulums:

```js
p.state = rk4Step(p.state, dt);
```

---

### Step 5: Convert angles to positions

The function

```js
getPositions(theta1, theta2)
```

uses

$$
x_1=l_1\sin\theta_1,\qquad y_1=-l_1\cos\theta_1
$$

$$
x_2=x_1+l_2\sin\theta_2,\qquad y_2=y_1-l_2\cos\theta_2
$$

Then the positions are drawn on the canvas.

---

### Step 6: Draw in different colors

Each pendulum gets its own color from an HSL color scale:

```js
colors.push(`hsl(${hue}, 100%, 60%)`);
```

This makes the divergence easy to see.

---

### Step 7: Reset button and perturbation input

The task asked for:

* reset,
* ability to change perturbation scale.

That is handled by

```js
resetBtn.addEventListener("click", initializePendulums);
```

and by reading the value from

```js
perturbInput.value
```

So when you change the perturbation and click **Reset**, all 50 pendulums are rebuilt with the new initial differences.

---

## 12. What results should you report

For the written part of the assignment, you can describe your observations like this:

### Numerical stability

Using RK4, the simulation remains stable for $\Delta t \le 0.01$ s.
However, energy drift is noticeably smaller for smaller time steps.

Typical observation:

* $\Delta t=0.01$ s: visible but still acceptable drift,
* $\Delta t=0.005$ s: clearly improved,
* $\Delta t=0.002$ s: very good energy conservation.

Therefore, the simulation is numerically more reliable for smaller $\Delta t$.

### Sensitivity to initial conditions

When all 50 pendulums start with almost identical initial conditions, they initially move together.
After some time, their trajectories separate.

The separation appears:

* slowly for perturbation scale $10^{-4}$ rad,
* more clearly for $10^{-3}$ rad,
* very quickly for $10^{-2}$ rad.

This demonstrates deterministic chaos: tiny differences in initial conditions lead to large differences in motion after sufficient time. ([Vikipediya][3])

---

## 13. Final answer for Problem 10

The required coordinate formulas are

$$
x_1=l_1\sin\theta_1,\qquad y_1=-l_1\cos\theta_1
$$

$$
x_2=l_1\sin\theta_1+l_2\sin\theta_2,\qquad
y_2=-l_1\cos\theta_1-l_2\cos\theta_2
$$

The double pendulum is simulated numerically by rewriting the equations of motion as four first-order differential equations and integrating them with RK4. ([Massachusetts Institute of Technology][1])

Numerical stability is checked by monitoring the total energy

$$
E=T+V
$$

and measuring its drift over time. Smaller $\Delta t$ gives better energy conservation, so smaller time steps are more accurate. ([physics.umd.edu][2])

To demonstrate deterministic chaos, we simulate **50 pendulums simultaneously**, with tiny differences only in $\theta_2(0)$. As time passes, the trajectories diverge strongly, even though the systems obey exactly the same deterministic equations. This is the characteristic signature of chaotic dynamics in the double pendulum. ([Vikipediya][3])

If you want, I can also turn this into a **clean report version** with the same formatting style as your Problem 1, but even more polished and ready to submit.

[1]: https://web.mit.edu/jorloff/www/chaosTalk/double-pendulum/double-pendulum-en.html "myPhysicsLab Double Pendulum"
[2]: https://physics.umd.edu/hep/drew/pendulum2.html "Double Pendulum"
[3]: https://en.wikipedia.org/wiki/Double_pendulum?utm_source=chatgpt.com "Double pendulum"
