# Simulation of Blood vessel growth in Tumour environements
As part of researching computational biology state-of-the-art methodologies during my Master's Thesis, I was tasked with implementing an open-source library published by Oxford University to assess its potential at modelling microfluidic cell culture experiments designed to mimic actual in-vivo blood vessel growth process.

The specific framework that I focused on was Microvessel Chaste (https://jmsgrogan.github.io/MicrovesselChaste/) for spatial modelling of vascularized tissues. The library allows for custom agent-based models to be created by interfacing established linear algebra and ODE solvers with powerful visualization packages. 
![image](https://user-images.githubusercontent.com/26292532/119268967-45437e00-bbc3-11eb-9e31-78975cbcbea6.png)

I implemented an off-lattice model, which in contrast to the classical cell-automaton models, does not use a discrete grid and is derived from the equation of motion and uses chemical gradients as the driving force of motion. The goal was to focus on a single interconnecting channel in the middle of the microfluidic device (please see below) which on the left-end (blue) would contain cells representative of a blood vessel and chemicals representative of tumours on the right-end (red).

![image](https://user-images.githubusercontent.com/26292532/119289760-2e2f7b00-bc19-11eb-82a9-f11bd608befb.png)

The model was able to generate realistic blood vessel networks (as illustrated below) but due to fixed assumptions around in-vivo environment did not allow us to customize it specifically to intricate microfluidic environements. As the result, I wrote custom differential system of equations model and used actaul experiment data to enable researchers to identify optimal microfluidic device dimensions and chemical concentrations in order to reduce costs and improve the quality of their cell culture experiments.

![image](https://user-images.githubusercontent.com/26292532/119268974-52606d00-bbc3-11eb-8f9a-74629cae8df8.png)
