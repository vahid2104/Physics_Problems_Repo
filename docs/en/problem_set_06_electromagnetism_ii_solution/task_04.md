# Problem 4 – Rotating loop (induction)

For a conducting loop rotating in a magnetic field, we need to calculate:

* the magnetic flux through the loop,
* the induced electromotive force,
* the amplitude of the induced EMF,
* how the amplitude depends on angular velocity,
* and the physical mechanism of EMF generation.

---

## Given data

A loop has:

$$
N=\text{number of turns}
$$

$$
S=\text{area of one turn}
$$

The magnetic field is uniform:

$$
\vec B=\text{constant}
$$

The loop rotates with angular velocity:

$$
\omega
$$

The rotation axis is perpendicular to the magnetic field.

---

# 1. Magnetic flux (\Phi(t))

Magnetic flux through one loop is defined as

$$
\Phi = \vec B \cdot \vec S
$$

Here, (\vec S) is the area vector.

The magnitude of the area vector is

$$
|\vec S|=S
$$

The direction of (\vec S) is perpendicular to the surface of the loop.

So we can write:

$$
\Phi = BS\cos\theta
$$

where (\theta) is the angle between the magnetic field (\vec B) and the area vector (\vec S).

---

## Since the loop rotates

The angle changes with time:

$$
\theta = \omega t
$$

So, for one turn:

$$
\Phi_1(t)=BS\cos(\omega t)
$$

But the loop has (N) turns, so the total magnetic flux linkage is

$$
\Phi(t)=NBS\cos(\omega t)
$$

Therefore,

$$
\boxed{\Phi(t)=NBS\cos(\omega t)}
$$

---

# 2. Induced EMF (\mathcal{E}(t))

According to Faraday’s law of electromagnetic induction:

$$
\mathcal{E}(t)=-\frac{d\Phi}{dt}
$$

We already found:

$$
\Phi(t)=NBS\cos(\omega t)
$$

Now differentiate it with respect to time:

$$
\frac{d\Phi}{dt}
================

\frac{d}{dt}\left[NBS\cos(\omega t)\right]
$$

Since (N), (B), and (S) are constants:

$$
\frac{d\Phi}{dt}
================

NBS\frac{d}{dt}\cos(\omega t)
$$

Using the derivative rule:

$$
\frac{d}{dt}\cos(\omega t)=-\omega\sin(\omega t)
$$

So,

$$
\frac{d\Phi}{dt}
================

-NBS\omega\sin(\omega t)
$$

Now use Faraday’s law:

$$
\mathcal{E}(t)=-\frac{d\Phi}{dt}
$$

$$
\mathcal{E}(t)=-[-NBS\omega\sin(\omega t)]
$$

Therefore,

$$
\mathcal{E}(t)=NBS\omega\sin(\omega t)
$$

So,

$$
\boxed{\mathcal{E}(t)=NBS\omega\sin(\omega t)}
$$

---

# 3. Amplitude of induced EMF (\mathcal{E}_0)

The induced EMF is

$$
\mathcal{E}(t)=NBS\omega\sin(\omega t)
$$

The maximum value of (\sin(\omega t)) is

$$
1
$$

So the maximum EMF is

$$
\mathcal{E}_0=NBS\omega
$$

Therefore,

$$
\boxed{\mathcal{E}_0=NBS\omega}
$$

This is called the amplitude of the induced EMF.

---

# 4. How does the amplitude depend on (\omega)?

We found:

$$
\mathcal{E}_0=NBS\omega
$$

Here, (N), (B), and (S) are constant.

So,

$$
\mathcal{E}_0 \propto \omega
$$

This means the amplitude is directly proportional to angular velocity.

If (\omega) becomes 2 times larger:

$$
\omega_{\text{new}}=2\omega
$$

then

$$
\mathcal{E}_{0,\text{new}}=NBS(2\omega)
$$

$$
\mathcal{E}_{0,\text{new}}=2NBS\omega
$$

So,

$$
\mathcal{E}_{0,\text{new}}=2\mathcal{E}_0
$$

Therefore,

$$
\boxed{\text{If angular velocity doubles, the EMF amplitude also doubles.}}
$$

---

# 5. Mechanism of EMF generation

The loop rotates inside a magnetic field.

Because of this rotation, the angle between the magnetic field (\vec B) and the loop’s area vector (\vec S) changes continuously.

So the magnetic flux changes with time:

$$
\Phi(t)=NBS\cos(\omega t)
$$

According to Faraday’s law:

$$
\mathcal{E}=-\frac{d\Phi}{dt}
$$

That means:

$$
\boxed{\text{Changing magnetic flux produces induced EMF.}}
$$

This is the basic principle of an electric generator.

---

## Important physical idea

When the loop is rotating, the magnetic flux is sometimes maximum, sometimes zero, and sometimes negative.

Because the flux changes periodically, the induced EMF also changes periodically.

So the EMF is alternating:

$$
\mathcal{E}(t)=NBS\omega\sin(\omega t)
$$

This is an AC voltage.

---

# When is the magnetic flux maximum?

Magnetic flux is

$$
\Phi(t)=NBS\cos(\omega t)
$$

Flux is maximum when

$$
\cos(\omega t)=1
$$

So,

$$
\Phi_{\max}=NBS
$$

This happens when the area vector is parallel to the magnetic field.

In simple words:

$$
\boxed{\text{Flux is maximum when the loop surface is perpendicular to the magnetic field.}}
$$

---

# When is the EMF maximum?

EMF is

$$
\mathcal{E}(t)=NBS\omega\sin(\omega t)
$$

EMF is maximum when

$$
\sin(\omega t)=1
$$

So,

$$
\mathcal{E}_{\max}=NBS\omega
$$

This happens when the magnetic flux changes most rapidly.

In simple words:

$$
\boxed{\text{EMF is maximum when the loop plane is parallel to the magnetic field.}}
$$

---

# Final answers for Problem 4

The magnetic flux is

$$
\boxed{\Phi(t)=NBS\cos(\omega t)}
$$

The induced EMF is

$$
\boxed{\mathcal{E}(t)=NBS\omega\sin(\omega t)}
$$

The EMF amplitude is

$$
\boxed{\mathcal{E}_0=NBS\omega}
$$

The amplitude depends directly on angular velocity:

$$
\boxed{\mathcal{E}_0\propto \omega}
$$

So if (\omega) increases, the EMF amplitude increases by the same factor.

The mechanism is:

$$
\boxed{\text{Rotation changes magnetic flux, and changing magnetic flux creates induced EMF.}}
$$

So this rotating loop works like a simple AC generator. ✅
