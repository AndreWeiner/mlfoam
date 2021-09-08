# OpenFOAM technical committee on data-driven modeling

This document represents a draft roadmap for the potential initiation of a technical committee on data-driven modeling with OpenFOAM. The structure of this documents mirrors the wiki pages of [existing technical committees](https://www.openfoam.com/governance/technical-committees).

## Our objectives in a nutshell

This section briefly summarizes **why** we would like to initiate a technical committee on data-driven modeling. The technical roadmap details **how** we plan to achieve our objectives.

- short term objectives
  - reduce the technical barrier to get started with data-riven modeling in OpenFOAM to enable more people to include data-driven workflows in their applications or research
  - promote data-driven techniques that are already available in OpenFOAM, e.g., dynamic mode decomposition (DMD)
- long term objectives
  - aid the understanding of when to use data-driven models in the CFD workflow
  - accelerate developments and applications of machine learning (ML) with OpenFOAM
  - establish tested ML models as a natural element of CFD simulations to improve accuracy and/or speed

## Potential workflow

We would like to have short virtual meetings (max. 1h) every **two** month and meet in person, if possible, at the OpenFOAM conference and workshop. The bi-monthly meetings serve to update all members about the recent progress and to coordinate upcoming efforts.

## Interaction with existing committees

Data-driven modeling and in particular machine learning is going to touch every aspect CFD with OpenFOAM and requires coordination with all other technical committees. We still need to clarify if our objectives and efforts might be embedded in an existing committee, or if a new committee should be formed that coordinates with existing ones whenever necessary. Our currently preferred mode would be to get in touch with the most suitable available committee when new developments are available (tutorials, models, numerics, ...), but to organize and bundle all efforts within separate committee. Otherwise, transferable technical and practical knowledge might be too scattered.

To find the most suitable structure, we will get in touch with the existing committees.

## Technical roadmap

### libtorch C++ API seamlessly integrated with OpenFOAM

- Simplified construction of Neural Networks (NN) in OpenFOAM. 
- Enabled RTS for activation functions. 
- Created a CI test pipeline for unit tests. 
- Simplified learning of field data in OpenFOAM
  - Learning geometric fields in OpenFOAM.
  - Learning near-boudary fields. 
  - Learning field sub-sets.
- Developed adapter class hierarchy roots for ML models in OpenFOAM
  - ML boundary condition
  - ML lagrangian models 
  - ML pressure-velocity coupling algorithm
- High-Performance Computing with OpenFOAM and libtorch
  - Learning OpenFOAM geometric fields in parallel
  - Offloading to the GPU 
  - Global training vs weak NN conditions on process boundaries
- Documentation 
  - Tutorial cases:
    1. Learning a pressure field (internal field)
    2. Learning a boundary field (BCs)
    3. Learning a surface (sub-set of a geometric field)
  - Workflows for hyperparameter tuning.

## How to get in touch

The idea for the new technical committee is currently worked out and put forward by

- Tomislav Marić, TU Darmstadt, Germany
- Andre Weiner, TU Braunschweig, Germany

If you would like to contribute to this roadmap, provide additional ideas or spark up a discussion, the most direct way to get in touch would be to open an issue in this repository.
