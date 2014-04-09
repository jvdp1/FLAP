# FLAP
### FLAP, Fortran command Line Arguments Parser for poor men

A very simple and stupid tool for building easily nice Command Line Interface for modern Fortran projects.

### A Taste of FLAP

Running the test program a taste of FLAP is served:
```bash
+--> flap_test, a testing program for FLAP library
+--> Parsing Command Line Arguments
|--> Error: the Command Line Interface requires at least 1 arguments to be passed whereas only 0 have been!
|--> The Command Line Interface (CLI) has the following options
|-->   FLAP_Test -string value [-integer value] [-real value] [-boolean]
|--> Each Command Line Argument (CLA) has the following meaning:
|-->   [-string value] or [-s value]
|-->     String input
|-->     It is a non optional CLA thus must be passed to CLI
|-->   [-integer value] or [-i value]
|-->     Integer input
|-->     It is a optional CLA which default value is "-1"
|-->   [-real value] or [-r value]
|-->     Real input
|-->     It is a optional CLA which default value is "1.0"
|-->   [-boolean] or [-b]
|-->     Boolean input
|-->     It is a optional CLA which default value is ".false."
|--> Usage examples:
|-->   -) flap_test -s 'Hello FLAP'
|-->   -) flap_test -s 'Hello FLAP' -i -2
|-->   -) flap_test -s 'Hello FLAP' -i -2 -r 33.d0
|-->   -) flap_test -string 'Hello FLAP' -boolean
```

## Table of Contents

* [Team Members](#team-members)
* [What is FLAP?](#what)
* [Main features](#main-features)
* [Todos](#todos)
* [Requirements](#requirements)
* [Copyrights](#copyrights)
* [Usage](#usage)

## <a name="team-members"></a>Team Members
* Stefano Zaghi <stefano.zaghi@gmail.com>

## <a name="what"></a>What is FLAP?

Modern Fortran standards (2003+) have introduced support for Command Line Arguments (CLA), thus it is possible to construct nice and effective Command Line Interface (CLI). FLAP is a small library designed to simplify the (repetitive) construction of complicated CLI in pure Fortran (standard 2003+). FLAP has been inspired by the python module _argparse_ trying to mimic it. Once you have defined what arguments are required setting up the CLI through a user-friendly methods, FLAP will parse the CLAs for you. It is worthy of note that FLAP, as _argparse_, also automatically generates help and usage messages and issues errors when users give the program invalid arguments.

## <a name="main-features"></a>Main features
+ user-friendly methods for building flexible and effective Command Line Interfaces (CLI);
+ handling optional and non optional Command Line Argument (CLA);
+ handling boolean CLA;
+ automatic generation of help and usage messages;
+ errors trapping for invalid CLI usage.
+ ...

## <a name="todos"></a>Todos
+ Support for positional CLAs;
+ support for multiple valued (list of values) CLAs.
+ ...

## <a name="requirements"></a>Requirements
+ Modern Fortran Compiler (standard 2003+);
+ a lot of patience with the author.

FLAP is developed on a GNU/Linux architecture. For Windows architecture there is no support, however it should be work out-of-the-box.

## <a name="Copyrights"></a>Copyrights

FLAP is an open source project, it is distributed under the [GPL v3](http://www.gnu.org/licenses/gpl-3.0.html). Anyone is interest to use, to develop or to contribute to FLAP is welcome.

## <a name="usage"></a>Usage
