# Simple Open EtherCAT Master Library
[![Build Status](https://github.com/OpenEtherCATsociety/SOEM/workflows/build/badge.svg?branch=master)](https://github.com/OpenEtherCATsociety/SOEM/actions?workflow=build)

BUILDING
========


Prerequisites for all platforms
-------------------------------

 * CMake 2.8.0 or later


Windows (Visual Studio)
-----------------------

 * Start a Visual Studio command prompt then:
   * `mkdir build`
   * `cd build`
   * `cmake .. -G "NMake Makefiles"`
   * `nmake`

Linux & macOS
--------------

   * `mkdir build`
   * `cd build`
   * `cmake ..`
   * `make`

### Build RPM

   * `cmake .`
   * `make package`

### Deploy RPM

* Find 32 bit soem rpm path in build output from [buildcentos6-32](http://buildsba:8080/job/soem-library/label=buildcentos6-32/) or [buildcentos7-64](http://buildsba:8080/job/soem-library/label=buildcentos7-64/).
* scp rpm file to fsfs:/data/repos/lcogt/6 and fsfs:/data/repos/lcogt/7 (as root)
* run lcogt.bash script in fsfs:/data/repos to add to yum (as root)


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
