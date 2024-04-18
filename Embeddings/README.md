# Embeddings

Each respective file in this directory represents a different quantum image encoding representation to understand each implementation's structure and how they work. Each method is based on different image representations described by Su et al. [1].

## Flexible Representation of Quantum Images (FRQI)
Implementation in file $\textbf{\textit{FRQI.ipynb}}$ [2]

Compiles and converts color and position information of an image into a quantum state given the formula for classical image representation.

$$
\ket{I(\theta)} = \frac{1}{2^n}\sum_{i=0}^{2^{2n}-1} (cos\theta_i\ket{0} + sin\theta_i\ket{1}) \otimes \ket{i}
$$

- Color information encoding: $cos\theta_i\ket{0} + sin\theta_i\ket{1}$
- Pixel position encoding: $\ket{i}$

System needs to first be put in full superposition via the Hadamard operation except for the last qubit which is used to encode for color. Controlled rotations can be broken down into standard rotations and $CNOT$ gates.

Values of $\theta$:
- $0$ = $\textbf{black}$
- $\frac{\pi}{2}$ = $\textbf{white}$

## Novel Enhanced Quantum Repreentation (NEQR)
Implementation in file $\textbf{\textit{NEQR.ipynb}}$ [2]

Compared to FRQI, NEQR does not compile color by angle, but uses the basic state of quantum sequences to store color information encodings. NEQR stores grayscale and position information represented by

$$
\ket{I(\theta)} = \frac{1}{2^n}\sum_{y=0}^{{2^n}-1}\sum_{x=0}^{{2^n}-1} \otimes_{i=0}^{q-1} \ket{C^i_{yx}} \ket{yx}
$$

## Referenes

[1] Su J., Guo X., Liu C., Li L. (2020). $\textit{A New Trend of Quantum Image Representations}$. https://ieeexplore.ieee.org/document/9268129.

[2] IBM Qikit. (2021). $\textit{How To Start Experimenting With Quantum Image Processing}$. https://medium.com/qiskit/how-to-start-experimenting-with-quantum-image-processing-283dddcc6ba0.

