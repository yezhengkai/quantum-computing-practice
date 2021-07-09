# quantum-computing-practice
This repository is my practice on various quantum computing toolkit.

# Basic concepts of quantum computing
## Euler's formula
$$
e^{i \theta} = cos(\theta) + i sin(\theta)
$$

$$
|e^{i \theta}|^2 = |cos(\theta) + i sin(\theta)|^2 = (cos(\theta) + i sin(\theta))(cos(\theta) - i sin(\theta)) = cos^2(\theta) + sin^2(\theta) = 1
$$

## Hermitian matrix
A square matrix $A$ is a *Hermitian matrix* if it is equal to its complex conjugate transpose
$$
A^* = \bar{A}^T = A
$$
If a Hermitian matrix $\bar{A} = A$ is real , it is a *symmetric matrix*, $A^T = A$.

## Unitary matrix
$A$ is a *unitary matrix* if its conjugate transpose is equal to its inverse
$$
A^* = A^{-1} \text{, i.e., } A^* A = I
$$

> ℹ️ In physics, especially in quantum mechanics, the Hermitian adjoint of a matrix is denoted by a dagger (†) and the equation above becomes
${\displaystyle U^{\dagger }U=UU^{\dagger }=I.}$


When a unitary matrix $\bar{A} = A$ is real, it becomes an *orthogonal matrix*, $A^T = A^{-1}$.

## Normal matrix
A square matrix $A$ is *normal* if it commutes with its conjugate transpose:
$$
A^* A = A A^*
$$
If $A^* = A^T$ is real, then $A^T A = A A^T$.

## Qubit
### Dirac notation
$$
|0\rangle ={\bigl [}{\begin{smallmatrix}1\\0\end{smallmatrix}}{\bigr ]}
$$

$$
|1\rangle ={\bigl [}{\begin{smallmatrix}0\\1\end{smallmatrix}}{\bigr ]}
$$

### State
A **pure qubit state** is a coherent **superposition** of the basis states. This means that a single qubit can be described by a **linear combination** of $|0\rangle$ and $|1\rangle$:
$$
|\psi \rangle =\alpha |0\rangle +\beta |1\rangle
$$
where $\alpha$ and $\beta$ are **probability amplitudes** and can in general both be complex numbers.

When we **measure** this qubit in the standard basis, according to the [Born rule](https://en.wikipedia.org/wiki/Born_rule), the probability of outcome $|0\rangle$  with value "0" is $|\alpha |^{2}$ and the probability of outcome $|1\rangle$ with value "1" is $|\beta |^{2}$.

Because the absolute squares of the amplitudes equate to probabilities, it follows that $\alpha$ and $\beta$ must be constrained by the equation
$$
|\alpha |^{2}+|\beta |^{2}=1.
$$

### Bolch sphere
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/6b/Bloch_sphere.svg/330px-Bloch_sphere.svg.png" style="float: right; width:20%; margin: 0% 0% 2% 2%;" >

It might, at first sight, seem that there should be four degrees of freedom in $|\psi \rangle =\alpha |0\rangle +\beta |1\rangle \,$, as $\alpha$ and $\beta$  are complex numbers with two degrees of freedom each. However, one degree of freedom is removed by the normalization constraint $|\alpha |^{2}+|\beta |^{2}=1.$. This means, with a suitable change of coordinates, one can **eliminate one of the degrees of freedom**.

One possible choice is that of [Hopf coordinates](https://en.wikipedia.org/wiki/3-sphere#Hopf_coordinates):
$$
{\begin{aligned}\alpha &=e^{i\psi }\cos {\frac {\theta }{2}},\\\beta &=e^{i(\psi +\phi )}\sin {\frac {\theta }{2}}.\end{aligned}}
$$

Additionally, for a single qubit the overall phase of the state $\psi$ has **no physically observable consequences**, so we can arbitrarily choose $\alpha$ to be real (or $\beta$ in the case that $\alpha$ is zero), leaving just two degrees of freedom:
$$
{\begin{aligned}\alpha &=\cos {\frac {\theta }{2}},\\\beta &=e^{i\phi }\sin {\frac {\theta }{2}},\end{aligned}}
$$
where ${\displaystyle e^{i\phi }}$ is the physically significant **relative phase**.

The surface of the Bloch sphere is a **two-dimensional space**, which represents the **state space** of the pure qubit states. This state space has **two local degrees of freedom**, which can be represented by the two angles $\phi$ and $\theta$.


# Learning resources
- [awesome-quantum-computing](https://github.com/desireevl/awesome-quantum-computing)
- [QOSF: Learn](https://qosf.org/learn_quantum/)
- [Frank Zickert's blogs](https://pyqml.medium.com/)


# References
- [Azure Quantum Documentation](https://docs.microsoft.com/en-us/azure/quantum/)
- [Normal, Hermitian, and unitary matrices](http://fourier.eng.hmc.edu/e161/lectures/algebra/node4.html)
- [Blog: The Qubit Phase](https://towardsdatascience.com/the-qubit-phase-b5fea2026ea)
- [Wikipedia: Unitary matrix](https://en.wikipedia.org/wiki/Unitary_matrix)
- [Wikipedia: Qubit](https://en.wikipedia.org/wiki/Qubit)
