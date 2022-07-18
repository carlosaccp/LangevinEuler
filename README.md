# Numerical Langevin

The aim of this project is to numerically compute the Langevin map, which is given by the PDE:

$$
\frac{\partial S_x(t)}{\partial t} = B_t S_x(t)
$$

Fixing $x$ we can turn this into an ODE:

$$
\frac{dS_x(t)}{dt} = B_t S_x(t) ; \quad S_x(0) = x
$$

Which can be solved using Forward Euler. We also numerically compute the derivative of the Langevin map, $DS_x(t) = DS(t)$ ($DS$ is independent of $x$) by solving the following ODE:

$$
\frac{d[DS(t)]}{dt} = B_t [DS_x(t)] ; \quad DS(0) = \text{Id}
$$

This is also solved using Forward Euler.

All of the code is written in Julia and relies on the `LinearAlgebra.jl` and `GridInterpolations.jl` libraries.
