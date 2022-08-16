# Simple Open EtherCAT Master Library
[![Build Status](https://github.com/OpenEtherCATsociety/SOEM/workflows/build/badge.svg?branch=master)](https://github.com/OpenEtherCATsociety/SOEM/actions?workflow=build)

BUILDING
========


Prerequisites for all platforms
-------------------------------

 * CMake 2.8.0 or later


Linux
--------------

### Build RPM

   * `cmake .`
   * `make package`

### Use the buildenv project to build for a target host

The [buildenv](https://github.com/LCOGT/buildenv) project provides wrappers around jenkins build swarm nodes allowing a developer to test compilations
or to build one-off projects such as an RPM for a target machine.

Steps:
* check out buildenv
* build your target environment
* build artefact for target

So to build the soem rpm for rocky 8:

```console
$ cd ~/
$ git clone git@github.com:LCOGT/buildenv.git
$ cd buildenv
$ ./makeenv r8
$ cd ~/workspace/SOEM
$ cmake . && make package
```

### Deploy RPM

* Find soem rpm path you have built.
* scp rpm file as root to the relevant repo, e.g. for rocky8 fsfs:/data/repos/lcogt/8
* run lcogt.bash script in fsfs:/data/repos to add to yum (as root)


Windows (Visual Studio)
-----------------------

 * Start a Visual Studio command prompt then:
   * `mkdir build`
   * `cd build`
   * `cmake .. -G "NMake Makefiles"`
   * `nmake`
   
ERIKA Enterprise RTOS
---------------------

 * Refer to http://www.erika-enterprise.com/wiki/index.php?title=EtherCAT_Master

Documentation
-------------

See https://openethercatsociety.github.io/doc/soem/


Want to contribute to SOEM or SOES?
-----------------------------------

If you want to contribute to SOEM or SOES you will need to sign a Contributor
License Agreement and send it to us either by e-mail or by physical mail. More
information is available in the [PDF](http://openethercatsociety.github.io/cla/cla_soem_soes.pdf).
