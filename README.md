# <ins>Hi</ins>gh-order <ins>Vla</ins>sov-Poisson <ins>Shea</ins>th solver by <ins>S</ins>emi-<ins>L</ins>agrangian.

* Authors : [Yann Barsamian](https://www.barsamian.am/), [Michel Mehrenberger](http://www.i2m.univ-amu.fr/perso/mehrenberg.m/), [Averil Prost](https://averil-prost.github.io/).
 
Simulation of the symmetric sheath problem with ionization term. Discretization by Semi-Lagrangian with Lagrange polynomial interpolation and time splitting. 

Expected file structure upon run:

<table>
<tr>
<td align='right'>

data\_input/

data\_output/ 

python\_diags/	

yaml/	

include/

compile\_hivlashea.sh 

hivlashea.c 

hivlashea.out 

diag\_sheath.py	

savedata.sh	

clean.sh	

</td>
<td>

folder for initial conditions (.dat)

outputs from c code (.hdf5, .dat, .txt...)

outputs from diag_sheath (.png, .mp4, .txt...)

folder for configuration files (.yaml)

all c dependencies

compile script

main of the c code

when created, ignored by git. executable

python script to generate post-treatment diags

script to copy inputs, outputs and yaml in a separate folder

script to clean output folders

</td>
</tr>
</table>

How to use: 
- compile with `./compile_hivlashea.sh` 
- execute directly in the folder by `./hivlashea yaml/theyamlfile.yaml`
- if needed, create images/videos with `python[3] diag_sheath.py` (!!! modify yamlfilename)
- if needed, create a copy of the data by `./savedata yaml/theyamlfile.yaml`
- if needed, clean output folders by `./clean` (!!! be sure)

