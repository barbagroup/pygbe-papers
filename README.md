# pygbe-papers

## Submitted 2015

**Title 1:**

*"Probing protein orientation near charged nanosurfaces for  simulation-assisted biosensor design"*

**Abstract:**

Protein-surface interactions are ubiquitous in biological processes and bioengineering, 
yet are not fully understood. In biosensors, a key factor determining the sensitivity and 
thus the performance of the device is the orientation of the ligand molecules on the bioactive 
device surface. Adsorption studies thus seek to determine how orientation can be influenced by 
surface preparation, varying surface charge and ambient salt concentration. In thiswork, protein 
orientation near charged nanosurfaces is obtained under electrostatic effects using the Poisson-
Boltzmann equation, in animplicit-solvent model. Sampling the free energy for protein GB1D4' at 
a range of tilt and rotation angles with respect to the charged surface, we calculated the 
probability of the protein orientations and observed a dipolar behavior.This result is consistent 
with published experimental studies and combined Monte Carlo and molecular dynamics simulations 
using this small protein, validating our method. More relevant to biosensor technology, antibodies 
suchas immunoglobulin G are still a formidable challenge to molecular simulation, due to their 
large size. We obtained the probability distribution of orientations for the iso-type IgG2a at 
varying surface charge and salt concentration. This iso-type was not found to have a preferred 
orientation in previous studies, unlike IgG1 whose larger dipole moment was assumed to make it 
easier to control. Our results show a high-probability and favorable orientation for IgG2a with 
positive surface charge of 0.2C/m^2 and 9mM salt concentration. The results also show that local 
interactions dominate over dipole moment for this protein. Improving immunoassay sensitivity may 
thus be assisted by numerical studies using our method (and open-source code), guiding changes to 
fabrication protocols or protein engineering of ligand molecules to obtain more favorable orientations.

**Title 2:**

*"Poisson-Boltzmann model for protein-surface electrostatic interactions and grid-convergence study using the PyGBe code"*

*Abstract:*

Interactions between surfaces and proteins occur in many vital processes and are crucial in biotechnology: the ability to control specific interactions is essential in fields like biomaterials, biomedical implants and biosensors. In the latter case, biosensor sensitivity hinges on ligand proteins adsorbing on bioactive surfaces with a favorable orientation, exposing reaction sites to target molecules.
Protein adsorption, being a free-energy-driven process, is difficult to study experimentally. This paper develops and evaluates a computational model to study electrostatic interactions of proteins and charged nanosurfaces, via the Poisson-Boltzmann equation.
We extended the implicit-solvent model used in the open-source code PyGBe to include surfaces of imposed charge or potential. This code solves the boundary integral formulation of the Poisson-Boltzmann equation, discretized with surface elements. PyGBe has at its core a treecode-accelerated Krylov iterative solver, resulting in O(N log N) scaling, with further acceleration on hardware via multi-threaded execution on GPUs. It computes solvation and surface free energies, providing a framework for studying the effect of electrostatics on adsorption.
We then derived an analytical solution for a spherical charged surface interacting with a spherical molecule, then completed a grid-convergence study to build evidence on the correctness of our approach. The study showed the error decaying with the average area of the boundary elements, i.e., the method is $O(1/N)$, which is consistent with our previous verification studies using PyGBe.
We also studied grid-convergence using a real molecular geometry (protein GB1D4'), in this case using Richardson extrapolation (in the absence of an analytical solution) and confirmed the O(1/N) scaling in this case.
PyGBe is open-source under an MIT license and is hosted under version control at [https://github.com/barbagroup/pygbe](https://github.com/barbagroup/pygbe). In addition, we prepared "reproducibility packages"  to supplement this paper, consisting of running and post-processing scripts in Python to allow replication of the grid-convergence studies, all the way to generating the final plots, with a single command.
