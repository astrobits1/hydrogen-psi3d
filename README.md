<h1>Hydrogen Wavefunction Computation and Orbital Generation</h1>

<h2>Motivation & Overview</h2>
This project was the result of my attempt to computationally visualize atomic orbitals in 3D using the wavefunction alone along with its probability density measures. <br>
<br>
All the computation was done by implementing all component functions (Legendre, Laguerre Polynomials for radial and angular components) directly from their mathematical expressions by using sequence based closed forms that could be computationally evaluated.<br>
Various plots for different quantum numbers were obtained by plotting the obtained probability densities.<br>

<h2>Method</h2>

* Electron wave function $\psi_{n, l, m_{l}}(r, \theta, \phi)$ was obtained by computing $R_{n, l}(r)$ (radial) and $Y_{l, m_l}(\theta, \phi)$ (angular) components individually.
* Probability density function for orbital with certain quantum numbers $n, l, m_l$ was resolved using $|\psi(r, \theta, \phi)|^2$ and was then sampled in 3D space around origin
spherically.
* Normalised probability values were then plotted as granular points until probability integral gave sufficiently high number (>0.97).
* Sign of $\psi(r, \theta, \phi)$ was used to assign colour gradient and transparency to points, blue being `+` and red being `-`.
* For $m \neq 0$, linear combination was done for $+m$ and $-m$ angular wave functions to obtain complete wavefunction for symmetric orbitals.
* Normalization was handled for radial and angular components, and verified by integration.

<h2>Tools and Libraries</h2>

* Python (3.12.12)
* Plotly (5.24.1)
* Matplotlib
* NumPy

<h2>Renders</h2>

| | | |
:---:|:---:|:---:
<img src="output/1s.png" width="100%"> <br> | <img src="output/2pz.png" width="100%"/> <br> | <img src="output/3dxz.png" width="100%"/> <br>
<img src="output/3dx2y2.png" width="100%"> <br> | <img src="output/4f1.png" width="100%"/> <br> | <img src="output/4f3.png" width="100%"/> <br>
<img src="output/5g2.png" width="100%"> <br> | <img src="output/5g4.png" width="100%"/> <br> | <img src="output/5g5.png" width="320" height="275"/> <br>
<img src="output/op1.png" width="100%"> <br> | <img src="output/op2.png" width="100%"/> <br> | <img src="output/op3.png" width="100%"/>

<h4>Bonus: Hypothetical higher orbital render (10l) </h3>

| | | |
:---:|:---:|:---:
<img src="output/10l6.png" width="100%"> <br> | <img src="output/10l7.png" width="100%"/> <br> | <img src="output/op4.png" width="100%"/> <br>
