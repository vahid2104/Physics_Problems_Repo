## Problem 5 – Superposition of waves, beats, and group velocity

Two harmonic waves are given:

$$
y_1(x,t)=A\sin(kx-\omega t)
$$

$$
y_2(x,t)=A\sin(kx-(\omega+\Delta\omega)t)
$$

We need to determine:

* the resultant wave (y=y_1+y_2),
* reduce it to product form,
* find the beat frequency and beat period at (x=0),
* explain the physical meaning of the carrier and the envelope,
* and give Python/HTML/JS code to visualize the waves and their superposition.

---

## 1. Add the two waves

We start from

$$
y=y_1+y_2
$$

So

$$
y=A\sin(kx-\omega t)+A\sin(kx-(\omega+\Delta\omega)t)
$$

Factor out (A):

$$
y=A\left[\sin(kx-\omega t)+\sin(kx-(\omega+\Delta\omega)t)\right]
$$

Now we use the trigonometric identity

$$
\sin\alpha+\sin\beta=2\sin\left(\frac{\alpha+\beta}{2}\right)\cos\left(\frac{\alpha-\beta}{2}\right)
$$

Let

$$
\alpha = kx-\omega t
$$

and

$$
\beta = kx-(\omega+\Delta\omega)t
$$

---

## 2. Compute the average and the difference

First compute

$$
\frac{\alpha+\beta}{2}
$$

Substitute:

$$
\frac{(kx-\omega t)+(kx-(\omega+\Delta\omega)t)}{2}
$$

$$
=\frac{2kx-(2\omega+\Delta\omega)t}{2}
$$

$$
=kx-\left(\omega+\frac{\Delta\omega}{2}\right)t
$$

Now compute

$$
\frac{\alpha-\beta}{2}
$$

Substitute:

$$
\frac{(kx-\omega t)-\left(kx-(\omega+\Delta\omega)t\right)}{2}
$$

The (kx) terms cancel:

$$
=\frac{-\omega t+\omega t+\Delta\omega, t}{2}
$$

$$
=\frac{\Delta\omega, t}{2}
$$

---

## 3. Write the resultant in product form

Using the identity:

$$
y=2A\sin\left(kx-\left(\omega+\frac{\Delta\omega}{2}\right)t\right)\cos\left(\frac{\Delta\omega}{2}t\right)
$$

So the resultant wave is

$$
\boxed{
y(x,t)=2A\sin\left(kx-\left(\omega+\frac{\Delta\omega}{2}\right)t\right)\cos\left(\frac{\Delta\omega}{2}t\right)
}
$$

---

## 4. Identify carrier and envelope

This expression has the form

$$
y=(\text{carrier})\times(\text{envelope})
$$

So:

### Carrier wave

The sine factor is

$$
\sin\left(kx-\left(\omega+\frac{\Delta\omega}{2}\right)t\right)
$$

This is the fast oscillation.

Its angular frequency is approximately the average of the two frequencies:

$$
\omega_{\text{carrier}}=\omega+\frac{\Delta\omega}{2}
$$

So the carrier describes the rapid up-and-down oscillation.

---

### Envelope

The cosine factor is

$$
\cos\left(\frac{\Delta\omega}{2}t\right)
$$

This changes much more slowly if (\Delta\omega) is small.

The total amplitude is therefore

$$
A_{\text{eff}}(t)=2A\cos\left(\frac{\Delta\omega}{2}t\right)
$$

If we want the visible amplitude, we usually take the magnitude:

$$
|A_{\text{eff}}(t)|=2A\left|\cos\left(\frac{\Delta\omega}{2}t\right)\right|
$$

So the envelope is

$$
\boxed{
\pm 2A\cos\left(\frac{\Delta\omega}{2}t\right)
}
$$

or, for the amplitude size,

$$
\boxed{
2A\left|\cos\left(\frac{\Delta\omega}{2}t\right)\right|
}
$$

---

## 5. Beat frequency at (x=0)

Now let us study the oscillation at the fixed point (x=0).

Then

$$
y_1(0,t)=A\sin(-\omega t)=-A\sin(\omega t)
$$

$$
y_2(0,t)=A\sin(-(\omega+\Delta\omega)t)=-A\sin((\omega+\Delta\omega)t)
$$

Their sum is still modulated by

$$
\cos\left(\frac{\Delta\omega}{2}t\right)
$$

The intensity of the sound or the amplitude pulses rise and fall with the beat phenomenon.

The envelope magnitude repeats whenever

$$
\left|\cos\left(\frac{\Delta\omega}{2}t\right)\right|
$$

repeats.

This happens when the argument changes by (\pi), so

$$
\frac{\Delta\omega}{2}T_{\text{beat}}=\pi
$$

Therefore,

$$
T_{\text{beat}}=\frac{2\pi}{\Delta\omega}
$$

So the beat frequency is

$$
f_{\text{beat}}=\frac{1}{T_{\text{beat}}}
=\frac{\Delta\omega}{2\pi}
$$

Thus,

$$
\boxed{
f_{\text{beat}}=\frac{\Delta\omega}{2\pi}
}
$$

and

$$
\boxed{
T_{\text{beat}}=\frac{2\pi}{\Delta\omega}
}
$$

---

## 6. Why this is called beats

The two waves have almost the same frequency.

Sometimes they reinforce each other, giving a large amplitude.

Sometimes they nearly cancel, giving a small amplitude.

So at a fixed point, the oscillation becomes:

* loud / strong,
* then weak,
* then loud again.

That repeating increase and decrease is called **beats**.

---

## 7. Physical interpretation

Let us explain the meaning in simple words.

### Envelope

The envelope tells us how the **overall amplitude** changes slowly with time.

It describes:

* when the two waves interfere constructively,
* when they interfere destructively,
* and how the amplitude grows and shrinks.

So the envelope is the slow modulation.

---

### Carrier wave

The carrier is the fast sine wave inside the envelope.

It describes the actual rapid oscillation of the medium.

So:

* the **carrier** gives the quick oscillation,
* the **envelope** gives the slow variation of amplitude.

---

## 8. About group velocity

The title mentions group velocity, so let us connect it to this result.

Here both waves have the **same** wave number (k), but different angular frequencies:

$$
y_1=A\sin(kx-\omega t), \qquad y_2=A\sin(kx-(\omega+\Delta\omega)t)
$$

Because the envelope factor is

$$
\cos\left(\frac{\Delta\omega}{2}t\right)
$$

it depends only on (t), not on (x).

That means the envelope does **not move along the (x)-axis** in this exact problem.

So for the waves exactly as given, there is no spatially moving wave packet, only temporal beats.

---

### Important note

To get a moving envelope and define a true group velocity, we usually need

$$
y_1=A\sin(kx-\omega t)
$$

$$
y_2=A\sin((k+\Delta k)x-(\omega+\Delta\omega)t)
$$

Then the envelope depends on both (x) and (t), and its speed is approximately

$$
v_g=\frac{\Delta\omega}{\Delta k}
$$

or in the limit

$$
v_g=\frac{d\omega}{dk}
$$

But for your exact formulas, the envelope only beats in time.

---

## 9. Final mathematical answers

The resultant wave is

$$
\boxed{
y(x,t)=2A\sin\left(kx-\left(\omega+\frac{\Delta\omega}{2}\right)t\right)\cos\left(\frac{\Delta\omega}{2}t\right)
}
$$

Carrier:

$$
\boxed{
\sin\left(kx-\left(\omega+\frac{\Delta\omega}{2}\right)t\right)
}
$$

Envelope:

$$
\boxed{
2A\cos\left(\frac{\Delta\omega}{2}t\right)
}
$$

Beat frequency at (x=0):

$$
\boxed{
f_{\text{beat}}=\frac{\Delta\omega}{2\pi}
}
$$

Beat period:

$$
\boxed{
T_{\text{beat}}=\frac{2\pi}{\Delta\omega}
}
$$

Physical meaning:

* the **carrier** describes the fast oscillation,
* the **envelope** describes the slow change of amplitude due to interference.

---

# 10. Python code to visualize the waves and beats

This Python code uses `matplotlib` animation.

It shows:

* wave (y_1),
* wave (y_2),
* their sum.

Since your problem has the same (k) for both waves, the envelope does not move in space; instead the whole wave gets stronger and weaker with time.

```python
import numpy as np
import matplotlib.pyplot as plt
from matplotlib.animation import FuncAnimation

# Parameters
A = 1.0
k = 2.0
omega = 8.0
delta_omega = 0.8

# Space grid
x = np.linspace(0, 4*np.pi, 1000)

# Figure
fig, ax = plt.subplots(figsize=(10, 6))
line1, = ax.plot(x, np.zeros_like(x), label='y1', linewidth=1.5)
line2, = ax.plot(x, np.zeros_like(x), label='y2', linewidth=1.5)
line_sum, = ax.plot(x, np.zeros_like(x), label='y = y1 + y2', linewidth=2.5)

ax.set_xlim(x.min(), x.max())
ax.set_ylim(-2.5*A, 2.5*A)
ax.set_xlabel('x')
ax.set_ylabel('y')
ax.set_title('Superposition of two waves: beats in time')
ax.legend()
ax.grid(True)

time_text = ax.text(0.02, 0.95, '', transform=ax.transAxes)

def update(frame):
    t = frame * 0.03

    y1 = A * np.sin(k*x - omega*t)
    y2 = A * np.sin(k*x - (omega + delta_omega)*t)
    y = y1 + y2

    line1.set_ydata(y1)
    line2.set_ydata(y2)
    line_sum.set_ydata(y)

    time_text.set_text(f"t = {t:.2f} s")
    return line1, line2, line_sum, time_text

ani = FuncAnimation(fig, update, frames=400, interval=40, blit=True)
plt.show()
```

---

# 11. HTML + JavaScript version

This version runs in a browser.

It draws:

* the first wave,
* the second wave,
* the sum.

You can save it as `beats.html` and open it in a browser.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Wave Superposition and Beats</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      background: #f4f4f4;
      margin: 20px;
    }
    canvas {
      background: white;
      border: 1px solid #ccc;
    }
  </style>
</head>
<body>
  <h2>Superposition of Two Waves – Beats</h2>
  <p>The blue and green curves are the two waves. The red curve is their sum.</p>
  <canvas id="canvas" width="900" height="450"></canvas>

  <script>
    const canvas = document.getElementById("canvas");
    const ctx = canvas.getContext("2d");

    const A = 60;               // pixel amplitude
    const k = 2.0;
    const omega = 8.0;
    const deltaOmega = 0.8;

    const width = canvas.width;
    const height = canvas.height;
    const midY = height / 2;

    let t = 0;

    function drawAxes() {
      ctx.strokeStyle = "#999";
      ctx.lineWidth = 1;

      // x-axis
      ctx.beginPath();
      ctx.moveTo(0, midY);
      ctx.lineTo(width, midY);
      ctx.stroke();

      // y-axis
      ctx.beginPath();
      ctx.moveTo(40, 0);
      ctx.lineTo(40, height);
      ctx.stroke();
    }

    function drawWave(color, func) {
      ctx.beginPath();
      ctx.strokeStyle = color;
      ctx.lineWidth = 2;

      for (let px = 0; px < width; px++) {
        let x = (px / width) * 4 * Math.PI;
        let y = func(x);
        let py = midY - y;

        if (px === 0) {
          ctx.moveTo(px, py);
        } else {
          ctx.lineTo(px, py);
        }
      }
      ctx.stroke();
    }

    function animate() {
      ctx.clearRect(0, 0, width, height);
      drawAxes();

      drawWave("blue", x => A * Math.sin(k * x - omega * t));
      drawWave("green", x => A * Math.sin(k * x - (omega + deltaOmega) * t));
      drawWave("red", x =>
        A * Math.sin(k * x - omega * t) +
        A * Math.sin(k * x - (omega + deltaOmega) * t)
      );

      ctx.fillStyle = "black";
      ctx.font = "18px Arial";
      ctx.fillText("Blue: y1, Green: y2, Red: y1 + y2", 20, 30);
      ctx.fillText("t = " + t.toFixed(2), 20, 55);

      t += 0.02;
      requestAnimationFrame(animate);
    }

    animate();
  </script>
</body>
</html>
```

---

## 12. What you will see in the animation

Because both waves have the same (k),

* the pattern in space stays sinusoidal,
* but the total amplitude changes with time,
* so the red curve becomes large, then small, then large again.

That is exactly the beat phenomenon.

---

## Final answers for Problem 5

The superposition is

$$
\boxed{
y(x,t)=2A\sin\left(kx-\left(\omega+\frac{\Delta\omega}{2}\right)t\right)\cos\left(\frac{\Delta\omega}{2}t\right)
}
$$

The **carrier wave** is

$$
\boxed{
\sin\left(kx-\left(\omega+\frac{\Delta\omega}{2}\right)t\right)
}
$$

The **envelope** is

$$
\boxed{
2A\cos\left(\frac{\Delta\omega}{2}t\right)
}
$$

At (x=0), the beat frequency is

$$
\boxed{
f_{\text{beat}}=\frac{\Delta\omega}{2\pi}
}
$$

and the beat period is

$$
\boxed{
T_{\text{beat}}=\frac{2\pi}{\Delta\omega}
}
$$

Physically:

* the **carrier** describes the fast oscillation,
* the **envelope** describes the slow variation of amplitude due to interference.

For the waves exactly as given, the envelope does **not** move in space, because it depends only on (t). A true moving envelope and group velocity require slightly different values of both (k) and (\omega).


