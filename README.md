# marathon

`marathon` runs sets of computational chemistry calculations in batch.

    marathon -n 2 nwchem *.nw
    marathon -h

## Supported software

- [ADF & adfnbo](https://www.scm.com/)
- [Gaussian](http://gaussian.com/)
- [GENNBO](http://nbo6.chem.wisc.edu/)
- [MOPAC](http://openmopac.net/)
- [NWChem](http://www.nwchem-sw.org/index.php/Main_Page)
- [ORCA & ORCA4](https://orcaforum.cec.mpg.de/)
- [Psi4](http://www.psicode.org/)

## Installation

After downloading the tarball and using `cd` to go where the files are, simply do a `sudo make install` and everything will be installed.

But `marathon` will need to know where ORCA is in your system.
So set an environment variable in your `~/.bashrc` (or equivalent) as follows:

    export ORCABIN="/path/to/your/orca/"

This should point to the absolute path to the ORCA binary parent directory.
ORCA may thus *not* be in `PATH`.

## TODO

- (A) Trap some useful signals (e.g. HUP signal) within `marathon`.
- (B) Implement quiet mode and make it default.
  - The behaviour of MOPAC now is quiet already.
    Make it show its output in nonquiet/verbose mode.
