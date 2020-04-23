Simple tar implementation for PHP
=================================

Design goals
------------

I needed a simple (no external dependencies, no specific php.ini settings) tool that is able to create a verbatim tar archive of a directory, including empty directories, broken symlinks, device files.

This implementation supports the following:
 - empty directories
 - symbolic links (broken/valid)
 - character/block devices
 - arbitrary file name lengths (GNU longlink)

It does not support:
  - FIFOs
  - link targets with a length of 100 or more
