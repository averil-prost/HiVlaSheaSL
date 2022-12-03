# **Hi**gh-order **Vla**sov-Poisson **Shea**th solver by **S**emi-**L**agrangian.

* Authors : [Yann Barsamian](https://www.barsamian.am/), [Michel Mehrenberger](http://www.i2m.univ-amu.fr/perso/mehrenberg.m/).
 
Simulation of the symmetric sheath problem with ionization term. Discretization by Semi-Lagrangian with Lagrange polynomial interpolation and time splitting. 

File structure on sept, 5th 2022:

- data\_input/ 		*folder for initial conditions (.dat)*
- data\_output/ 		*outputs from Yann c code (.hdf5, .dat, .txt...)*
- python\_diags/		*outputs from diag_sheath (.png, .mp4, .txt...)*
- yaml/			*folder for configuration files (.yaml)*
- include/		*all c dependencies*

- compile\_hivlashea.sh 	*compile script*
- hivlashea.c 		*main of the c code*
- hivlashea.out 	*when created, ignored by git. executable*
- diag\_sheath.py	*python script to generate post-treatment diags*
- savedata.sh		*script to copy inputs, outputs and yaml in a separate folder*
- clean.sh		*script to clean output folders*

How to use: 
- compile with `./compile_hivlashea.sh` 
- execute directly in the folder by `./hivlashea yaml/theyamlfile.yaml`
- if needed, create images/videos with `python[3] diag_sheath.py` (!!! modify yamlfilename)
- if needed, create a copy of the data by `./savedata yaml/theyamlfile.yaml`
- if needed, clean output folders by `./clean` (!!! be sure)

