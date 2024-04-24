In [[Quantum Mechanics]], the Wave Function of a system is a mathematical representation that encodes everything that there is to know about that system.

[[Classical physics]] describes the relationships of different values that different objects "just have" (energy, momentum, position, mass, etc). In Quantum Mechanics, objects and systems are described by a wave function that not only "has values" - they are encoded in its definition and through that, their connection is embedded within its definition.
In other words, the Wave Function in Quantum Mechanics, doesn't only represent the "objects" we study like in Classical Physics, it acts as a comprehensive description for every phenomena and provides the basic connection between the values we can study about a system.

As we observe in real world experiments and measurements, the wave function is also influenced by the act of measurement itself.

Both measuring, and in-tern also manipulating the Wave Function of a system is being done using [[Quantum Operators]].

The framework of Quantum Operators acting on a Wave Function is the foundation to almost everything in the theory of Quantum Mechanics. Almost all equations in the Quantum Mechanical Framework describe the relationships between the values measured from a wave function using the corresponding Quantum Operators.
A good example is the [[Schrödinger Equation]] that implements the rules of [[Energy Conservation]] and [[Mechanical Energy Equation]] using the respective operators that measure the relevant values off of a given Wave Function, which in tern give a description of a higher level behavior of the Wave Function of a system under certain conditions.

In addition, the Wave Function implements [Uncertainty](Uncertainty Principle) and [[Super Position]] through a weighted [[Integration]] over all possible [Eigenstates](Eigenstate) and their corresponding [[Probabilities]].
As suggested by the Quantum Framework.

To showcase the implementation of Wave Functions and their Quantum Operators to describe the behavior of quantum systems and how we measure values about them, we'll discuss the 

## The Wave Function Of A Particle
The wave function of a [[Particle]] is a function that has a value in every point in space and time.
It encodes everything we can know about the particle and its behavior.

As mentioned, the Wave Function implements [[Super Position]] via integrating over all possible Eigenstates.

To discuss how the wave function encodes momentum and energy, we'll discuss the case of a single Eigenstate of a single particle.
##### The wave-function of an eigenstate
Via observations and measurements in real-life experiments we observe the following behavior:
The [[Energy]] of an Eigenstate is given by the rate of change of the state's wave function over time - the more energy this eigenstate has, the more rapidly it will change over time.
In addition, the [[Momentum]] of an eigenstate is given by the rate of change of the state's wave function over space - the more momentum this eigenstate has, the more rapidly it will change over space.
In other words:
- The Energy of the eigenstate is proportional to the frequency of the wave function.
- The Momentum of the eigenstate is proportional to the wavelength of the wave function.

A function that implements these properties, is a simple harmonic oscillator:
$$\sin(kx-{\omega}t)$$
where (via experimental observations and measurements):
$$\omega=\frac{E}{\hbar}$$
$$k=\frac{p}{\hbar}$$

This function, encodes the momentum and energy of an eigenstate in a function that behaves as a sinusoidal wave. Here, the frequency over time and space depend on the momentum and energy of the particle - just like we observe.

In the quantum mechanics framework, we expand to using complex numbers. This is because there, we can represent waves with a complex exponential, via Euler's formula:
$$e^{i\theta}=\sin(\theta)+i\cos(\theta)$$
The benefits of representing the state as a complex exponential will become apparent in the progression of this note.

To represent the same wave equation in this this framework, we just substitute $\theta$ with $kx-{\omega}t$.
This yields a final equation of the form:
$$e^{i(kx-{\omega}t)}$$
Or with the momentum and energy operators factored in place of  $k$ and $\omega$ :
$$e^{{\frac{i}{\hbar}}(px-Et)}$$

#### Measurements And Operators On The Wave Function
As mentioned, and later shown, the wave function of the eigenstate of a particle encodes the values of p and E that eigenstate possesses.

It was shown how we construct a generic eigenstate wave function given the momentum and energy of that state.
But, we can do the opposite. Given a wave equation, we can algebraically isolate these values from it, performing a measurement.

Using what we call the energy and momentum operators, we can perform these measurements on the wave function.
The energy and momentum operators are the following:
$$\hat{E}=-i\hbar\frac{\partial}{{\partial}t}$$
$$\hat{p}=-i\hbar\frac{\partial}{{\partial}x}$$
Right of the bat, we can clearly see the relation mentioned above, the linear relation between the energy and the rate of change over time, as well as the linear relation between the momentum and the rate of change over space.

To get an even deeper of an understanding, let's operate with them on the wave function of an eigenstate.

Consider the eigenstate:
$$\Psi(\vec{x},t)=e^{{\frac{i}{\hbar}}(px-Et)}$$

Operating with $\hat{E}$ on $\Psi$:
$$\hat{E}\Psi(\vec{x},t)$$
$$=-i\hbar\frac{\partial}{{\partial}t}e^{{\frac{i}{\hbar}}(px-Et)}$$
$$=-i\hbar\frac{iE}{\hbar}e^{{\frac{i}{\hbar}}(px-Et)}$$
$$=Ee^{{\frac{i}{\hbar}}(px-Et)}$$
$$=E\Psi(\vec{x},t)$$
Operating with $\hat{p}$ on $\Psi$:
$$\hat{p}\Psi(\vec{x},t)$$
$$=-i\hbar\frac{\partial}{{\partial}x}e^{{\frac{i}{\hbar}}(px-Et)}$$
$$=-i\hbar\frac{ip}{\hbar}e^{{\frac{i}{\hbar}}(px-Et)}$$
$$=pe^{{\frac{i}{\hbar}}(px-Et)}$$
$$=p\Psi(\vec{x},t)$$

We can easily see how by applying the momentum and energy operators on an eigenstate's wave function we can isolate the momentum and energy values of the eigenstate in the form of introducing a factor of these values on the state.

In addition, we can see the algebraic benefits of an eigenstate's wave function being represented by an exponential. This allows for the algebraic properties that enable us to perform the measurement operations presented above.

#### Integrating Over All Eigenstates
As discussed, the Eigenstate of a particle with a determined momentum is:
$$\psi(\vec{p},\vec{x},t)=e^{\frac{i}{h}(\vec{p}\vec{x}-Et)}$$
Which looks like a harmonic oscillator infinitely spread out over space.

Since particles never have a definite momentum state, but have a probability distribution of finding the particle at a given momentum.

Let's consider the momentum probability distribution of a given particle as a [[Gaussian Distribution]] centered at momentum $p_0$ with uncertainty (standard deviation) $\Delta{p}$:
$$\phi(\vec{p})=\frac{1}{\Delta{p}{\sqrt{2\pi}}}e^{-\frac{(\vec{p}-p_0))^2}{2\Delta{p}}}$$

The total wave function would be an integral of all momentum Eigenstates multiplied by their respective probability:
$$\Psi(\vec{x},t)=\int_{-\infty}^{\infty}\phi(\vec{p})\psi(\vec{p},\vec{x},t)\space d^3p$$

When taking into account the uncertainty in the momentum of the particle, an implementation of the [[Uncertainty Principle]] comes up.
The Wave Function, from being spread-out over all time and space for the Eigenstate of a definite momentum, becomes a localized function, a wave-packet, with non-zero values only in a small space around a certain position. Surprisingly enough, the distribution of the Wave Function over space in this case takes the shape of yet another Gaussian Distribution with a standard deviation (or uncertainty) of $\Delta{x}$.
Where the relation between $\Delta{p}$ and $\Delta{x}$ is:
$$\Delta{x}\Delta{p}\geq\frac{\hbar}{2}$$

#### Obtaining Position Probabilities
After integrating over the infinite set of Eigenstates in the way the Quantum Mechanical Framework suggests, we arrive at a single function - this is the wave function of the system.

The wave function of a particle encodes the probability distribution of finding the particle at any point in space and time. To get the probability of finding a particle in a point of space and time, we take the value of the wave function at that point, we then take its amplitude (its absolute value) and square it.

Let's consider the wave function of a particle, a function of space and time:
$$\Psi(\vec{x},t)$$
The probability of finding the particle at position $\vec{X}$ and time $T$ is given by:
$$P(\vec{X},T)=|\Psi(\vec{X},T)|^2$$

#### Summary
A quantum system can be comprehensively described by the wave function - The wave function of a system, encodes everything we can know about that system.

We can perform measurements on this function in different ways to obtain these encoded values from it, measuring them.

In classical physics, we build equations that directly link different values we can measure about a system. $E=m\frac{v^2}{2}$, $F=ma$ etc.

In quantum mechanics we construct equations that govern the behavior and shape of this wave function, which in tern describe the same relations. Again, through the wave function, instead of doing so directly.