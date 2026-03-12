# Problem 1 – Vectors and linear transformations

Given:

$$
\vec a=(2,-1,3), \qquad \vec b=(1,4,-2)
$$

and the matrix

$$
A=
\begin{pmatrix}
2 & 1 & 0\\
0 & 1 & -1\\
1 & 0 & 1
\end{pmatrix}
$$

We need to determine:

- the lengths \( |\vec a| \) and \( |\vec b| \),
- the normalized vector \( \hat a \),
- the dot product \( \vec a\cdot\vec b \) and the angle between the vectors,
- the cross product \( \vec a\times\vec b \) and the area of the parallelogram,
- the product \( A\vec a \),
- the determinant \( \det A \),
- whether the transformation preserves orientation.

---

## 1. Lengths of the vectors

For a vector \( (x,y,z) \), its length is

$$
|(x,y,z)|=\sqrt{x^2+y^2+z^2}
$$

### Length of \( \vec a \)

$$
|\vec a|=\sqrt{2^2+(-1)^2+3^2}
$$

$$
|\vec a|=\sqrt{4+1+9}=\sqrt{14}
$$

### Length of \( \vec b \)

$$
|\vec b|=\sqrt{1^2+4^2+(-2)^2}
$$

$$
|\vec b|=\sqrt{1+16+4}=\sqrt{21}
$$

---

## 2. Normalized vector \( \hat a \)

The normalized vector is defined by

$$
\hat a=\frac{\vec a}{|\vec a|}
$$

Substitute \( \vec a=(2,-1,3) \) and \( |\vec a|=\sqrt{14} \):

$$
\hat a=\frac{(2,-1,3)}{\sqrt{14}}
$$

Therefore:

$$
\hat a=\left(\frac{2}{\sqrt{14}},-\frac{1}{\sqrt{14}},\frac{3}{\sqrt{14}}\right)
$$

---

## 3. Dot product \( \vec a\cdot\vec b \)

The dot product is

$$
\vec a\cdot\vec b = 2\cdot 1 + (-1)\cdot 4 + 3\cdot(-2)
$$

$$
\vec a\cdot\vec b = 2-4-6=-8
$$

So:

$$
\vec a\cdot\vec b=-8
$$

---

## 4. Angle between the vectors

We use the formula

$$
\vec a\cdot\vec b=|\vec a|\,|\vec b|\cos\theta
$$

Hence

$$
\cos\theta=\frac{\vec a\cdot\vec b}{|\vec a|\,|\vec b|}
$$

Substitute the known values:

$$
\cos\theta=\frac{-8}{\sqrt{14}\sqrt{21}}
$$

$$
\cos\theta=\frac{-8}{\sqrt{294}}
$$

Therefore:

$$
\theta=\arccos\left(\frac{-8}{\sqrt{294}}\right)
$$

Approximation:

$$
\theta\approx 117.9^\circ
$$

---

## 5. Cross product \( \vec a\times\vec b \)

We compute the determinant:

$$
\vec a\times\vec b=
\begin{vmatrix}
\mathbf i & \mathbf j & \mathbf k\\
2 & -1 & 3\\
1 & 4 & -2
\end{vmatrix}
$$

Expand along the first row:

$$
\vec a\times\vec b=
\mathbf i
\begin{vmatrix}
-1 & 3\\
4 & -2
\end{vmatrix}
-\mathbf j
\begin{vmatrix}
2 & 3\\
1 & -2
\end{vmatrix}
+\mathbf k
\begin{vmatrix}
2 & -1\\
1 & 4
\end{vmatrix}
$$

Now calculate each component.

### \( \mathbf i \)-component

$$
(-1)(-2)-3\cdot 4=2-12=-10
$$

### \( \mathbf j \)-component

$$
2(-2)-3(1)=-4-3=-7
$$

Because of the minus sign in front of \( \mathbf j \), this becomes

$$
-(-7)=7
$$

### \( \mathbf k \)-component

$$
2\cdot 4-(-1)\cdot 1=8+1=9
$$

Therefore:

$$
\vec a\times\vec b=(-10,7,9)
$$

---

## 6. Area of the parallelogram

The area of the parallelogram spanned by \( \vec a \) and \( \vec b \) is the magnitude of the cross product:

$$
|\vec a\times\vec b|=\sqrt{(-10)^2+7^2+9^2}
$$

$$
|\vec a\times\vec b|=\sqrt{100+49+81}=\sqrt{230}
$$

So:

$$
\text{Area}=\sqrt{230}
$$

---

## 7. Product \( A\vec a \)

We multiply the matrix by the vector:

$$
A\vec a=
\begin{pmatrix}
2 & 1 & 0\\
0 & 1 & -1\\
1 & 0 & 1
\end{pmatrix}
\begin{pmatrix}
2\\
-1\\
3
\end{pmatrix}
$$

Compute component by component:

### First component

$$
2\cdot 2+1\cdot(-1)+0\cdot 3=4-1=3
$$

### Second component

$$
0\cdot 2+1\cdot(-1)+(-1)\cdot 3=-1-3=-4
$$

### Third component

$$
1\cdot 2+0\cdot(-1)+1\cdot 3=2+3=5
$$

Therefore:

$$
A\vec a=(3,-4,5)
$$

---

## 8. Determinant of \( A \)

We calculate

$$
\det A=
\begin{vmatrix}
2 & 1 & 0\\
0 & 1 & -1\\
1 & 0 & 1
\end{vmatrix}
$$

Expand along the first row:

$$
\det A=
2\begin{vmatrix}
1 & -1\\
0 & 1
\end{vmatrix}
-1\begin{vmatrix}
0 & -1\\
1 & 1
\end{vmatrix}
+0\begin{vmatrix}
0 & 1\\
1 & 0
\end{vmatrix}
$$

Now compute the minors.

### First minor

$$
\begin{vmatrix}
1 & -1\\
0 & 1
\end{vmatrix}
=1\cdot 1-(-1)\cdot 0=1
$$

### Second minor

$$
\begin{vmatrix}
0 & -1\\
1 & 1
\end{vmatrix}
=0\cdot 1-(-1)\cdot 1=1
$$

So:

$$
\det A=2\cdot 1-1\cdot 1+0=1
$$

Therefore:

$$
\det A=1
$$

---

## 9. Orientation of the transformation

A linear transformation preserves orientation if its determinant is positive.

Since

$$
\det A=1>0
$$

the transformation preserves orientation.

---

## Final answers for Problem 1

$$
|\vec a|=\sqrt{14}, \qquad |\vec b|=\sqrt{21}
$$

$$
\hat a=\left(\frac{2}{\sqrt{14}},-\frac{1}{\sqrt{14}},\frac{3}{\sqrt{14}}\right)
$$

$$
\vec a\cdot\vec b=-8
$$

$$
\theta=\arccos\left(\frac{-8}{\sqrt{294}}\right)\approx 117.9^\circ
$$

$$
\vec a\times\vec b=(-10,7,9)
$$

$$
\text{Area}=\sqrt{230}
$$

$$
A\vec a=(3,-4,5)
$$

$$
\det A=1
$$

The transformation preserves orientation.

---