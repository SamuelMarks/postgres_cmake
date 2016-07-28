[![Build Status](https://travis-ci.org/stalkerg/postgres_cmake.svg?branch=cmake)](https://travis-ci.org/stalkerg/postgres_cmake)

CMake build and test howto
=================
```bash
git clone https://github.com/stalkerg/postgres_cmake.git
cd ./postgres_cmake
#build dir is optional but best way for CMake
mkdir build
cd build
CFLAGS="-s -O2" cmake .. -DCMAKE_INSTALL_PREFIX="/usr/local"
#strip binary + O2 optimisation
make -j2
make check
make isolation_check
make contrib_check

#Optional:
make plperl_check
make pltcl_check

#For example setup for python2.7:
#-DPython_ADDITIONAL_VERSIONS=2.7 -DPYTHON_EXECUTABLE=/usr/bin/python2.7
make plpython_check

make install
make installcheck
```


PostgreSQL Database Management System
=====================================

This directory contains the source code distribution of the PostgreSQL
database management system.

PostgreSQL is an advanced object-relational database management system
that supports an extended subset of the SQL standard, including
transactions, foreign keys, subqueries, triggers, user-defined types
and functions.  This distribution also contains C language bindings.

PostgreSQL has many language interfaces, many of which are listed here:

	http://www.postgresql.org/download

See the file INSTALL for instructions on how to build and install
PostgreSQL.  That file also lists supported operating systems and
hardware platforms and contains information regarding any other
software packages that are required to build or run the PostgreSQL
system.  Copyright and license information can be found in the
file COPYRIGHT.  A comprehensive documentation set is included in this
distribution; it can be read as described in the installation
instructions.

The latest version of this software may be obtained at
http://www.postgresql.org/download/.  For more information look at our
web site located at http://www.postgresql.org/.
