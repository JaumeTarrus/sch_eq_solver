# sch_eq_solver
Python program to numerically solve the schroedinger equation and obtain the spectrum of some two-body nonrelativisitic problem

The Schroedinger equation for the reduced wave function (r.w.f) is a differential equation. The solution for this differential equation, the r.w.f, diverges at r going to infinity unless the value of the energy in the equation
corresponds to one of the eigenvalues. To find these eigenvalues we scan the energies starting from some suitable value (for example the minimum of the potential if it has one). At each state we check if the r.w.f diverges for
r going to infinty. In practice we are checking that the value of the r.f.w at some large r is close to zero. We should note that since we cannot obtain the eigenvalue with exact accuracy in practice the r.f.w will always
diverge at some large r value. However, for an energy close to the eigenvalue we will observe the r.f.w to become close to zero at some r and keep close to zero for some range of r which will increase as we get closer to
the eigenvalue. Since we add constant steps of energy at some point we will corss the eigenvalue, this can be detected by the change in sign of the divergence. We checking for this every step and when it occours the step is
reduced by one order of magnitude. This loop is repeated until the value of the r.f.w at the largest r of the range of r we are otaining the numerical solution for is 10^-3 smaller than the maximum of the r.w.f in the same range.
Then we save the last energy value as the eigenenergy as well as the r.w.f and expected value of 1/r, and the kinetic energy. Excited states in the pricnipal quantum number are obtained starting from the energy of the state below.
Excited state states in the angual momentum are obtained from the same initial energy guess.

