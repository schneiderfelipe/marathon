# marathon

## Usage

Here is how to use `marathon`:

    $ marathon {methane,ethane,n-propane}.inp

`marathon` may also be run under `nohup` as follows:

    $ nohup marathon *.inp &

## Installation

After downloading the tarball and using `cd` to go where the files are, simply do a `sudo make install` and everything will be installed.

But `marathon` will need to know where ORCA is in your system.
So set an environment variable in your `~/.bashrc` (or equivalent) as follows:

    export ORCABIN="/path/to/your/orca"

This should point to the absolute path to the ORCA binary.
ORCA may thus *not* be in `PATH`.
You can even change versions by issuing

    $ ORCABIN="/path/to/another/orca" marathon *.inp

## TODO

(A) Trap some useful signals in `marathon`
(B) Make `marathon` go to each folder in order to run (make things such as `$ marathon */*.inp` work)
