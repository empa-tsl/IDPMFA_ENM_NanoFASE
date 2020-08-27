# IDPMFA_ENM_NanoFASE
IDPMFA_ENM_NanoFASE is a tool developed as part of the following publication:

Title: Integrated dynamic probabilistic material flow analysis of engineered materials in European countries

Authors: Véronique Adam, Qie Wu, Bernd Nowack

Submitted to the journal NanoImpact in September 2020.

IDPMFA_ENM_NanoFASE is a tool that generates probability distributions associated with the flows of nano-Ag, nano-TiO2 and nano-ZnO within their lifecycle and towards the environment, at the national scale for each European country (EU28, Norway and Switzerland) from 2000 to 2020 with a yearly timestep.

The tool is written in Python 3 and made of three packages, one for each ENM. Each package contains five modules:

Components.py, in which the different classes of compartments and flows are defined
Model.py, where the methods required to link the compartments together with the flows are defined
Simulator.py, which includes the methods required to run the simulation and extract results
ENM_Dynamic_model_Country.py, in which all system components and transfers are implemented and parametrized with the associated probability distributions from the input data
ENM_Runner_Country.py, which specifies the time periods and number of simulation runs, initiates the simulation experiment and processes the results.
Two additionnal functions are used to generate specific probability functions:

TriangularBalanced.py
TruncatingFunctions.py
ENM_Dynamic_model_Country.py takes as input a csv file containing the probability distributions of the produced amounts of ENMs in each year: "ENM_production2000-2020.csv".

To adapt the tool to another substance, the user needs to adapt the module named  "ENM_Dynamic_model_Country" and its input file, which includes data on production. To adapt the type of results extracted, the user needs to adapt the module named "ENM_Runner_Country".

For further details, the user is referred to the above publication.
