wiff-snapshot
=============

wiff-snapshot allows you to take "snapshots" of Dynacases' contexts and restore
them.

Snapshot contains:
- context's files
- database's dump
- context's definition from dynacase-control

Snapshot DOES NOT contains:
- vaults

Note:
- This tool is meant for development purposes and might not be suited for
  production use.
- The produced snapshot file is not portable. This means it cannot be restored
  on a machine with different context's root pathnames or database services.
  The snapshot file is meant to be restored on the same machine that took the
  snapshot.

Usage
-----

Take a snapshot of context "foo" into file "foo.snap":

    # ./wiff-snapshot snapshot /var/www/dynacase-control foo foo.snap

Restore snapshot of context "foo" from snapshot file "foo.snap" :

    # ./wiff-snapshot restore /var/www/dynacase-control foo foo.snap

