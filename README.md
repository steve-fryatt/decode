Decode
======

Guess the sequences selected by the computer.


Introduction
------------

The aim of Decode is to guess a sequence of four colours selected randomly by the computer. Load it on to the iconbar in the usual way and click Select on its icon to open the game window.

Sequences always contain four different coloured pegs from the row of ten at the top of the window: no colour will be used more than once. Up to twelve guesses can be made and after each, the computer will score the guess to show how close it is to the correct answer. Using this information, it should be possible to identify the chosen sequence.


Building
--------

Decode consists of a collection of un-tokenised BASIC, which must be assembled using the [SFTools build environment](https://github.com/steve-fryatt). It will be necessary to have suitable Linux system with a working installation of the [GCCSDK](http://www.riscos.info/index.php/GCCSDK) to be able to make use of this.

With a suitable build environment set up, making Decode is a matter of running

	make

from the root folder of the project. This will build everything from source, and assemble a working !Decode application and its associated files within the build folder. If you have access to this folder from RISC OS (either via HostFS, LanManFS, NFS, Sunfish or similar), it will be possible to run it directly once built.

To clean out all of the build files, use

	make clean

To make a release version and package it into Zip files for distribution, use

	make release

This will clean the project and re-build it all, then create a distribution archive (no source), source archive and RiscPkg package in the folder within which the project folder is located. By default the output of `git describe` is used to version the build, but a specific version can be applied by setting the `VERSION` variable -- for example

	make release VERSION=1.23


Licence
-------

Decode is licensed under the EUPL, Version 1.2 only (the "Licence"); you may not use this work except in compliance with the Licence.

You may obtain a copy of the Licence at <http://joinup.ec.europa.eu/software/page/eupl>.

Unless required by applicable law or agreed to in writing, software distributed under the Licence is distributed on an "**as is**"; basis, **without warranties or conditions of any kind**, either express or implied.

See the Licence for the specific language governing permissions and limitations under the Licence.