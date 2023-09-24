# scm - simple clipboard manager

scm is a minimalist clipboard manager for X.

## Requirements
In order to build scm you need the Xlib and Xfixes header files.\
It is also expected that you have dmenu installed.

## Running scm

Arguments:
* `-d` specifies the cache directory
* `-v` prints the version number
* `-V` enables debug messages which are printed to stderr
* `-p` listens for PRIMARY selection changes
* `-1` runs scm for one loop iteration (fetch, save and quit)
* `-k` prevents scm from removing old entry files.

The `scmd` script sets the cache directory to **\$XDG_CACHE_HOME** or
**\$HOME/.cache/scm**. All arguments passed to scmd are redirected to scm.

The `scmenu` script parses the `line_cache` file generated by scm and pipes
the data to `dmenu`. By default scm will store up to 30 entries.
This behavior can be changed by editing the config.h file and recompiling scm.
