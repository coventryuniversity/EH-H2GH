Hitchhiker's Guide to Ethical Hacking
=====================================

A Field manual created by students and staff on the Coventry University Ethical Hacking course.


Working On the H2GH
====================

Below is an quick overview of how to contribute to the guide. 
Further details can be found in the guide itself (how meta is that)

Getting Started
----------------

1) Fork the repository
   In Github click "Fork" (top right) 

2) Download your Forked repository 

```bash
$ git clone <url>
```

3) <optional> Create a Feature Branch

```bash
$ git branch <feature>
$ git checkout <feature>
```

Setup the working environment
------------------------------

1) Create a new virtualenv http://docs.python-guide.org/en/latest/dev/virtualenvs/

...bash
$ virtualenv --no-site-packages env
...

2) Enter the virtualenv

...bash
$ source env/bin/activate
...

3) Install any dependencies

...bash
(env)$ pip install sphinx
....

Building the Documents
-----------------------

The documents can be compiled using the makefile.
Several build options exist, but for the moment we will use HTML

...bash
(env)$ make html
...

The output is available in *build/html*


Submitting Updates
==================

TODO:
=====

Contributors
=============

@djgoldsmith