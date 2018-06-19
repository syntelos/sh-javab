
Java package build script following sh-android.


Synopsis

    javab

Description

    This script encapsulates a package build process.

Status

    Work in progress.

Design

    Unanticipated variations in project organization (directory
    structure and file location) are solved by configuration.  

    Refer to the documentation more more information.

Documentation

    Invoking

        2>&1 javab -? | less

    will pipe the help text to the 'less' pager.

Installation

    Prerequisites

	The home 'bin' directory (${HOME}/bin) must exist, and must be
	in the PATH.

    Synopsis

        ./install; echo $?

    Description

	This will attempt to copy the "javab" shell script to
	'${HOME}/bin', and to validate the installation.

    Results

	The installation script will fail (result code "1", not "0")
	when '${HOME}/bin' is not found, or 'which javab' is not
	'${HOME}/bin/javab'.  The installation will also fail when
	the 'which' program is not (properly) installed.

Quick start

    In the root directory of a project, as (for example)

        cd ~/src/some-java-application

    Run

	javab init; echo $?

	javab build; echo $?


    If it fails, the design intent is to remedy the situation by
    testing, probing, and configuration.


Caveats

    This script (creates and) destroys the application project
    (working directory) [sub] directory 'bin'.

References

    https://github.com/syntelos/sh-android
