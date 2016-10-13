---
layout: page
title: ETA/OS
tagline: ETA/OS reference
---
{% include JB/setup %}


## About

ETA/OS is a small scale, embedded kernel and/or operating system. It provides
basic hardware abstraction allowing an application programmer to build somewhat
portable embedded applications. Some of its features:

  * Scheduler (semi-SMP ready)
  * Memory management
  * Driver core
  * Bunch of basic drivers (USART etc..)

## License

ETA/OS is licenced as GNU General Public Licence version 3 or newer. 
The COPYING file should contian more information about the licence, or
if it's not included, look at http://www.gnu.org/licences/.

    ETA/OS
    Copyright (C) 2014 2015 2016 <etaos@googlegroups.com>

    This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with this program.  If not, see <http://www.gnu.org/licenses/>.

## Compiling ETA/OS

To retrieve and build ETA/OS the following tools are required:

Retreiving:

  * Git or
  * a tarball download

Build tools (for the host and target system):

  * gcc
  * as
  * ld
  * objcopy
  * a working linux distro

Before you can build ETA/OS you have to configure it. Run

    make menuconfig ARCH=<archname>

to start the configuration process.

When you are finished configuring the project run the following make commands
to fully build ETA/OS:

    make prepare ARCH=<archname>
    make all ARCH=<archname>
    make modules_install ARCH=<archname> INSTALL_MOD_PATH=<path>

After that, you are ready to compile an application. To compile an application
you need application sources and Kbuild file in a sepperate directory (anywhere).
See the usr/tests/ directory for some examples.

## Contributing

ETA/OS is free software, and anyone is more then welcome to contribute to this
project. If you have written a patch, you can send this patch or pull request to 
etaos@googlegroups.com. For more information on how to contribute to etaos,
please read our [contribution guide](contrib.html).

## Help

The full documentation of ETA/OS is available [here](docs). If you need any kind
of further help, and with any kind we mean any kind, you can contact us
in the following ways:

  * Using the mailing list (etaos@googlegroups.com)

Feel free to ask all your questions there.

