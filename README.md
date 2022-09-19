# Spectral Proper Orthogonal Decomposition
In this project, the ultimate goal is to use neural networks to predict flow features.

In the first step, a two-dimensional simulation is performed in ANSYS Fluent to resolve vortex shedding downstream of three cylinders. The flow domain is depicted below:
![Geometry](https://user-images.githubusercontent.com/72427100/191092678-b2749bdf-1e47-4d09-a7ad-60e31ad3ff8d.jpg)


The velocity components in the $x$- and $y$-directions and vorticity are sampled on a regular grid just downstream of the cylinders. The results are stored in u, v, and W.npy files:
- Domain size: 100 mm $\times$ 50 mm (in $x$- and $y$-directions respectively) \
- Number of snapshots: 640 \
- Sampling frequency: 3.25 ms \
- $Re = \frac{\rho U_{in} D}{\mu}$ ~ 300

Each of the velocity and vorticity signals can be used to perform SPOD analysis. The spod.py file (from https://github.com/mathe-lab/PySPOD) contains the function that calculate the SPOD modes.
