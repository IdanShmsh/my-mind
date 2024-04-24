The Schrödinger Equation, which takes the form:
$$\hat{E}\Psi(\vec{x},t)=\hat{H}\Psi(\vec{x},t)$$
Or the more expanded form:
$$-i\hbar\frac{\partial}{\partial{t}}\Psi(\vec{x},t)=(-\frac{\hbar^2}{2m}\frac{\partial^2}{\partial{x}^2}+\hat{V})\Psi(\vec{x},t)$$

Is the most basic comprehensive description of the quantum mechanical world and the behavior of the mathematics describing it.

It governs the behavior of the wave function of a single eigenstate by introducing classical mechanics in conjunction with the operators we use to perform measurements on the wave function of a system.

The Schrödinger Equation revolves around the idea that the total energy of a system is the sum of its kinetic energy and potential energy - governed by the [[Mechanical Energy Equation]]:
$$E=T+V$$
To be a quantum mechanical equation, which can describe quantum mechanical phenomena, it needs to describe the behavior of the wave function of a system, and through it, the classical relations that this idea provides.

To do so, let's consider the momentum and energy operators:
$$\hat{E}=-i\hbar\frac{\partial}{{\partial}t}$$
$$\hat{p}=-i\hbar\frac{\partial}{{\partial}x}$$
As shown in the note about the [[Wave Function]] they implement the relationships:
$$\hat{E}\Psi(\vec{x},t)=E\Psi(\vec{x},t)$$
$$\hat{p}\Psi(\vec{x},t)=p\Psi(\vec{x},t)$$

In addition, we'll consider some additional operator $\hat{V}$ which implements:
$$\hat{V}\Psi(\vec{x},t)=V(\vec{x},t)\Psi(\vec{x},t)$$
Where $V(\vec{x},t)$ is the potential energy acting on the state at every point in time and space. This operator doesn't have a specific global definition like $\hat{E}$ and $\hat{p}$ have since it is highly specific to the formation of the system being studied.

In addition, we'll consider the expression that calculates the kinetic energy of a system given its momentum:
$$T=\frac{p^2}{2m}$$
Coming back to the mechanical energy equation, we can very easily perform a few algebraic transformations:

First, we'll substitute $T$ for $\frac{p^2}{2m}$:
$$E=\frac{p^2}{2m}+V$$
Next, we'll multiply everything by $\Psi(\vec{x},t)$
$$E\Psi(\vec{x},t)=\frac{p^2}{2m}\Psi(\vec{x},t)+V\Psi(\vec{x},t)$$
Quickly, let's consider the result of operating with $\hat{p}^2$ on $\Psi(\vec{x},t)$:
$$\hat{p}^2\Psi(\vec{x},t)$$
$$=\hat{p}\space\hat{p}\Psi(\vec{x},t)$$
$$=\hat{p}\space{p}\Psi(\vec{x},t)$$
$$={p}\space\hat{p}\Psi(\vec{x},t)$$
$$={p}\space\hat{p}\Psi(\vec{x},t)$$
$$=p^2\Psi(\vec{x},t)$$
showing that:
$$\hat{p}^2\Psi(\vec{x},t)=p^2\Psi(\vec{x},t)$$
> Note that this algebraic statement can only be done given that $\Psi(\vec{x},t)$ is an eigenstate.


Finally, we'll substitute $E\Psi(\vec{x},t)$, $p^2\Psi(\vec{x},t)$ and $V\Psi(\vec{x},t)$ with their operator counterparts as shown above:
$$\hat{E}\Psi(\vec{x},t)=E\Psi(\vec{x},t)$$
$$\hat{p}^2\Psi(\vec{x},t)=p^2\Psi(\vec{x},t)$$
$$\hat{V}\Psi(\vec{x},t)=V(\vec{x},t)\Psi(\vec{x},t)$$
Arriving at our final expression of the form:
$$\hat{E}\Psi(\vec{x},t)=\frac{\hat{p}^2}{2m}\Psi(\vec{x},t)+\hat{V}\Psi(\vec{x},t)$$
Substituting the definitions of the operators back in:
$$\hat{E}=-i\hbar\frac{\partial}{{\partial}t}$$
$$\hat{p}^2=(-i\hbar\frac{\partial}{{\partial}x})^2=-\hbar^2\frac{\partial^2}{\partial{x}^2}$$
We get:
$$-i\hbar\frac{\partial}{\partial{t}}\Psi(\vec{x},t)=-\frac{\hbar^2}{2m}\frac{\partial^2}{\partial{x}^2}\Psi(\vec{x},t)+\hat{V}\Psi(\vec{x},t)$$
Finally factoring out $\Psi(\vec{x},t)$:
$$-i\hbar\frac{\partial}{\partial{t}}\Psi(\vec{x},t)=(-\frac{\hbar^2}{2m}\frac{\partial^2}{\partial{x}^2}+\hat{V})\Psi(\vec{x},t)$$
This is the Schrödinger Equation in all its glory.

If we consider:
$$\hat{H}=\hat{T}+\hat{V}$$
$$\hat{H}=-\frac{\hbar^2}{2m}\frac{\partial^2}{\partial{x}^2}+\hat{V}$$
We can conclude:
$$\hat{E}\Psi(\vec{x},t)=\hat{H}\Psi(\vec{x},t)$$

#### Summary
The Schrödinger Equation implements the rules governed by the [[Mechanical Energy Equation]] by acting on the wave function of the eigenstate of a system, this is what makes it quantum mechanical.
It does so by substituting the total energy, kinetic energy and potential energy with the quantum operators that measure these values when acted on a state.