---
layout: post
title: "Quantum Mechanics: The Schrodinger Equation"
date: 2026-03-15
categories: notes quantum
mathjax: true
author: Kumar Azad
---

## 1. The Time-Dependent Schrodinger Equation (TDSE)

The central equation of non-relativistic quantum mechanics:

$$i\hbar \frac{\partial \Psi}{\partial t} = \hat{H}\Psi$$

For a single particle of mass $m$ in a potential $V(\mathbf{r}, t)$:

$$i\hbar \frac{\partial \Psi}{\partial t} = \left[ -\frac{\hbar^2}{2m} \nabla^2 + V(\mathbf{r}, t) \right] \Psi$$

In 1D:

$$i\hbar \frac{\partial \Psi}{\partial t} = -\frac{\hbar^2}{2m} \frac{\partial^2 \Psi}{\partial x^2} + V(x,t)\Psi$$

---

## 2. Separation of Variables & the TISE

For time-independent potentials $V = V(x)$, we separate $\Psi(x,t) = \psi(x) \cdot T(t)$.

The time part solves trivially:

$$T(t) = e^{-iEt/\hbar}$$

The spatial part satisfies the **Time-Independent Schrodinger Equation (TISE)**:

$$\hat{H}\psi = E\psi \quad \Longrightarrow \quad -\frac{\hbar^2}{2m}\frac{d^2\psi}{dx^2} + V(x)\psi = E\psi$$

The full solution is a superposition:

$$\Psi(x,t) = \sum_n c_n \psi_n(x)\, e^{-iE_n t/\hbar}$$

---

## 3. The Infinite Square Well

**Setup:** $V(x) = 0$ for $0 \le x \le L$, $V = \infty$ otherwise.

Boundary conditions force $\psi(0) = \psi(L) = 0$.

### Stationary States

$$\boxed{\psi_n(x) = \sqrt{\frac{2}{L}} \sin\left(\frac{n\pi x}{L}\right)}, \quad n = 1, 2, 3, \ldots$$

### Energy Eigenvalues

$$\boxed{E_n = \frac{n^2 \pi^2 \hbar^2}{2mL^2} = n^2 E_1}$$

The **ground state energy** $E_1 \neq 0$ is the **zero-point energy**, a consequence of the Heisenberg uncertainty principle:

$$\Delta x \cdot \Delta p \ge \frac{\hbar}{2}$$

### Orthonormality

$$\int_0^L \psi_m^*(x)\, \psi_n(x)\, dx = \delta_{mn}$$

---

## 4. The Quantum Harmonic Oscillator

**Potential:** $V(x) = \frac{1}{2}m\omega^2 x^2$

### Algebraic Method (Ladder Operators)

Define:

$$\hat{a}_{\pm} = \frac{1}{\sqrt{2\hbar m\omega}}\left(\mp ip + m\omega x\right)$$

The Hamiltonian becomes:

$$\hat{H} = \hbar\omega\left(\hat{a}_+\hat{a}_- + \frac{1}{2}\right)$$

### Energy Levels

$$\boxed{E_n = \hbar\omega\left(n + \frac{1}{2}\right)}, \quad n = 0, 1, 2, \ldots$$

### Ground State Wavefunction

$$\psi_0(x) = \left(\frac{m\omega}{\pi\hbar}\right)^{1/4} \exp\left(-\frac{m\omega}{2\hbar}x^2\right)$$

---

## 5. Interpretation: The Born Rule

The wavefunction $\Psi(x,t)$ is a **probability amplitude**. The probability of finding the particle between $x$ and $x + dx$ at time $t$ is:

$$P(x,t)\,dx = |\Psi(x,t)|^2\,dx
$$

Normalization requires:

$$\int_{-\infty}^{\infty} |\Psi(x,t)|^2\,dx = 1$$

---

## 6. Expectation Values

For any observable $\hat{Q}(x, p)$:

$$\langle Q \rangle = \int \Psi^* \hat{Q}\left(x, \frac{\hbar}{i}\frac{\partial}{\partial x}\right) \Psi\, dx$$

For position and momentum:

$$\langle x \rangle = \int |\Psi|^2 x\, dx, \qquad \langle p \rangle = \int \Psi^* \frac{\hbar}{i}\frac{\partial \Psi}{\partial x}\, dx$$

---

*Back to [Physics Notes](/quantumscribe.github.io/notes/)*
