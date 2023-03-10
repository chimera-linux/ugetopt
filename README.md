# ugetopt

This is a standalone version of the `getopt` program from the `util-linux`
suite (https://en.wikipedia.org/wiki/util-linux).

It supports all the features of the regular version, minus currently:

* NLS

Current Git revision: `a6c81d6103d1e6acda4c6473b258cc785628671b`

It is a single-file implementation, primarily configured for Chimera Linux's
`musl` environment, but it should be functional on any Linux system. It is
somewhat less portable than the upstream version, primarily due to a much
simpler build system that makes assumptions.

The primary reason for separation is so that it can be used in environments
that do not use `util-linux`, and so that it can be compiled with stricter
hardening flags that upstream `util-linux` suite cannot be built with.

## Licensing

Same as upstream, i.e. GPL 2.0 or any later version.
