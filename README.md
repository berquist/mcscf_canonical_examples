# Canonical examples of MCSCF-based calculations

Every time I need an example of an input for a multiconfigurational or multireference calculation, or want to look up something for Chemistry Stack Exchange, I wish I had a set of good, worked examples.

If you'd like to contribute, feel free to submit a pull request. Please, no Gaussian inputs or outputs. Any other package is fine.

## Folder structure

This is subject to change if a better solution presents itself.

`molecule w/ charge -> active space / multiplicity / state-specific or state-averaged -> [programs]`

Examples:

```
benzene/
    ...
water/
    README.md
    casscf_4_4_singlet_ss_0/
        dalton.dal
        gamess.inp
        molcas.in
        molpro.in
        orca.in
        psi4.in
    water.xyz
water_cation/
    casscf_3_4_doublet_sa_0_1_2/
        ...
```

## Examples

- Benzene  (D_{6h} -> D_{2h})
- Beryllium atom (K_{h} -> D_{2h})
- Nitrogen dimer (D_{\infty h} -> D_{2h})
- Water (C_{2v})
- Water cation (C_{2v})

## Program notes

- When freezing orbitals in DALTON using `*CONFIGURATION INPUT/.INACTIVE`, the number specified for each irrep is the _doubly occupied orbitals_, not the electrons. This is similarly true for Psi4 `*_docc` and `active`.
- For Psi4, you might think you want `frozen_docc`, but you actually want `restricted_docc`, otherwise the internal orbitals will never have their MO coefficients updated.

## Useful resources

- [D2h Character table](http://www.webqc.org/symmetrypointgroup-d2h.html)
