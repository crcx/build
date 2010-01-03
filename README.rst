=====
build
=====

Description
-----------
This is a small tool for building an application with a minimal
amount of red tape. It allows you to specify compiler flags,
libraries, and dependencies without using a separate file.

Compiling
---------

::

   gcc build.c -o build

Usaging It
----------

::

   build appname

How it works
------------

- open appname.c

- look for the key lines in appname.c

- look for key lines in dependencies of appname.c

- compile everything

Adding to your app
------------------

Linker arguments:

::

   //LIBS -lncurses

Dependencies:

::

   //USES a b c d

a, b, c, and d will be built and linked against appname

Compiler Flags:

::

   //FLAGS -Wall -O3

All of these lines must start in the first column of the code;
indented lines are ignored by build.
