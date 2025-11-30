# Quantum Hydrodynamic Descritpion of Astrophysical Plasma

## Abstract
A quantum hydrodynamic description of plasma is a theoretical framework that
attempts to describe the behaviour of a plasma at a macroscopic level, taking into account both
quantum mechanics and the principles of fluid dynamics. In this framework, the plasma is treated
as a collection of charged particles, such as ions and electrons, that interact with each other through
the electromagnetic force. The behaviour of the plasma is described by a set of hydrodynamic
equations, which describe the motion of the particles, their interactions, and the electromagnetic
fields that they generate. At the quantum level, the particles are treated as wave functions, and the
hydrodynamic equations are modified to include quantum effects such as wave-particle duality
and uncertainty principle. One of the key advantages of a quantum hydrodynamic description of
plasma is that it allows for a more accurate and comprehensive understanding of plasma behaviour
than classical models. This can be particularly important in fields such as astrophysical plasmas.

# B.Tech Thesis Paper

This project is based on our research work that involves a hydrodynamic description of astrophysical plasma 

You can read the paper here:  
👉 [**Quantum Hydrodynamic Description of Plasma (PDF)**](https://github.com/andreaneenu/Quantum_plasma/blob/main/Quantum_Plasma_Thesis_Paper.pdf)

## Simulation
**PIC (Particle-In-Cell System)**  

In plasma physics, the PIC method is a numerical approach that simulates a collection of charged particles that interact via external and self-induced electromagnetic fields.  
A spatial grid is used to describe the field while the particles move in continuous space.  
The field and the particle motion are solved concurrently.

This project implements a **self-consistent 1D electrostatic plasma simulation** under the following assumptions:

1. No variation in plasma and particle quantities (charge density, velocity, position, etc.) or in the electric field along the z-direction.  
2. The magnetic field is zero along the x-axis in which the particles move.  
3. Distances are restricted to the order of the **Debye length**, where charge separation occurs and charge density is non-zero.  
4. Simulation time is limited to the order of the **electron plasma frequency**, ensuring zero average current densities (no self-magnetic field).  
5. **Collisions are neglected.**

Under these conditions, **Maxwell’s equations reduce to Poisson’s equation**, which specifies the electric field distribution at any given time.

---

### ⚙️ PIC Algorithm for 1D Electrostatic Plasma Simulation

1. Initialize particle data (positions, velocities, perturbation distribution)  
2. Initialize grid (number of cells, grid length, cell spacing)  
3. **While** `t < t_max` do:  
   1. Compute particle contributions to the grid  
   2. Calculate the electric field (stored in discretized grid array)  
   3. Update forces acting on particles  
   4. Move particles to new positions  
   5. Advance time: `t → t + t_step`  
4. End loop  
5. Output particle and grid data  
6. Compute and print simulation statistics  
---
## 🧾 Acknowledgment and Copyright Notice
We used the LCPFCT routines developed by Boris, Jay P. and team at the Naval Research Lab Washington DC : [LCPFCT](https://apps.dtic.mil/sti/citations/ADA265011).
We implemented the Python wrappers for the fortran subroutines with the help of the github repo : [Scivision](https://github.com/letapk/espic1d).  
We also cross checked our results using the **ESPIC1D** code developed by [Kartik Patel](https://github.com/letapk/espic1d).  
All copyrights for the original code belong to the respective author.

The modifications and additional documentation presented here were made **solely for academic and research purposes**.  
No commercial use is intended, and full credit is given to the original developer for the base implementation.

## 📘 References for the simulation
- Birdsall, C. K., & Langdon, A. B. *Plasma Physics via Computer Simulation*, McGraw-Hill (1985).  
- Hockney, R. W., & Eastwood, J. W. *Computer Simulation Using Particles*, Taylor & Francis (1988).  

