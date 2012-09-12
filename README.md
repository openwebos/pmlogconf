PmLogConf
=========

Summary
-------
Configuration files used by PmLogLib, PmLogDaemon and PmLogCtl


Dependencies
============

Below are the tools (and their minimum versions) required to build PmLogConf:

* cmake (version required by openwebos/cmake-modules-webos)
* openwebos/cmake-modules-webos 1.0.0 RC3

How to Build on Linux
=====================

## Building

Once you have downloaded the source, enter the following to build it (after
changing into the directory under which it was downloaded):

    $ mkdir BUILD
    $ cd BUILD
    $ cmake ..
    $ sudo make install

The directory under which the files are installed defaults to <tt>/usr/local/webos</tt>.
You can install them elsewhere by supplying a value for <tt>WEBOS_INSTALL_ROOT</tt>
when invoking <tt>cmake</tt>. For example:

    $ cmake -D WEBOS_INSTALL_ROOT:PATH=$HOME/projects/openwebos ..
    $ make install

will install the files in subdirectories of <tt>$HOME/projects/openwebos</tt>.

Specifying <tt>WEBOS_INSTALL_ROOT</tt> also causes <tt>pkg-config</tt> to look
in that tree first before searching the standard locations. You can specify
additional directories to be searched prior to this one by setting the
the <tt>PKG_CONFIG_PATH</tt> environment variable.

If not specified, <tt>WEBOS\_INSTALL\_ROOT</tt> defaults to <tt>/usr/local/webos</tt>.

If you need to enable terse logging, then set WEBOS_CONFIG_LOGGING_TERSE to TRUE
when invoking _cmake_. For example:

        $ cmake -D WEBOS_CONFIG_LOGGING_TERSE=TRUE ..

If you need to enable sdk logging, then set WEBOS_CONFIG_LOGGING_SDK to TRUE
when invoking _cmake_. For example:

        $ cmake -D WEBOS_CONFIG_LOGGING_SDK=TRUE ..

To configure for a debug build, enter:

    $ cmake -D CMAKE_BUILD_TYPE:STRING=Debug ..

To see a list of the make targets that <tt>cmake</tt> has generated, enter:

    $ make help

## Uninstalling

From the directory where you originally ran <tt>make install<tt>, enter:

    $ [sudo] make uninstall

You will need to use <tt>sudo</tt> if you did not specify <tt>WEBOS\_INSTALL\_ROOT</tt>.

## Copyright and License Information

All content, including all source code files and documentation files in this repository are:

 Copyright (c) 2010-2012 Hewlett-Packard Development Company, L.P.

All content, including all source code files and documentation files in this repository are:
Licensed under the Apache License, Version 2.0 (the "License");
you may not use this content except in compliance with the License.
You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
