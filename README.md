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