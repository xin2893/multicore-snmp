# Multi-core SNMP Version 0.1.0 #

This is a process based wrapper around the Python binding for Net-SNMP.  It uses multiprocessing from Python 2.6 or greater to create a worker pool that processes SNMP requests.  Net-SNMP with Python bindings are synchronous, but this API solves that problem.

Want to help?  Shoot me an email.

## Example ##
Here is an example of it running on localhost on a mac laptop

```
mac% time python multisnmp.py
Unordered results:
	('Darwin mac.local 9.6.0 Darwin Kernel Version 9.6.0: Mon Nov 24 17:37:00 PST 2008; root:xnu-1228.9.59~1/RELEASE_I386 i386',)
	('Darwin mac.local 9.6.0 Darwin Kernel Version 9.6.0: Mon Nov 24 17:37:00 PST 2008; root:xnu-1228.9.59~1/RELEASE_I386 i386',)
Stopping Process #0
Stopping Process #1
python multisnmp.py  0.18s user 0.08s system 107% cpu 0.236 total

```

## Download ##

You can download the script here:

http://multicore-snmp.googlecode.com/files/multicore_0.1.0.py.zip

Or you can work on a version from the trunk:

http://code.google.com/p/multicore-snmp/source/browse/trunk/multicore.py

## Requirements ##

**Install Python 2.6 or greater, and make sure it is first in your path.  For example, if you just type `python` you should see the python 2.6 prompt.**

**Download and compile Net-SNMP 5.4.2.1 or greater with Python bindings:**

http://www.net-snmp.org/download.html

Make sure you compile with this option **AND** have python2.6 as your default python.

`./configure --with-python-modules`

## To Do ##

A lot.  This is just a quick and dirty proof of concept.  This will be turned into a fairly high level API shortly though.  Stay tuned!