## Problem 7 – Forced oscillator and resonance

We are given the differential equation

$$
m \frac{d^2 x}{dt^2} + b \frac{dx}{dt} + k x = F_0 \cos(\Omega t)
$$

We want to:

1. solve the equation analytically,
2. solve it numerically,
3. study the steady-state amplitude as a function of $\Omega$,
4. generate the resonance curve,
5. investigate the phase shift,
6. explain the phenomenon of resonance.

To keep the explanation basic and clear, we will proceed step by step in the same style as your Problem 1.

---

## 1. Meaning of the equation

The equation

$$
m \frac{d^2 x}{dt^2} + b \frac{dx}{dt} + k x = F_0 \cos(\Omega t)
$$

describes a **driven damped oscillator**.

Each term has a physical meaning:

* $m \dfrac{d^2x}{dt^2}$ is the inertia term,
* $b \dfrac{dx}{dt}$ is damping,
* $kx$ is the spring restoring force,
* $F_0\cos(\Omega t)$ is an external periodic driving force.

So this is a mass on a spring with friction, while an external force keeps pushing it periodically.

---

## 2. Solve the equation analytically

The total solution is the sum of:

$$
x(t)=x_h(t)+x_p(t)
$$

where:

* $x_h(t)$ is the solution of the homogeneous equation,
* $x_p(t)$ is a particular solution caused by the driving force.

---

### 2.1 Homogeneous solution

First solve

$$
m \frac{d^2 x}{dt^2} + b \frac{dx}{dt} + k x = 0
$$

Divide by $m$:

$$
\frac{d^2x}{dt^2}+\frac{b}{m}\frac{dx}{dt}+\frac{k}{m}x=0
$$

Assume a solution of the form

$$
x_h(t)=e^{rt}
$$

Then

$$
mr^2+br+k=0
$$

This is the characteristic equation.

For the usual underdamped case, the solution is

$$
x_h(t)=e^{-\frac{b}{2m}t}\left(C_1\cos(\omega_d t)+C_2\sin(\omega_d t)\right)
$$

where

$$
\omega_d=\sqrt{\frac{k}{m}-\frac{b^2}{4m^2}}
$$

This part dies out with time because of the exponential factor.

So after a long time, the motion is dominated by the forced oscillation.

---

### 2.2 Particular solution

Now solve

$$
m \frac{d^2 x}{dt^2} + b \frac{dx}{dt} + k x = F_0 \cos(\Omega t)
$$

Because the forcing is cosine, we try a solution of the form

$$
x_p(t)=C\cos(\Omega t)+D\sin(\Omega t)
$$

Differentiate:

$$
\frac{dx_p}{dt}=-C\Omega\sin(\Omega t)+D\Omega\cos(\Omega t)
$$

$$
\frac{d^2x_p}{dt^2}=-C\Omega^2\cos(\Omega t)-D\Omega^2\sin(\Omega t)
$$

Substitute into the equation:

$$
m(-C\Omega^2\cos(\Omega t)-D\Omega^2\sin(\Omega t))
+b(-C\Omega\sin(\Omega t)+D\Omega\cos(\Omega t))
+k(C\cos(\Omega t)+D\sin(\Omega t))
=F_0\cos(\Omega t)
$$

Now group cosine terms and sine terms.

For $\cos(\Omega t)$:

$$
(k-m\Omega^2)C+b\Omega D
$$

For $\sin(\Omega t)$:

$$
(k-m\Omega^2)D-b\Omega C
$$

So we get the system

$$
(k-m\Omega^2)C+b\Omega D=F_0
$$

$$
(k-m\Omega^2)D-b\Omega C=0
$$

Solve this system. The result is

$$
C=\frac{F_0(k-m\Omega^2)}{(k-m\Omega^2)^2+b^2\Omega^2}
$$

$$
D=\frac{F_0 b\Omega}{(k-m\Omega^2)^2+b^2\Omega^2}
$$

Therefore,

$$
x_p(t)=
\frac{F_0(k-m\Omega^2)}{(k-m\Omega^2)^2+b^2\Omega^2}\cos(\Omega t)
+
\frac{F_0 b\Omega}{(k-m\Omega^2)^2+b^2\Omega^2}\sin(\Omega t)
$$

---

### 2.3 Amplitude form

It is more convenient to write the steady-state motion as

$$
x_p(t)=A(\Omega)\cos(\Omega t-\delta)
$$

Using the identity

$$
A\cos(\Omega t-\delta)=A\cos\delta\cos(\Omega t)+A\sin\delta\sin(\Omega t)
$$

we compare coefficients:

$$
A\cos\delta=C
$$

$$
A\sin\delta=D
$$

So the amplitude is

$$
A(\Omega)=\sqrt{C^2+D^2}
$$

Substitute $C$ and $D$:

$$
A(\Omega)=
\frac{F_0}{\sqrt{(k-m\Omega^2)^2+b^2\Omega^2}}
$$

This is the most important formula.

Therefore, the **steady-state amplitude as a function of driving frequency** is

$$
\boxed{
A(\Omega)=\frac{F_0}{\sqrt{(k-m\Omega^2)^2+b^2\Omega^2}}
}
$$

---

### 2.4 Phase shift

From

$$
\tan\delta=\frac{D}{C}
$$

we get

$$
\tan\delta=\frac{b\Omega}{k-m\Omega^2}
$$

So the phase shift is

$$
\boxed{
\delta(\Omega)=\arctan!\left(\frac{b\Omega}{k-m\Omega^2}\right)
}
$$

More precisely, to choose the correct quadrant, in numerical work it is best to use

$$
\boxed{
\delta(\Omega)=\operatorname{atan2}(b\Omega,;k-m\Omega^2)
}
$$

---

## 3. Final analytical solution

So the full solution is

$$
x(t)=x_h(t)+x_p(t)
$$

For the underdamped case:

$$
x(t)=
e^{-\frac{b}{2m}t}\left(C_1\cos(\omega_d t)+C_2\sin(\omega_d t)\right)
+
A(\Omega)\cos(\Omega t-\delta)
$$

where

$$
\omega_d=\sqrt{\frac{k}{m}-\frac{b^2}{4m^2}}
$$

$$
A(\Omega)=\frac{F_0}{\sqrt{(k-m\Omega^2)^2+b^2\Omega^2}}
$$

$$
\delta(\Omega)=\operatorname{atan2}(b\Omega,;k-m\Omega^2)
$$

The first part is transient and disappears with time.

The second part is the long-time periodic motion.

---

## 4. Numerical solution

To solve numerically, rewrite the second-order equation as two first-order equations.

Let

$$
v=\frac{dx}{dt}
$$

Then

$$
\frac{dx}{dt}=v
$$

and from the original equation

$$
m\frac{dv}{dt}+bv+kx=F_0\cos(\Omega t)
$$

so

$$
\frac{dv}{dt}=\frac{F_0\cos(\Omega t)-bv-kx}{m}
$$

Therefore, the system becomes

$$
\frac{dx}{dt}=v
$$

$$
\frac{dv}{dt}=\frac{F_0\cos(\Omega t)-bv-kx}{m}
$$

This can be solved numerically with Euler, Euler-Cromer, or RK4.

---

### 4.1 Simple Euler method

If the time step is $\Delta t$, then

$$
x_{n+1}=x_n+v_n\Delta t
$$

$$
v_{n+1}=v_n+\frac{F_0\cos(\Omega t_n)-bv_n-kx_n}{m}\Delta t
$$

This gives an approximate solution.

A better method is RK4, which is more accurate.

---

## 5. Investigate the steady-state amplitude as a function of $\Omega$

The steady-state amplitude is

$$
A(\Omega)=\frac{F_0}{\sqrt{(k-m\Omega^2)^2+b^2\Omega^2}}
$$

We now study how this depends on the driving frequency.

---

### 5.1 Low frequency

If $\Omega\to 0$, then

$$
A(0)=\frac{F_0}{k}
$$

So at very low driving frequency, the mass almost follows the force statically.

---

### 5.2 Very high frequency

If $\Omega$ becomes very large, then the term $m\Omega^2$ dominates:

$$
A(\Omega)\approx \frac{F_0}{m\Omega^2}
$$

So the amplitude becomes small.

That means the mass cannot keep up with a very rapidly changing force.

---

### 5.3 Near resonance

The amplitude becomes large when the denominator is smallest.

So resonance occurs near the frequency where

$$
(k-m\Omega^2)^2+b^2\Omega^2
$$

is minimal.

For weak damping, resonance is close to the natural frequency

$$
\omega_0=\sqrt{\frac{k}{m}}
$$

More exactly, the displacement amplitude has its maximum at

$$
\boxed{
\Omega_{\text{res}}=\sqrt{\frac{k}{m}-\frac{b^2}{2m^2}}
}
$$

provided the damping is not too large.

---

## 6. Resonance curve

The **resonance curve** is the graph of

$$
A(\Omega)
$$

versus

$$
\Omega
$$

That is,

$$
A(\Omega)=\frac{F_0}{\sqrt{(k-m\Omega^2)^2+b^2\Omega^2}}
$$

This curve typically has:

* small amplitude at low $\Omega$,
* a peak near resonance,
* then decreasing amplitude at large $\Omega$.

If damping $b$ is small, the peak is high and sharp.

If damping $b$ is large, the peak is lower and broader.

---

## 7. Investigate the phase shift

The phase shift is

$$
\delta(\Omega)=\operatorname{atan2}(b\Omega,;k-m\Omega^2)
$$

Let us understand it physically.

---

### 7.1 Low frequency

When $\Omega$ is very small, $k-m\Omega^2\approx k>0$.

So

$$
\delta\approx 0
$$

This means the displacement is almost in phase with the force.

The mass moves almost together with the driving force.

---

### 7.2 At resonance

Near resonance, $k-m\Omega^2\approx 0$.

Then

$$
\tan\delta \to \infty
$$

so

$$
\delta\approx \frac{\pi}{2}
$$

Thus at resonance, the displacement lags the force by about $90^\circ$.

---

### 7.3 High frequency

When $\Omega$ is very large, $k-m\Omega^2<0$ and large in magnitude.

Then the phase shift approaches

$$
\delta\to \pi
$$

So at high frequency, the displacement is almost opposite in phase to the force.

---

## 8. Interpretation of resonance

Resonance happens when the driving frequency is close to the system’s natural frequency.

Then the external force adds energy very efficiently to the oscillator.

As a result, the oscillation amplitude becomes large.

Important facts:

* without damping, the amplitude would become extremely large at resonance,
* with damping, the amplitude stays finite,
* stronger damping reduces the resonance peak.

So resonance is the condition of strongest response of the oscillator to periodic forcing.

---

## 9. Example with numerical values

To make the problem concrete, let us choose

$$
m=1\ \text{kg},\qquad b=0.4\ \text{N·s/m},\qquad k=9\ \text{N/m},\qquad F_0=1\ \text{N}
$$

Then

$$
\omega_0=\sqrt{\frac{k}{m}}=\sqrt{9}=3\ \text{rad/s}
$$

So the natural angular frequency is

$$
\omega_0=3\ \text{rad/s}
$$

The resonance frequency is approximately

$$
\Omega_{\text{res}}=\sqrt{\frac{k}{m}-\frac{b^2}{2m^2}}
$$

Substitute the values:

$$
\Omega_{\text{res}}=\sqrt{9-\frac{0.4^2}{2}}
$$

$$
\Omega_{\text{res}}=\sqrt{9-0.08}
$$

$$
\Omega_{\text{res}}=\sqrt{8.92}
$$

$$
\Omega_{\text{res}}\approx 2.99\ \text{rad/s}
$$

So resonance occurs very close to

$$
\Omega\approx 3\ \text{rad/s}
$$

because the damping is small.

---

## 10. Final answers for Problem 7

### Analytical solution

The full solution is

$$
x(t)=x_h(t)+x_p(t)
$$

with

$$
x_h(t)=e^{-\frac{b}{2m}t}\left(C_1\cos(\omega_d t)+C_2\sin(\omega_d t)\right)
$$

$$
\omega_d=\sqrt{\frac{k}{m}-\frac{b^2}{4m^2}}
$$

and steady-state part

$$
x_p(t)=A(\Omega)\cos(\Omega t-\delta)
$$

where

$$
\boxed{
A(\Omega)=\frac{F_0}{\sqrt{(k-m\Omega^2)^2+b^2\Omega^2}}
}
$$

and

$$
\boxed{
\delta(\Omega)=\operatorname{atan2}(b\Omega,;k-m\Omega^2)
}
$$

---

### Numerical system

The numerical system is

$$
\frac{dx}{dt}=v
$$

$$
\frac{dv}{dt}=\frac{F_0\cos(\Omega t)-bv-kx}{m}
$$

and can be solved with Euler or RK4.

---

### Resonance

The resonance curve is the plot of

$$
A(\Omega)
$$

against

$$
\Omega
$$

The amplitude is maximal near

$$
\boxed{
\Omega_{\text{res}}=\sqrt{\frac{k}{m}-\frac{b^2}{2m^2}}
}
$$

for weak damping.

---

### Phase shift

The phase shift satisfies

$$
\boxed{
\tan\delta=\frac{b\Omega}{k-m\Omega^2}
}
$$

So:

* for small $\Omega$, $\delta\approx 0$,
* near resonance, $\delta\approx \dfrac{\pi}{2}$,
* for large $\Omega$, $\delta\approx \pi$.

---

## 11. HTML requirement – interactive change of forcing frequency

Below is a complete simple HTML file.
It lets you:

* change the forcing frequency $\Omega$ with a slider,
* solve the equation numerically,
* show the time evolution,
* show the resonance curve,
* show the phase shift.

You can save it as `forced_oscillator.html` and open it in a browser.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Forced Oscillator and Resonance</title>
  <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 20px;
      background: #f7f7f7;
      color: #222;
    }
    h1, h2 {
      margin-bottom: 8px;
    }
    .controls, .info {
      background: white;
      padding: 15px;
      border-radius: 10px;
      margin-bottom: 20px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.08);
    }
    label {
      display: block;
      margin-top: 10px;
    }
    input[type="range"] {
      width: 300px;
    }
    .value {
      font-weight: bold;
      color: #0b57d0;
    }
    canvas {
      background: white;
      border-radius: 10px;
      padding: 10px;
      margin-bottom: 20px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.08);
    }
    .row {
      display: flex;
      gap: 20px;
      flex-wrap: wrap;
    }
    .card {
      flex: 1 1 300px;
    }
  </style>
</head>
<body>
  <h1>Forced Oscillator and Resonance</h1>

  <div class="controls">
    <h2>Parameters</h2>

    <label>Mass m = <span class="value" id="mVal">1.0</span></label>
    <input type="range" id="m" min="0.5" max="5" step="0.1" value="1.0">

    <label>Damping b = <span class="value" id="bVal">0.4</span></label>
    <input type="range" id="b" min="0.0" max="3" step="0.05" value="0.4">

    <label>Spring constant k = <span class="value" id="kVal">9.0</span></label>
    <input type="range" id="k" min="1" max="20" step="0.1" value="9.0">

    <label>Force amplitude F₀ = <span class="value" id="F0Val">1.0</span></label>
    <input type="range" id="F0" min="0.1" max="5" step="0.1" value="1.0">

    <label>Driving frequency Ω = <span class="value" id="OmegaVal">3.0</span> rad/s</label>
    <input type="range" id="Omega" min="0.1" max="8" step="0.01" value="3.0">
  </div>

  <div class="info">
    <h2>Analytical formulas</h2>
    <p><b>Amplitude:</b> <span id="ampText"></span></p>
    <p><b>Phase shift:</b> <span id="phaseText"></span></p>
    <p><b>Natural frequency:</b> <span id="omega0Text"></span></p>
    <p><b>Resonance frequency (approx.):</b> <span id="resText"></span></p>
  </div>

  <div class="row">
    <div class="card">
      <canvas id="timeChart"></canvas>
    </div>
    <div class="card">
      <canvas id="resonanceChart"></canvas>
    </div>
  </div>

  <div class="row">
    <div class="card">
      <canvas id="phaseChart"></canvas>
    </div>
  </div>

  <script>
    const mSlider = document.getElementById("m");
    const bSlider = document.getElementById("b");
    const kSlider = document.getElementById("k");
    const F0Slider = document.getElementById("F0");
    const OmegaSlider = document.getElementById("Omega");

    const mVal = document.getElementById("mVal");
    const bVal = document.getElementById("bVal");
    const kVal = document.getElementById("kVal");
    const F0Val = document.getElementById("F0Val");
    const OmegaVal = document.getElementById("OmegaVal");

    const ampText = document.getElementById("ampText");
    const phaseText = document.getElementById("phaseText");
    const omega0Text = document.getElementById("omega0Text");
    const resText = document.getElementById("resText");

    function amplitude(m, b, k, F0, Omega) {
      return F0 / Math.sqrt((k - m * Omega * Omega) ** 2 + (b * Omega) ** 2);
    }

    function phaseShift(b, k, m, Omega) {
      return Math.atan2(b * Omega, k - m * Omega * Omega);
    }

    function rk4Solve(m, b, k, F0, Omega, tMax = 40, dt = 0.01) {
      let t = 0;
      let x = 0;
      let v = 0;

      const times = [];
      const xs = [];
      const force = [];

      function ax(t, x, v) {
        return (F0 * Math.cos(Omega * t) - b * v - k * x) / m;
      }

      while (t <= tMax) {
        times.push(t);
        xs.push(x);
        force.push(F0 * Math.cos(Omega * t));

        const k1x = v;
        const k1v = ax(t, x, v);

        const k2x = v + 0.5 * dt * k1v;
        const k2v = ax(t + 0.5 * dt, x + 0.5 * dt * k1x, v + 0.5 * dt * k1v);

        const k3x = v + 0.5 * dt * k2v;
        const k3v = ax(t + 0.5 * dt, x + 0.5 * dt * k2x, v + 0.5 * dt * k2v);

        const k4x = v + dt * k3v;
        const k4v = ax(t + dt, x + dt * k3x, v + dt * k3v);

        x += (dt / 6) * (k1x + 2 * k2x + 2 * k3x + k4x);
        v += (dt / 6) * (k1v + 2 * k2v + 2 * k3v + k4v);
        t += dt;
      }

      return { times, xs, force };
    }

    let timeChart, resonanceChart, phaseChart;

    function createCharts() {
      const ctx1 = document.getElementById("timeChart").getContext("2d");
      const ctx2 = document.getElementById("resonanceChart").getContext("2d");
      const ctx3 = document.getElementById("phaseChart").getContext("2d");

      timeChart = new Chart(ctx1, {
        type: "line",
        data: {
          labels: [],
          datasets: [
            { label: "x(t)", data: [], borderWidth: 2, pointRadius: 0 },
            { label: "F(t)", data: [], borderWidth: 2, pointRadius: 0 }
          ]
        },
        options: {
          responsive: true,
          plugins: { title: { display: true, text: "Numerical solution in time" } },
          scales: {
            x: { title: { display: true, text: "t (s)" } },
            y: { title: { display: true, text: "x(t), F(t)" } }
          }
        }
      });

      resonanceChart = new Chart(ctx2, {
        type: "line",
        data: {
          labels: [],
          datasets: [
            { label: "A(Ω)", data: [], borderWidth: 2, pointRadius: 0 },
            { label: "Current Ω", data: [], type: "scatter", pointRadius: 5 }
          ]
        },
        options: {
          responsive: true,
          plugins: { title: { display: true, text: "Resonance curve" } },
          scales: {
            x: { title: { display: true, text: "Ω (rad/s)" } },
            y: { title: { display: true, text: "Amplitude" } }
          }
        }
      });

      phaseChart = new Chart(ctx3, {
        type: "line",
        data: {
          labels: [],
          datasets: [
            { label: "δ(Ω)", data: [], borderWidth: 2, pointRadius: 0 },
            { label: "Current Ω", data: [], type: "scatter", pointRadius: 5 }
          ]
        },
        options: {
          responsive: true,
          plugins: { title: { display: true, text: "Phase shift" } },
          scales: {
            x: { title: { display: true, text: "Ω (rad/s)" } },
            y: { title: { display: true, text: "δ (rad)" } }
          }
        }
      });
    }

    function updateAll() {
      const m = parseFloat(mSlider.value);
      const b = parseFloat(bSlider.value);
      const k = parseFloat(kSlider.value);
      const F0 = parseFloat(F0Slider.value);
      const Omega = parseFloat(OmegaSlider.value);

      mVal.textContent = m.toFixed(2);
      bVal.textContent = b.toFixed(2);
      kVal.textContent = k.toFixed(2);
      F0Val.textContent = F0.toFixed(2);
      OmegaVal.textContent = Omega.toFixed(2);

      const A = amplitude(m, b, k, F0, Omega);
      const delta = phaseShift(b, k, m, Omega);
      const omega0 = Math.sqrt(k / m);

      let omegaRes = NaN;
      const inside = k / m - (b * b) / (2 * m * m);
      if (inside > 0) omegaRes = Math.sqrt(inside);

      ampText.textContent = `${A.toFixed(4)} m`;
      phaseText.textContent = `${delta.toFixed(4)} rad = ${(delta * 180 / Math.PI).toFixed(2)}°`;
      omega0Text.textContent = `${omega0.toFixed(4)} rad/s`;

      if (isNaN(omegaRes)) {
        resText.textContent = "No clear resonance peak for this damping";
      } else {
        resText.textContent = `${omegaRes.toFixed(4)} rad/s`;
      }

      const sol = rk4Solve(m, b, k, F0, Omega);
      timeChart.data.labels = sol.times;
      timeChart.data.datasets[0].data = sol.xs;
      timeChart.data.datasets[1].data = sol.force;
      timeChart.update();

      const Omin = 0.05;
      const Omax = 8.0;
      const n = 400;
      const Olist = [];
      const Alist = [];
      const Dlist = [];

      for (let i = 0; i <= n; i++) {
        const Om = Omin + (Omax - Omin) * i / n;
        Olist.push(Om);
        Alist.push(amplitude(m, b, k, F0, Om));
        Dlist.push(phaseShift(b, k, m, Om));
      }

      resonanceChart.data.labels = Olist;
      resonanceChart.data.datasets[0].data = Alist;
      resonanceChart.data.datasets[1].data = [{ x: Omega, y: A }];
      resonanceChart.update();

      phaseChart.data.labels = Olist;
      phaseChart.data.datasets[0].data = Dlist;
      phaseChart.data.datasets[1].data = [{ x: Omega, y: delta }];
      phaseChart.update();
    }

    createCharts();
    updateAll();

    [mSlider, bSlider, kSlider, F0Slider, OmegaSlider].forEach(slider => {
      slider.addEventListener("input", updateAll);
    });
  </script>
</body>
</html>
```

---

## 12. Short interpretation of the HTML

In the HTML:

* the **time plot** shows the numerical solution $x(t)$,
* the **resonance curve** shows how amplitude depends on $\Omega$,
* the **phase plot** shows how the phase shift changes with $\Omega$,
* the slider lets you interactively change the forcing frequency.

So this satisfies the requirement:

**interactive change of the forcing frequency**.

---

## 13. Very short summary

The driven damped oscillator has a steady-state solution

$$
x_p(t)=A(\Omega)\cos(\Omega t-\delta)
$$

with amplitude

$$
A(\Omega)=\frac{F_0}{\sqrt{(k-m\Omega^2)^2+b^2\Omega^2}}
$$

and phase shift

$$
\delta(\Omega)=\operatorname{atan2}(b\Omega,;k-m\Omega^2)
$$

The amplitude becomes largest near the natural frequency, producing **resonance**.

---

I can also turn this into a polished **report-style version** matching your formatting even more closely, with section numbering and cleaner final wording.
