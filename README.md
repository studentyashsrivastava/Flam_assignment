# Recovering Hidden Parameters of a Rotated Parametric Curve

Recover the unknown parameters of a rotated, exponentially modulated parametric curve using **only an unordered set of $(x,y)$ points**. The project combines geometric reasoning, Principal Component Analysis (PCA), and nonlinear least-squares optimization to recover the original curve without knowing the parameterization of any point.

---

# Final Result

The recovered parameters are

| Parameter                    |    Value |
| ---------------------------- | -------: |
| Rotation ($\theta$)          |  **30°** |
| Growth Parameter ($M$)       | **0.03** |
| Horizontal Translation ($X$) |   **55** |

## Interactive Visualization
The recovered parameters give the final latex string along with the Desmos link.

$$
\left(
t\cos(0.523599)
-e^{0.03|t|}\sin(0.3t)\sin(0.523599)+55,
;
42+t\sin(0.523599)
+e^{0.03|t|}\sin(0.3t)\cos(0.523599)
\right)
$$

for $t\in[6,60]$.

**Desmos:** **https://www.desmos.com/calculator/huxiiwkftc**

# Problem Statement

The dataset points are generated from the parametric equations

$$
x(t)=t\cos\theta-e^{M|t|}\sin(0.3t)\sin\theta+X
$$

$$
y(t)=42+t\sin\theta+e^{M|t|}\sin(0.3t)\cos\theta
$$

where

* $t\in[6,60]$
* $\theta$ is an unknown rotation angle
* $M$ controls exponential growth
* $X$ is an unknown horizontal translation

Only the $(x,y)$ coordinates are given.

The points are **unordered** (as shown by graph in notebook), meaning the original parameter value $t$ corresponding to each point is completely unknown.

The objective is to recover

* $\theta$
* $M$
* $X$

---