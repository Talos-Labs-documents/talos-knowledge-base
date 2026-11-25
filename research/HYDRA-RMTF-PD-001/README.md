# HYDRA-RMTF-PD-001
Open Inquiry Initiative | 2026-11-25 | Public research charter and generation-zero baseline

## Scope
Investigate whether a wormhole can provide access to an expanded spatial region or itself contain usable interior volume. Inspired by fictional pocket laboratories; fiction is not evidence. RMTF matter-state transmission does not imply control of spacetime. Light-speed transmission remains limited by distance.

## Generation zero: executed symbolic baseline
Use the ultrastatic Ellis-type metric in units c=G=1:
ds² = -dt² + dl² + (l²+a²)dΩ², a>0.
The areal radius r(l)=sqrt(l²+a²) has a minimum a at l=0. SymPy differentiation returned r''=a²/(a²+l²)^(3/2). For a radial null vector with orthonormal components (1,1,0,0), Einstein's equations give 8π T_ab k^a k^b = -2r''/r = -2a²/(a²+l²)². This is negative everywhere: the model violates the null energy condition. This is a constraint, not evidence of an engineered wormhole.
The proper spatial volume of the bounded segment -L≤l≤L is 8π(a²L+L³/3). For L=a, SymPy integration returned 32πa³/3. This demonstrates a finite interior volume in an assumed geometry, not a compact pocket universe; the model has two asymptotic ends. Increasing L increases volume but does not establish a compact exterior footprint.

Reproduction (Python with SymPy):
```python
import sympy as s
l,a=s.symbols('l a', real=True, positive=True)
r=s.sqrt(l*l+a*a)
print(s.simplify(s.diff(r,l,2)))
print(s.simplify(-2*s.diff(r,l,2)/r))
print(2*s.integrate(4*s.pi*(l*l+a*a),(l,0,a)))
```
The positive-l integration uses reflection symmetry. The symbolic check was executed; the full Einstein tensor and independent derivation remain to be verified.

## Hydra branch queue
1. GR: independently derive Einstein tensor and throat conditions.
2. Interior geometry: compare long throats, bag-of-gold geometries and compact boundaries; distinguish horizons from traversable mouths.
3. Quantum fields: evaluate energy inequalities and semiclassical assumptions.
4. Electromagnetic coupling: test stress-energy constraints; frequency alone is not a mechanism.
5. Stability: perturbations, tidal forces and backreaction.
6. Causality: global structure, conservation and boundary conditions.
7. Numerical methods: convergence tests and reproducible parameter sweeps.
8. Adversarial verification: independently reproduce calculations and challenge assumptions.

## Recursive protocol
RABE-001: descend assumptions, ascend dependencies, branch alternatives, evaluate evidence. Preserve failed paths, equations, units, source provenance, solver versions, code and raw results. Each generation must have bounded scope and explicit stop criteria. No branch advances merely because agents agree. Require independent implementation and qualified human review before physical claims. No physical experiments authorized by this charter.

## References for subsequent verification
Morris & Thorne (1988), Wormholes in spacetime and their use for interstellar travel, DOI: 10.1119/1.15620.
Ellis (1973), Ether flow through a drainhole, DOI: 10.1063/1.1666161.
These are foundational reading targets, not a completed literature review.

## Status
Generation zero: symbolic baseline executed, limited pass for differentiation and volume integration; ordinary null-energy-condition support fails for the selected geometry. Eight branches are proposed, not independently launched. No physical feasibility, pocket universe, or RMTF coupling demonstrated. AI-assisted research; independent expert review pending. Public release authorized by project owner. No private source code included.
