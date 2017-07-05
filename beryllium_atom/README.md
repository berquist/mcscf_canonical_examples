# Beryllium atom

The default aufbau-type closed-shell ground-state electron configuration is (1s)^{2}(2s)^{2}. However, it's pretty well-known that even the bare atom shows multiconfigurational behavior, with occupation of the (1s)^{2}(2s)^{1}(2p)^{1} and (1s)^{2}(2s)^{0}(2s)^{2} configurations, both of which are captured qualitatively by CAS(2,4). This should be large enough, since the 2p orbitals are triply-degenerate (they are atomic).

See the ORCA 4.0.0 manual starting on page 99 (section 8.1.7.2).

- `casscf_2_4_singlet_ss_0`: This is the example from the ORCA manual. Do everything in one go, no multi-step calculations.

> How did we know how to put the 2s and 2p orbitals in the active space? The answer is - WE DID NOT KNOW! In this case it was "good luck" that the initial guess produced the orbitals in such an order that we had the 2s and 2p orbitals active. **IN GENERAL IT IS YOUR RESPONSIBILITY THAT THE ORBITALS ARE ORDERED SUCH THAT THE ORBITALS THAT YOU WANT IN THE ACTIVE SPACE COME IN THE DESIRED ORDER.** In many cases this will require re-ordering and **CAREFUL INSPECTION** of the starting orbitals.
