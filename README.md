# UoB Positron Imaging Centre-Improved CFDEMcoupling

This repository is a fork of [**CFDEMcoupling-PUBLIC**](https://github.com/CFDEMproject/CFDEMcoupling-PUBLIC) with additions for an immersed boundary (IB) / fully-resolved CFD–DEM workflow.

**Contact:**

General queries: [fjbarter@outlook.com](mailto:fjbarter@outlook.com)

Specific implementation of the improved immersed-boundary method: [chehanqiao@outlook.com](mailto:chehanqiao@outlook.com)

## About this fork

This fork adds an improved fully resolved CFD–DEM / immersed boundary capability based on the CFDEM framework and the approach described by Zhang (2018) (see References).

### Additions in this fork

**New submodels**
- **Force model**
  - `ReactionIB` – fluid–particle interaction force based on the momentum source term (alternative to `ShirgaonkarIB`)
- **Voidfraction models**
  - `IBVoidFractionKempe`
  - `IBVoidFractionSDF`

**Solver**
- `cfdemSolverIBPICI`

**Tutorials / examples**
- Flow through ordered packings validation case in `./tutorials/` (SC, BCC, FCC) with comparison against analytical data (Zick & Homsy).

## Compatibility

This fork is based on the **OpenFOAM-6 compatible** CFDEMcoupling-PUBLIC codebase.

- Tested with: **OpenFOAM 6**
- OS: **Ubuntu 24.04, RedHatEnterprise 8.10**

PICI-CFDEMcoupling is compatible with [PICI-LIGGGHTS](https://github.com/uob-positron-imaging-centre/PICI-LIGGGHTS) and also backwards-compatible with LIGGGHTS-PUBLIC.

## Installation

Installation follows CFDEMcoupling-PUBLIC. Refer to [www.cfdem.com](www.cfdem.com) for the general procedure, then build this fork’s solvers/libraries using the usual CFDEM build scripts (e.g. `cfdemCompCFDEM`, depending on your environment).

## Upstream project: CFDEMcoupling-PUBLIC

CFDEMcoupling-PUBLIC is an Open Source coupled CFD-DEM framework combining the strengths of LIGGGHTS® DEM code and the Open Source CFD package OpenFOAM® [^1]. CFDEMcoupling stands for Computational Fluid Dynamics (CFD) - Discrete Element Method (DEM) coupling.

CFDEMcoupling-PUBLIC is compatible with [LIGGGHTS-PUBLIC](https://github.com/CFDEMproject/LIGGGHTS-PUBLIC).


### Trademarks / disclaimer

LIGGGHTS® and CFDEM® are registered trade marks of DCS Computing GmbH. Some parts of CFDEMcoupling are based on OpenFOAM®.


## Licence

PICI-CFDEMcoupling is open-source, distributed under the terms of the GNU General Public License v3 or later.

## How to cite

If you use PICI-CFDEMcoupling in a publication, please cite the following article (Open Access):

> [Hanqiao Che](https://orcid.org/0000-0002-7479-3504), [Christopher R. K. Windows-Yule](https://orcid.org/0000-0003-1305-537X), [Catherine O'Sullivan](https://orcid.org/0000-0002-0935-1910), [Jonathan Seville](https://orcid.org/0000-0003-0207-3521) "**A novel semi-resolved CFD-DEM method with two-grid mapping: methodology and validation.**" AIChE Journal, 2023. DOI: [10.1002/aic.18321](https://doi.org/10.1002/aic.18321).

```bibtex
@article{che2024cfddem,
  title={A novel semi-resolved CFD-DEM method with two-grid mapping: Methodology and verification},
  author={Che, Hanqiao and Windows-Yule, Kit and O'Sullivan, Catherine and Seville, Jonathan},
  journal={AIChE Journal},
  volume={70},
  number={2},
  pages={e18321},
  year={2024},
  doi = {https://doi.org/10.1002/aic.18321}
}
```

AND

> Christoph Goniva, Christoph Kloss, Niels G. Deen, Johannes A. M. Kuipers, Stefan Pirker "**Influence of rolling friction on single spout fluidized bed simulation.**" *Particuology*, 2012. DOI: [10.1016/j.partic.2012.05.002](https://doi.org/10.1016/j.partic.2012.05.002)

```bibtex
@article{goniva2012influence,
  title={Influence of rolling friction on single spout fluidized bed simulation},
  author={Goniva, Christoph and Kloss, Christoph and Deen, Niels G and Kuipers, Johannes AM and Pirker, Stefan},
  journal={Particuology},
  volume={10},
  number={5},
  pages={582--591},
  year={2012},
  publisher={Elsevier}
}
```

Also, we ask that you "star" :star: this repository to help us gauge the level of interest in this project. Your star not only signifies your support but also assists us in tracking user engagement, a crucial factor for securing future grant funding. Your contribution in this regard is highly appreciated.

## References:
C. Zhang, C. Wu, K. Nandakumar, Effective Geometric Algorithms for Immersed Boundary Method Using Signed Distance Field, Journal of Fluids Engineering, 141 (2018). 

T. Kempe, S. Schwarz, J. Fröhlich, Modelling of spheroidal particles in viscous flows,  Proceedings of the Academy Colloquium Immersed Boundary Methods: Current Status and Future Research Directions (KNAW, Amsterdam, The Netherlands, 15–17 June 2009), 2009.

Zick, A., & Homsy, G.  Stokes flow through periodic arrays of spheres. Journal of Fluid Mechanics, 115(1982), 13-26. DOI: [10.1017/S0022112082000627](https://doi.org/10.1017/S0022112082000627).