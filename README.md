GridFS FUSE
===========

Allows you to mount a MongoDB GridFS instance as a local filesystem.

Requirements
------------

* MongoDB 1.6+
* FUSE
* Boost

For ubuntu users, install:
* mongodb-dev
* libfuse-dev
* libboost-dev
* libboost-system-dev
* libboost-filesystem-dev
* libboost-thread-dev

Building
--------

    $ make

For ubuntu users:
Modify Makefile's -lfuse_ino64 to -lfuse

Usage
-----

    $ ./mount_gridfs --db=db_name --host=localhost --fsnode=fs mount_point
    $ ./mount_gridfs --db=db.storage.voice --host=localhost --fsnode=mp3 mount_point

Current Limitations
-------------------

* No directories
* No permissions or Mongo authentication
* File creation/writing very experimental
