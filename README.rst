``subpatch``
============

Generate .patch files from a submodule.

Prototype tool that could eventually get incorporated into rdopkg (see
https://github.com/openstack-packages/rdopkg/issues/16)

Usage::

  git checkout ceph-7.0-rhel-patches
  subpatch <git range>

Example: To check the entire ``-patches`` branch for submodule changes
downstream::

  subpatch v18.2.0..ceph-7.0-rhel-patches

Example: Check one single ``-patches`` branch change::

  subpatch 7eb4203~..7eb4203

This will generate ``.patch`` files and print some code for you to paste into
your RPM ``.spec`` file.

TODO
----

* Do the .spec file manipulations

* Incorporate into rdopkg

* Handle more than one submodule change at a time

* Handle submodules within submodules?
