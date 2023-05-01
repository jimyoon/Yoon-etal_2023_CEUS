# Yoon et al., 2023 CEUS
**Structural model choices regularly overshadow parametric uncertainty in agent-based simulations of household flood risk outcomes.**

Jim Yoon*, Heng Wan, Brent Daniel, Vivek Srikrishnan, David Judi

\* corresponding author:  jim.yoon@pnnl.gov

## Abstract
Agent-based models (ABMs) have been increasingly used for flood risk analysis, driven by the recognition that commonly used analyses typically neglect adaptive human behavior in relation to flood hazards. However, ABM simulation results can be highly sensitive to a number of modeling choices. Here, we introduce an agent-based modeling framework to explore the impact of structural versus parametric choices of household flood aversion on modeled outcomes of flood risk in a hypothetical urban environment. We deploy three structural variants of the model that fundamentally differ in the manner in which households are assumed to interface with flood hazards (disamenity, avoidance, and protection), evaluating multiple model parameterizations within each structural variant. The structural variants lead to fundamentally different conclusions regarding the evolution of flood risk, indicating that the structural choices made regarding human representation in flood risk ABMs have substantial bearing on modeling insights and ought to be elevated from an overlooked to a critical aspect of future modeling efforts.

## Contributing modeling software
| Model | Version | Repository Link |
|-------|---------|-----------------|
| CHANCE-C | 1.0 | https://github.com/jimyoon/icom_abm |

## Reproducing my workflow
__1.__ The scripts used for the simulations presented in the publication are stored in the github repo above in the constance_runs/20230322_CEUS_Publication directory.

__2.__ Run the abm_baltimore_example_CEUS2023.py script conduct a model simulation on a local machine. Model run and scenario options can be modified directly in the code to define structural/parametric variant options and scenario conditions (e.g., population growth rate).

__3.__ For the ensemble of model runs presented in the manuscript, the model is deployed on an HPC via the Slurm workload manager. A customized job script (icom_batch_CEUS2023.txt) and Python script for batch simulation (abm_baltimore_example_PIC_slurm_CEUS2023.py) are provided in the github repo.

__4.__ A successful model run results in a set of output files at the block group (e.g., "results_utility_") and at the agent level (e.g., "hh_results_utility_").

__5.__ The model outputs from step 4 above are processed through various segments of the "post_processing_examples_CEUS2023.py" file to generate the figures for Figures 2-4 of the manuscript. The figures generated via the script are subsequently touched up in Inkscape for final publication.

__6.__ The agent level outputs are processed through Raw Graphs (https://app.rawgraphs.io/) to generate the alluvial diagrams in Figure 5. Final touch-ups are implemented in Inkscape.
