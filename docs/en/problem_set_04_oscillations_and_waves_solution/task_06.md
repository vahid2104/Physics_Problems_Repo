## Problem 6 – Damped oscillator

We study the equation

$$
m\frac{d^2x}{dt^2}+b\frac{dx}{dt}+kx=0
$$

We want to:

1. derive the general solution,
2. classify the motion,
3. solve it numerically using RK4,
4. investigate the effect of (b),
5. generate the graph of (x(t)),
6. generate the phase portrait,
7. and prepare HTML with an interactive slider for (b).

---

## 1. Rewrite the equation in standard form

We start with

$$
m\frac{d^2x}{dt^2}+b\frac{dx}{dt}+kx=0
$$

Divide the whole equation by (m):

$$
\frac{d^2x}{dt^2}+\frac{b}{m}\frac{dx}{dt}+\frac{k}{m}x=0
$$

So the equation becomes

$$
x''+\frac{b}{m}x'+\frac{k}{m}x=0
$$

This is a linear second-order differential equation with constant coefficients.

---

## 2. Characteristic equation

To solve it, we try a solution of the form

$$
x(t)=e^{rt}
$$

Then

$$
x'(t)=re^{rt}, \qquad x''(t)=r^2e^{rt}
$$

Substitute into the differential equation:

$$
r^2e^{rt}+\frac{b}{m}re^{rt}+\frac{k}{m}e^{rt}=0
$$

Factor out (e^{rt}):

$$
e^{rt}\left(r^2+\frac{b}{m}r+\frac{k}{m}\right)=0
$$

Since (e^{rt}\neq 0), we get the characteristic equation:

$$
r^2+\frac{b}{m}r+\frac{k}{m}=0
$$

Multiply by (m):

$$
mr^2+br+k=0
$$

So the roots are

$$
r=\frac{-b\pm\sqrt{b^2-4mk}}{2m}
$$

Now the type of solution depends on the discriminant

$$
\Delta=b^2-4mk
$$

---

## 3. Classification of cases

There are three cases.

---

### Case 1: Underdamped motion

This happens when

$$
b^2<4mk
$$

Then the discriminant is negative, so the roots are complex:

$$
r=\frac{-b}{2m}\pm i\omega_d
$$

where

$$
\omega_d=\sqrt{\frac{k}{m}-\left(\frac{b}{2m}\right)^2}
$$

Therefore the solution is

$$
x(t)=e^{-\frac{b}{2m}t}\left(C_1\cos(\omega_d t)+C_2\sin(\omega_d t)\right)
$$

This is an oscillation with exponentially decreasing amplitude.

So in the underdamped case:

* the body still oscillates,
* but the amplitude gets smaller with time.

---

### Case 2: Critically damped motion

This happens when

$$
b^2=4mk
$$

Then the characteristic equation has one repeated root:

$$
r=-\frac{b}{2m}
$$

So the general solution is

$$
x(t)=\left(C_1+C_2 t\right)e^{-\frac{b}{2m}t}
$$

This case does not oscillate.

It returns to equilibrium as fast as possible without oscillating.

---

### Case 3: Overdamped motion

This happens when

$$
b^2>4mk
$$

Then the roots are real and different:

$$
r_1=\frac{-b+\sqrt{b^2-4mk}}{2m}, \qquad
r_2=\frac{-b-\sqrt{b^2-4mk}}{2m}
$$

So the general solution is

$$
x(t)=C_1e^{r_1 t}+C_2e^{r_2 t}
$$

This case also does not oscillate.

The system returns to equilibrium more slowly than in the critically damped case.

---

## 4. Summary of classification

The motion is classified by comparing (b^2) and (4mk):

### Underdamped

$$
b^2<4mk
$$

General solution:

$$
x(t)=e^{-\frac{b}{2m}t}\left(C_1\cos(\omega_d t)+C_2\sin(\omega_d t)\right)
$$

with

$$
\omega_d=\sqrt{\frac{k}{m}-\left(\frac{b}{2m}\right)^2}
$$

Behavior: oscillatory motion with decaying amplitude.

---

### Critically damped

$$
b^2=4mk
$$

General solution:

$$
x(t)=\left(C_1+C_2 t\right)e^{-\frac{b}{2m}t}
$$

Behavior: fastest return to equilibrium without oscillation.

---

### Overdamped

$$
b^2>4mk
$$

General solution:

$$
x(t)=C_1e^{r_1 t}+C_2e^{r_2 t}
$$

where

$$
r_{1,2}=\frac{-b\pm\sqrt{b^2-4mk}}{2m}
$$

Behavior: no oscillation, slower return to equilibrium.

---

## 5. Convert the equation to a system for RK4

To solve numerically, we convert the second-order equation into a first-order system.

Let

$$
x_1=x
$$

and

$$
x_2=\frac{dx}{dt}=v
$$

Then

$$
\frac{dx_1}{dt}=x_2
$$

and from the original equation

$$
m\frac{d^2x}{dt^2}+b\frac{dx}{dt}+kx=0
$$

we get

$$
\frac{d^2x}{dt^2}=-\frac{b}{m}\frac{dx}{dt}-\frac{k}{m}x
$$

So

$$
\frac{dx_2}{dt}=-\frac{b}{m}x_2-\frac{k}{m}x_1
$$

Therefore the system is

$$
\frac{dx}{dt}=v
$$

$$
\frac{dv}{dt}=-\frac{b}{m}v-\frac{k}{m}x
$$

This is the form we use in RK4.

---

## 6. RK4 method

Suppose the system is

$$
\frac{dx}{dt}=f(t,x,v)
$$

$$
\frac{dv}{dt}=g(t,x,v)
$$

Here,

$$
f(t,x,v)=v
$$

$$
g(t,x,v)=-\frac{b}{m}v-\frac{k}{m}x
$$

For step size (h), RK4 gives:

### For (x):

$$
k_{1x}=h,f(t_n,x_n,v_n)
$$

$$
k_{2x}=h,f\left(t_n+\frac{h}{2},x_n+\frac{k_{1x}}{2},v_n+\frac{k_{1v}}{2}\right)
$$

$$
k_{3x}=h,f\left(t_n+\frac{h}{2},x_n+\frac{k_{2x}}{2},v_n+\frac{k_{2v}}{2}\right)
$$

$$
k_{4x}=h,f(t_n+h,x_n+k_{3x},v_n+k_{3v})
$$

### For (v):

$$
k_{1v}=h,g(t_n,x_n,v_n)
$$

$$
k_{2v}=h,g\left(t_n+\frac{h}{2},x_n+\frac{k_{1x}}{2},v_n+\frac{k_{1v}}{2}\right)
$$

$$
k_{3v}=h,g\left(t_n+\frac{h}{2},x_n+\frac{k_{2x}}{2},v_n+\frac{k_{2v}}{2}\right)
$$

$$
k_{4v}=h,g(t_n+h,x_n+k_{3x},v_n+k_{3v})
$$

Then update:

$$
x_{n+1}=x_n+\frac{1}{6}(k_{1x}+2k_{2x}+2k_{3x}+k_{4x})
$$

$$
v_{n+1}=v_n+\frac{1}{6}(k_{1v}+2k_{2v}+2k_{3v}+k_{4v})
$$

This gives the numerical solution.

---

## 7. Effect of parameter (b)

Now let us investigate how the damping coefficient (b) changes the motion.

The equation is

$$
m x''+b x'+k x=0
$$

The term

$$
b x'
$$

is the damping force.

This force opposes the motion and removes energy from the system.

### When (b) is small

If (b) is small, then damping is weak.

So:

* the body still oscillates,
* the amplitude decreases slowly,
* the motion is underdamped.

---

### When (b) increases

As (b) becomes larger:

* the oscillations die out faster,
* the frequency becomes slightly smaller,
* the phase trajectory spirals to the origin more quickly.

---

### At the critical value

Critical damping occurs when

$$
b=b_c=2\sqrt{mk}
$$

At this value:

* oscillation just disappears,
* the body returns to equilibrium as fast as possible without overshooting.

---

### When (b>b_c)

Then the motion is overdamped.

So:

* there is no oscillation,
* the body slowly approaches equilibrium,
* the phase portrait no longer shows spirals.

---

## 8. Physical interpretation

The point (x=0) is the equilibrium position.

The damping term causes energy loss, so eventually the motion stops.

### In the graph (x(t)):

* underdamped motion looks like a decaying wave,
* critically damped motion falls to zero quickly without oscillation,
* overdamped motion falls to zero slowly without oscillation.

### In the phase portrait ((x,v)):

* underdamped motion gives a spiral toward the origin,
* critically damped motion approaches the origin without spiraling,
* overdamped motion approaches the origin more directly.

---

## 9. Example parameters

For an example, choose:

$$
m=1, \qquad k=4
$$

Then the critical damping value is

$$
b_c=2\sqrt{mk}=2\sqrt{1\cdot 4}=4
$$

So:

* if (b<4), motion is underdamped,
* if (b=4), motion is critically damped,
* if (b>4), motion is overdamped.

For example:

* (b=1): underdamped,
* (b=4): critically damped,
* (b=7): overdamped.

---

## 10. Final mathematical answer

The equation

$$
m x''+b x'+kx=0
$$

has characteristic equation

$$
mr^2+br+k=0
$$

with roots

$$
r=\frac{-b\pm\sqrt{b^2-4mk}}{2m}
$$

The three cases are:

### Underdamped

$$
b^2<4mk
$$

$$
x(t)=e^{-\frac{b}{2m}t}\left(C_1\cos(\omega_d t)+C_2\sin(\omega_d t)\right)
$$

where

$$
\omega_d=\sqrt{\frac{k}{m}-\left(\frac{b}{2m}\right)^2}
$$

---

### Critically damped

$$
b^2=4mk
$$

$$
x(t)=\left(C_1+C_2t\right)e^{-\frac{b}{2m}t}
$$

---

### Overdamped

$$
b^2>4mk
$$

$$
x(t)=C_1e^{r_1 t}+C_2e^{r_2 t}
$$

where

$$
r_{1,2}=\frac{-b\pm\sqrt{b^2-4mk}}{2m}
$$

---

## 11. HTML with interactive slider for (b)

Below is a complete HTML file. It:

* solves the damped oscillator numerically using RK4,
* lets you change (b) with a slider,
* plots (x(t)),
* plots the phase portrait ((x,v)),
* displays the classification.

Save it as `damped_oscillator.html` and open it in a browser.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Damped Oscillator</title>
  <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 20px;
      background: #f4f4f4;
      color: #222;
    }
    h1, h2 {
      text-align: center;
    }
    .controls {
      background: white;
      padding: 15px;
      border-radius: 10px;
      max-width: 900px;
      margin: 0 auto 20px auto;
      box-shadow: 0 2px 8px rgba(0,0,0,0.1);
    }
    .charts {
      display: grid;
      grid-template-columns: 1fr;
      gap: 20px;
      max-width: 900px;
      margin: 0 auto;
    }
    .chart-box {
      background: white;
      padding: 15px;
      border-radius: 10px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.1);
    }
    label {
      font-weight: bold;
    }
    input[type="range"] {
      width: 100%;
    }
    .info {
      margin-top: 10px;
      font-size: 1rem;
    }
    .formula {
      font-family: "Courier New", monospace;
      background: #eee;
      padding: 8px;
      border-radius: 6px;
      margin-top: 10px;
    }
  </style>
</head>
<body>

  <h1>Damped Oscillator</h1>

  <div class="controls">
    <p>Equation:</p>
    <div class="formula">m x'' + b x' + k x = 0</div>

    <br>

    <label for="bSlider">Damping coefficient b:</label>
    <input type="range" id="bSlider" min="0" max="10" step="0.1" value="1">
    <p><strong>b = <span id="bValue">1.0</span></strong></p>

    <div class="info">
      <p><strong>Parameters:</strong> m = 1, k = 4, x(0) = 1, v(0) = 0</p>
      <p><strong>Critical damping:</strong> \( b_c = 2\sqrt{mk} = 4 \)</p>
      <p><strong>Case:</strong> <span id="caseType">Underdamped</span></p>
    </div>
  </div>

  <div class="charts">
    <div class="chart-box">
      <h2>Displacement x(t)</h2>
      <canvas id="xtChart"></canvas>
    </div>

    <div class="chart-box">
      <h2>Phase Portrait (v vs x)</h2>
      <canvas id="phaseChart"></canvas>
    </div>
  </div>

  <script>
    const m = 1.0;
    const k = 4.0;
    const x0 = 1.0;
    const v0 = 0.0;
    const dt = 0.02;
    const tMax = 20.0;

    const bSlider = document.getElementById("bSlider");
    const bValue = document.getElementById("bValue");
    const caseType = document.getElementById("caseType");

    let xtChart, phaseChart;

    function derivatives(x, v, b) {
      return {
        dxdt: v,
        dvdt: -(b / m) * v - (k / m) * x
      };
    }

    function rk4Step(x, v, b, h) {
      const k1 = derivatives(x, v, b);

      const k2 = derivatives(
        x + 0.5 * h * k1.dxdt,
        v + 0.5 * h * k1.dvdt,
        b
      );

      const k3 = derivatives(
        x + 0.5 * h * k2.dxdt,
        v + 0.5 * h * k2.dvdt,
        b
      );

      const k4 = derivatives(
        x + h * k3.dxdt,
        v + h * k3.dvdt,
        b
      );

      const xNext = x + (h / 6) * (k1.dxdt + 2 * k2.dxdt + 2 * k3.dxdt + k4.dxdt);
      const vNext = v + (h / 6) * (k1.dvdt + 2 * k2.dvdt + 2 * k3.dvdt + k4.dvdt);

      return { xNext, vNext };
    }

    function simulate(b) {
      const tData = [];
      const xData = [];
      const phaseData = [];

      let x = x0;
      let v = v0;

      for (let t = 0; t <= tMax; t += dt) {
        tData.push(t.toFixed(2));
        xData.push(x);
        phaseData.push({ x: x, y: v });

        const step = rk4Step(x, v, b, dt);
        x = step.xNext;
        v = step.vNext;
      }

      return { tData, xData, phaseData };
    }

    function classify(b) {
      const disc = b * b - 4 * m * k;
      if (disc < 0) return "Underdamped";
      if (disc === 0) return "Critically damped";
      return "Overdamped";
    }

    function updateCharts() {
      const b = parseFloat(bSlider.value);
      bValue.textContent = b.toFixed(1);
      caseType.textContent = classify(b);

      const result = simulate(b);

      if (xtChart) xtChart.destroy();
      if (phaseChart) phaseChart.destroy();

      const xtCtx = document.getElementById("xtChart").getContext("2d");
      xtChart = new Chart(xtCtx, {
        type: "line",
        data: {
          labels: result.tData,
          datasets: [{
            label: "x(t)",
            data: result.xData,
            borderColor: "blue",
            fill: false,
            pointRadius: 0
          }]
        },
        options: {
          responsive: true,
          scales: {
            x: {
              title: { display: true, text: "t" }
            },
            y: {
              title: { display: true, text: "x(t)" }
            }
          }
        }
      });

      const phaseCtx = document.getElementById("phaseChart").getContext("2d");
      phaseChart = new Chart(phaseCtx, {
        type: "scatter",
        data: {
          datasets: [{
            label: "Phase portrait",
            data: result.phaseData,
            showLine: true,
            borderColor: "red",
            backgroundColor: "red",
            pointRadius: 0
          }]
        },
        options: {
          responsive: true,
          scales: {
            x: {
              title: { display: true, text: "x" }
            },
            y: {
              title: { display: true, text: "v" }
            }
          }
        }
      });
    }

    bSlider.addEventListener("input", updateCharts);
    updateCharts();
  </script>

</body>
</html>
```

---

## 12. What you can say about the graphs

When you move the slider:

### For small (b)

You will see:

* oscillations in (x(t)),
* slowly decreasing amplitude,
* a spiral in the phase portrait.

This is underdamped motion.

---

### For (b=4)

You will see:

* no oscillation,
* fastest approach to zero,
* phase curve goes directly to the origin.

This is critical damping.

---

### For large (b)

You will see:

* no oscillation,
* slower approach to equilibrium,
* no spiral in phase space.

This is overdamped motion.

---

## Final answers for Problem 6

The damped oscillator

$$
m x'' + b x' + kx = 0
$$

has characteristic equation

$$
mr^2+br+k=0
$$

The roots are

$$
r=\frac{-b\pm\sqrt{b^2-4mk}}{2m}
$$

The cases are:

### Underdamped

$$
b^2<4mk
$$

$$
x(t)=e^{-\frac{b}{2m}t}\left(C_1\cos(\omega_d t)+C_2\sin(\omega_d t)\right)
$$

---

### Critically damped

$$
b^2=4mk
$$

$$
x(t)=\left(C_1+C_2t\right)e^{-\frac{b}{2m}t}
$$

---

### Overdamped

$$
b^2>4mk
$$

$$
x(t)=C_1e^{r_1t}+C_2e^{r_2t}
$$

The numerical RK4 method uses the system

$$
\frac{dx}{dt}=v
$$

$$
\frac{dv}{dt}=-\frac{b}{m}v-\frac{k}{m}x
$$

Increasing (b) makes the motion more strongly damped:

* small (b): oscillatory decay,
* critical (b): fastest non-oscillatory return,
* large (b): slow non-oscillatory return.

The graph (x(t)) and the phase portrait clearly show these three regimes.

