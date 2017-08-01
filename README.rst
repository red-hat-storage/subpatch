``subpatch``
============

Generate .patch files from a submodule.

Prototype tool that could eventually get incorporated into rdopkg (see
https://github.com/openstack-packages/rdopkg/issues/16)

Usage::

  git checkout ceph-2-rhel-patches
  subpatch <git range>

Example::

  subpatch 7eb4203~..7eb4203

This will generate ``.patch`` files and print some code for you to paste into
your RPM ``.spec`` file.

An example that could fit with rdopkg::

  subpatch v10.2.5~..ceph-2-rhel-patches

This would check the entire "-patches" branch for submodule changes downstream.

TODO
----

* Do the .spec file manipulations

* Incorporate into rdopkg

* Handle more than one submodule change at a time

* Handle submodules within submodules?

* Integration with Debian packaging / `rhcephpkg
<https://github.com/red-hat-storage/rhcephpkg>`_
