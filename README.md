# Electron-phonon coupled cluster equations

This repository contains automatically generated equations 
for the theories presented in [this work](https://arxiv.org/abs/2009.13568)

## Ground-state coupled cluster equations

The file [epcc_equations.py](equations/epcc_equations.py) contains the equations for
three ground-state theories: ep-CCSD-1-S1, ep-CCSD-12-S1, ep-ccsd-12-S12

Note:
    - The output from the code generator has not been materially altered, though
    some formatting has been cleaned up
    - The equations compute the CC residual, the diagonal terms must be subtracted
    in order to obtain the equations for the CC iteration
    - The Fock matrix and matrix of normal modes are not assumed to be diagonal, even
    though they will usually be diagonal
    - The equations are not optimized in any way

## Equation-of-motion CC  equations for excited states
The file [eom_epcc_equations.py](equations/eom_epcc_equations.py) contains the equations for
the sigma vectors of EE, IP, and EA EOM extensions to ep-CCSD-1-S1.

Note:
    - The output from the code generator has not been materially altered, though
    some formatting has been cleaned up
    - 2 versions of each equations are shown.
        - The "\_slow" version is comes from the full expression
        - The "\_int" version use code generation separately for the pieces of the similarity-transformed
        Hamiltonian and the sigma vector in terms of those pieces.
