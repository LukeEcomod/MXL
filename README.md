# MXL
Convective boundary layer slab model

Simple Python-implementation of convective mixed boundary layer model. Based maily on:
Janssen & Pozzer, 2015. Geosci Model Devel. 8, 453 - 471.
Stull, 1988. Boundary layer -handbook
Matlab-code of Gaby Katul (lifting condensation level)

mxl - model code
mxl_demo - simple demonstration of MXL-model using one daytime data from Hyytiälä.

TODO:
* Nocturnal boundary layer height development OR (at minimum) initial height and scalar condentrations in the morning. Zilitinkevich, 1972. 'Equilibrium height'; discuss with Gaby
* MXL and LCL predictions: validate against Hyde soundings and ceilometer data?

* For coupling with APES MLM we need to: 
0) define constant height z at which the 'hand-shaking' of MLM and MXL occurs (50m?), 
1) MLM needs U & ustar at z as forcing; how to formulate these with MXL -approach?
2) Do we impose PAR, NIR and LW at z from external forcing, OR should we at some stage think cloud development and model radiation       budget. Same concerns U & ustar. For MXL wind budget, we need momentum flux at the surface, or use imposed ustar
3) For coupled simulations, where heat, water vapor and co2 fluxes are computed using canopy MLM, we need reasonable development of     nocturnal boundary layer. In principle, we want forcings (in particular T and LWin) to be realistic for nocturnal canopy MLM simulations. And, we need a reference volume (bl height) into / from which the canopy sources / sinks affect. The nocturnal mass / energy exchange then leads to initial conditions (theta, q, co2) at next morning.
  
