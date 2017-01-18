``subpatch``
============

Generate .patch files from a submodule.

Prototype tool that could eventually get incorporated into rdopkg (see
https://github.com/openstack-packages/rdopkg/issues/16)

Usage::

  subpatch <git range>

Example::

  subpatch 7eb4203~..7eb4203

This will generate ``.patch`` files and print some code for you to paste into
your RPM ``.spec`` file.

TODO
----

* Rewrite this in Python

* Do the .spec file manipulations

* Incorporate into rdopkg

* Handle more than one submodule change at a time

* Handle submodules within submodules?
