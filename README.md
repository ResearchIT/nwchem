# Singularity Recipe for NWChem

This repo contains recipes to run [NWChem](http://www.nwchem-sw.org/index.php/Main_Page)
within a [Singularity](http://singularity.lbl.gov/) container, which can be built 
using [Singularity Hub](https://singularity-hub.org/)

Versions:

* 6.6 - NWChem with OpenMPI installed via EPEL

## How to Use:

You need to have openmpi v1 installed on your local machine (via yum or as a module).
Testing was performed with openmpi 1.10.6.

Run example:

mpirun -np 2 singularity exec shub://ResearchIT/nwchem:6.6-openmpi nwchem_openmpi test.nw

## Alternative method:
use the provided bash wrapper and module file to use the nwchem singularity container like a standard module
(this assumes you have a singularity/2.4 and openmpi/1 modules)

e.g.

module load nwchem/6.6
mpirun -np 2 nwchem test.nw
