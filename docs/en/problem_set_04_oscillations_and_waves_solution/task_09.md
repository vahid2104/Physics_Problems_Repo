## Problem 9 – Chain of (N) springs (discrete wave model)

We consider a line of (N) equal masses, each of mass (m), connected by identical springs of constant (k).

Each mass can move horizontally around its equilibrium position.

Let

[
x_i(t)
]

be the displacement of the (i)-th mass from equilibrium.

We want to:

1. write the equations of motion,
2. solve them numerically for (N=20,50,100),
3. create a local initial disturbance,
4. observe how the pulse moves,
5. study how (k) and (m) change the propagation speed.

---

## 1. Physical model

Each mass is connected to its neighbors by springs.

So:

* the first mass is connected to the second,
* the last mass is connected to the previous one,
* each interior mass is connected to two neighbors.

We assume small oscillations and identical springs.

---

## 2. Force acting on one mass

Consider an interior mass (i), where

[
i=2,3,\dots,N-1
]

The spring on the left pulls according to the relative displacement

[
x_{i-1}-x_i
]

The spring on the right pulls according to

[
x_{i+1}-x_i
]

By Hooke’s law, the total force is

[
F_i=k(x_{i+1}-x_i)-k(x_i-x_{i-1})
]

Simplify:

[
F_i=k(x_{i+1}-2x_i+x_{i-1})
]

Now use Newton’s second law:

[
m\ddot{x}_i=F_i
]

So for an interior mass,

[
m\ddot{x}*i=k(x*{i+1}-2x_i+x_{i-1})
]

Therefore,

[
\ddot{x}*i=\frac{k}{m}(x*{i+1}-2x_i+x_{i-1})
]

---

## 3. Equations of motion for the whole chain

### Interior masses

For

[
i=2,\dots,N-1
]

the equations are

[
m\ddot{x}*i=k(x*{i+1}-2x_i+x_{i-1})
]

---

### Boundary masses

To keep the model simple, we use **fixed ends**:

[
x_0=0, \qquad x_{N+1}=0
]

That means the chain is attached at both ends.

Then:

#### First mass

[
m\ddot{x}_1=k(x_2-2x_1+x_0)
]

Since (x_0=0),

[
m\ddot{x}_1=k(x_2-2x_1)
]

#### Last mass

[
m\ddot{x}*N=k(x*{N+1}-2x_N+x_{N-1})
]

Since (x_{N+1}=0),

[
m\ddot{x}*N=k(x*{N-1}-2x_N)
]

---

## 4. Final system of equations

So the chain is described by

[
m\ddot{x}_1=k(x_2-2x_1)
]

[
m\ddot{x}*i=k(x*{i+1}-2x_i+x_{i-1}), \qquad i=2,\dots,N-1
]

[
m\ddot{x}*N=k(x*{N-1}-2x_N)
]

These are (N) coupled second-order differential equations.

---

## 5. Local initial disturbance

Now we need to disturb the chain only in one small region.

A simple choice is:

* initially all velocities are zero,
* only one mass or a few nearby masses are displaced.

For example, if the middle mass is displaced:

[
x_i(0)=
\begin{cases}
A, & i=\frac{N}{2} \
0, & \text{otherwise}
\end{cases}
]

and

[
\dot{x}_i(0)=0
]

This creates a local pulse.

Another smoother choice is a Gaussian-like shape:

[
x_i(0)=A\exp\left[-\frac{(i-i_0)^2}{\sigma^2}\right]
]

with all initial velocities equal to zero.

This is often better numerically, because it produces a cleaner pulse.

---

## 6. Numerical solution idea

The equations are too large to solve by hand for (N=20,50,100), so we solve them numerically.

We rewrite the motion in time steps:

[
t_0,\ t_1,\ t_2,\dots
]

with small step

[
\Delta t
]

At each step we compute:

1. the acceleration of each mass,
2. update velocity,
3. update position.

A simple stable method is **Euler-Cromer**.

---

## 7. Acceleration formula

From the equations of motion,

[
a_i=\ddot{x}*i=\frac{k}{m}(x*{i+1}-2x_i+x_{i-1})
]

For fixed ends we use

[
x_0=0,\qquad x_{N+1}=0
]

So at each time step we can compute all accelerations.

---

## 8. Time stepping formulas

If (v_i) is the velocity of mass (i), then Euler-Cromer gives

[
v_i^{,new}=v_i+\Delta t, a_i
]

[
x_i^{,new}=x_i+\Delta t, v_i^{,new}
]

We repeat this many times.

That gives the full numerical motion.

---

## 9. What we expect physically

When only one part of the chain is disturbed, that disturbance does not stay in one place.

Instead:

* the disturbed mass pulls its neighbors,
* they start moving,
* the pulse travels along the chain.

So we observe **wave propagation** in a discrete system.

At the fixed ends, the pulse reflects and travels back.

---

## 10. Effect of (N=20,50,100)

We now compare three chain lengths.

### Case (N=20)

The chain is short.

So:

* the pulse reaches the end quickly,
* reflections happen soon,
* the motion looks more “coarse” because there are fewer masses.

---

### Case (N=50)

The chain is longer.

So:

* the pulse travels farther before reflection,
* the shape of the propagation is smoother than for (N=20),
* the wave behavior is easier to see.

---

### Case (N=100)

The chain is even longer.

So:

* the system looks closer to a continuous string,
* the pulse propagation becomes smoother,
* reflections take longer to appear.

As (N) increases, the discrete model resembles a continuous wave more closely.

---

## 11. Effect of (k) and (m) on propagation speed

From the equation

[
\ddot{x}*i=\frac{k}{m}(x*{i+1}-2x_i+x_{i-1})
]

we see that the factor controlling the dynamics is

[
\frac{k}{m}
]

This means:

* if (k) increases, the springs are stiffer,
* if (m) increases, the masses are heavier.

### Larger (k)

A larger spring constant means stronger restoring forces.

So the neighbors react more quickly.

Therefore, the pulse moves faster.

---

### Larger (m)

A larger mass means more inertia.

So each mass is harder to accelerate.

Therefore, the pulse moves more slowly.

---

### Approximate dependence

The propagation speed in a spring-mass chain is proportional to

[
v \propto \sqrt{\frac{k}{m}}
]

So:

* doubling (k) increases speed by factor (\sqrt{2}),
* doubling (m) decreases speed by factor (\sqrt{2}).

---

## 12. Interpretation of the propagation speed

So the main rule is:

[
\text{faster propagation} \Longleftrightarrow \text{large }k \text{ and small }m
]

[
\text{slower propagation} \Longleftrightarrow \text{small }k \text{ and large }m
]

This is exactly what we should observe in the numerical simulation.

---

## 13. Example numerical setup

A typical simulation may use:

[
A=1
]

[
\Delta t=0.02
]

[
k=1,\qquad m=1
]

with a local initial disturbance at the center.

Then we can repeat the simulation for:

* (N=20),
* (N=50),
* (N=100),

and later compare different values such as:

* (k=0.5,\ 1,\ 2),
* (m=0.5,\ 1,\ 2).

---

## 14. What to observe in the animation

In the animation, you should see:

1. the initially displaced region starts moving,
2. the disturbance splits and travels through the chain,
3. the pulse reaches the boundaries,
4. the pulse reflects,
5. changing (k) or (m) changes how quickly this happens.

So the animation directly shows discrete wave propagation.

---

## 15. Final conclusions

The equations of motion for a chain of (N) masses and springs are

[
m\ddot{x}_1=k(x_2-2x_1)
]

[
m\ddot{x}*i=k(x*{i+1}-2x_i+x_{i-1}), \qquad i=2,\dots,N-1
]

[
m\ddot{x}*N=k(x*{N-1}-2x_N)
]

with fixed ends

[
x_0=0,\qquad x_{N+1}=0
]

A local initial disturbance produces a pulse that propagates through the chain.

For larger (N), the motion looks smoother and more wave-like.

The propagation speed depends mainly on

[
\sqrt{\frac{k}{m}}
]

So:

* increasing (k) makes the pulse faster,
* increasing (m) makes the pulse slower.

---

# HTML requirement – animation of the entire chain

Below is a complete HTML file that animates the chain for (N=20,50,100) and lets you change (k) and (m).

Save it as `chain_springs.html` and open it in a browser.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Chain of N Springs – Discrete Wave Model</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 20px;
      background: #f4f6f8;
      color: #222;
    }

    h1 {
      text-align: center;
    }

    .controls {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
      justify-content: center;
      margin-bottom: 20px;
      background: white;
      padding: 15px;
      border-radius: 10px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.08);
    }

    .controls label {
      font-weight: bold;
    }

    .controls input,
    .controls select,
    .controls button {
      padding: 6px 10px;
      font-size: 14px;
    }

    canvas {
      display: block;
      margin: 0 auto;
      background: white;
      border: 1px solid #ccc;
      border-radius: 10px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.08);
    }

    .info {
      max-width: 900px;
      margin: 20px auto 0;
      background: white;
      padding: 15px;
      border-radius: 10px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.08);
      line-height: 1.6;
    }

    code {
      background: #eef;
      padding: 2px 5px;
      border-radius: 4px;
    }
  </style>
</head>
<body>
  <h1>Chain of N Springs – Discrete Wave Model</h1>

  <div class="controls">
    <label>
      N:
      <select id="N">
        <option value="20">20</option>
        <option value="50" selected>50</option>
        <option value="100">100</option>
      </select>
    </label>

    <label>
      k:
      <input type="number" id="k" value="1" step="0.1" min="0.1">
    </label>

    <label>
      m:
      <input type="number" id="m" value="1" step="0.1" min="0.1">
    </label>

    <label>
      dt:
      <input type="number" id="dt" value="0.02" step="0.005" min="0.001">
    </label>

    <label>
      Disturbance amplitude:
      <input type="number" id="A" value="40" step="5">
    </label>

    <button id="restartBtn">Restart simulation</button>
  </div>

  <canvas id="canvas" width="1000" height="420"></canvas>

  <div class="info">
    <p><strong>How it works:</strong> The masses are connected by springs. A local displacement is given near the center, and then the system evolves using the Euler-Cromer method.</p>
    <p><strong>Observe:</strong> the pulse travels through the chain, reflects at the fixed ends, and changes speed when <code>k</code> or <code>m</code> changes.</p>
    <p><strong>Main rule:</strong> propagation speed is approximately proportional to <code>sqrt(k/m)</code>.</p>
  </div>

  <script>
    const canvas = document.getElementById("canvas");
    const ctx = canvas.getContext("2d");

    const NInput = document.getElementById("N");
    const kInput = document.getElementById("k");
    const mInput = document.getElementById("m");
    const dtInput = document.getElementById("dt");
    const AInput = document.getElementById("A");
    const restartBtn = document.getElementById("restartBtn");

    let N, k, m, dt, A;
    let x = [], v = [], a = [];
    let baseX = [];
    let centerY = canvas.height / 2;
    let leftMargin = 60;
    let rightMargin = 60;

    function initSimulation() {
      N = parseInt(NInput.value);
      k = parseFloat(kInput.value);
      m = parseFloat(mInput.value);
      dt = parseFloat(dtInput.value);
      A = parseFloat(AInput.value);

      x = new Array(N).fill(0);
      v = new Array(N).fill(0);
      a = new Array(N).fill(0);
      baseX = new Array(N);

      const spacing = (canvas.width - leftMargin - rightMargin) / (N - 1);
      for (let i = 0; i < N; i++) {
        baseX[i] = leftMargin + i * spacing;
      }

      // Local Gaussian disturbance near the center
      const i0 = Math.floor(N / 2);
      const sigma = Math.max(2, N / 15);

      for (let i = 0; i < N; i++) {
        x[i] = A * Math.exp(-((i - i0) * (i - i0)) / (sigma * sigma));
        v[i] = 0;
      }
    }

    function computeAcceleration() {
      for (let i = 0; i < N; i++) {
        const left = (i === 0) ? 0 : x[i - 1];
        const right = (i === N - 1) ? 0 : x[i + 1];
        a[i] = (k / m) * (right - 2 * x[i] + left);
      }
    }

    function stepSimulation() {
      computeAcceleration();

      for (let i = 0; i < N; i++) {
        v[i] += a[i] * dt;
        x[i] += v[i] * dt;
      }
    }

    function draw() {
      ctx.clearRect(0, 0, canvas.width, canvas.height);

      // Guide line
      ctx.strokeStyle = "#cccccc";
      ctx.lineWidth = 1;
      ctx.beginPath();
      ctx.moveTo(leftMargin, centerY);
      ctx.lineTo(canvas.width - rightMargin, centerY);
      ctx.stroke();

      // Springs/links
      ctx.strokeStyle = "#2a6";
      ctx.lineWidth = 2;
      ctx.beginPath();
      ctx.moveTo(baseX[0], centerY - x[0]);
      for (let i = 1; i < N; i++) {
        ctx.lineTo(baseX[i], centerY - x[i]);
      }
      ctx.stroke();

      // Masses
      for (let i = 0; i < N; i++) {
        ctx.beginPath();
        ctx.fillStyle = "#1565c0";
        ctx.arc(baseX[i], centerY - x[i], 5, 0, 2 * Math.PI);
        ctx.fill();
      }

      // Text
      ctx.fillStyle = "#111";
      ctx.font = "16px Arial";
      ctx.fillText(`N = ${N}`, 20, 25);
      ctx.fillText(`k = ${k}`, 20, 50);
      ctx.fillText(`m = ${m}`, 20, 75);
      ctx.fillText(`Approx. speed ~ sqrt(k/m) = ${Math.sqrt(k/m).toFixed(3)}`, 20, 100);
    }

    function animate() {
      stepSimulation();
      draw();
      requestAnimationFrame(animate);
    }

    restartBtn.addEventListener("click", () => {
      initSimulation();
    });

    initSimulation();
    animate();
  </script>
</body>
</html>
```

---

## 16. Short report-style summary

You can also write the final result in a compact form like this:

### Final answer for Problem 9

A chain of (N) masses connected by springs satisfies

[
m\ddot{x}*i=k(x*{i+1}-2x_i+x_{i-1})
]

for interior masses, with fixed-end boundary conditions

[
x_0=0,\qquad x_{N+1}=0
]

Numerical simulation for (N=20,50,100) shows that a local initial disturbance propagates as a pulse through the chain and reflects at the ends.

For larger (N), the system behaves more like a continuous wave medium.

The propagation speed increases when (k) increases and decreases when (m) increases.

Approximately,

[
v\propto \sqrt{\frac{k}{m}}
]

Thus:

* stiffer springs ((k) larger()) give faster propagation,
* heavier masses ((m) larger()) give slower propagation.

The HTML animation shows the motion of the full chain and allows direct observation of these effects.

---

