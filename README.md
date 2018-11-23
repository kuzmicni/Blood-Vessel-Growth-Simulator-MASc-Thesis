# Agent-based-modelling
The blood vessel growth models are built using Microvessel Chaste which is an open library for spatial modelling of vascularized tissues. The library allows for custom agent-based models to be created by interfacing established parallel linear algebra, ODE solvers, and visualization packages. 

Our models are of the off-lattice type which in contrast to the classical cell-automaton models do not use a discrete grid and are derived from the equation of motion (m_i*r_i''=-c*r_i'+sum(F_ij)), where each cell is initially assigned an initial r_i position, the guiding force F_ij from the neighbouring sites is a function of tumour growth factor gradient and cellular states, and diffusion of tumour growth factor is modelled by a steady-state diffusion equation. 

We assume that viscous forces dominate inertial forces and approximate the system as the first-order (c*r_i'=sum(F_ij)) which enables us to solve the system using the forward Euler scheme and solve for the cell position r_i(t) as follows: 
r_i(t_n+1)=r_(i)+(dt/c)*(sum(F_ij)).
