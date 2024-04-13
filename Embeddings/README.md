# Embeddings

## Flexible Representation of Quantum Images (FRQI)
Implementation in file $``\textbf{\textit{FRQI.ipynb}}"$

Compiles and coonverts color and position information of an image into a quantum state given the formula for classical image representation.
$$
\ket{I(\theta)} = \frac{1}{2^n}\sum_{i=0}^{2^{2n}-1} (cos\theta_i\ket{0} + sin\theta_i\ket{1}) \otimes \ket{i}
$$

- Color information encoding: $cos\theta_i\ket{0} + sin\theta_i\ket{1}$
- Pixel position encoding: $\ket{i}$

System needs to first be put in full superposition via the Hadamard operation except for the last qubit which is used to encode for color. Controlled rotations can be broken dwn into standard rotations and $CNOT$ gates.

Values of $\theta$:
- $0$ = $\textbf{black}$
- $\frac{\pi}{2}$ = $\textbf{white}$


## Referenes

https://medium.com/qiskit/how-to-start-experimenting-with-quantum-image-processing-283dddcc6ba0

https://ieeexplore.ieee.org/document/9268129