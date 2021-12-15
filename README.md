# Docker container for the core GAP system

The Docker container for the core GAP system is available at DockerHub here:
https://registry.hub.docker.com/u/jamesdbmitchell/gap-docker-minimal-arm-32

This GAP Docker container provides only the core GAP system and several
packages which are needed by GAP (GAPDoc, PrimGrp, SmallGrp, TransGrp,
PackageManager).  It may be used, for example, in automated tests of different
configurations of GAP packages by installing them in the `pkg` subdirectory of
`/home/gap/inst/gap-4.X.Y/`.

If you install Docker, you may run GAP in this container interactively. As you
see from the output below, it does not have a number of packages included in
the official GAP distribution. 

```
$ docker run --rm -i -t jamesdbmitchell/gap-docker-minimal-arm-32:version-4.11.1

gap@efe71f407f1e:~$ gap -A
 *********   GAP 4.11.1 of 2021-03-02
 *  GAP  *   https://www.gap-system.org
 *********   Architecture: armv7l-unknown-linux-gnueabihf-default32-kv7
 Configuration:  gmp 6.2.0, GASMAN, readline
 Loading the library and packages ...
 Packages:   GAPDoc 1.6.4, PrimGrp 3.4.1, SmallGrp 1.4.2, TransGrp 3.3
 Try '??help' for help. See also '?copyright', '?cite' and '?authors'
gap> 
```
