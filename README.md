# marathon

`marathon` runs sets of computational chemistry calculations in batch.
It currently supports ADF, NWChem and ORCA.

    marathon -n 2 nwchem *.nw
    marathon -h

## Installation

After downloading the tarball and using `cd` to go where the files are, simply do a `sudo make install` and everything will be installed.

But `marathon` will need to know where ORCA is in your system.
So set an environment variable in your `~/.bashrc` (or equivalent) as follows:

    export ORCABIN="/path/to/your/orca/"

This should point to the absolute path to the ORCA binary parent directory.
ORCA may thus *not* be in `PATH`.

## TODO

- (A) Trap some useful signals (e.g. HUP signal) within `marathon`.
- (B) Set number of threads for ORCA using the command line.
- (B) Implement quiet (`-q`) mode.
