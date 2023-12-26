# libslirp
A user-mode networking library used by virtual machines, containers or various tools.

This is an optional dependency of the QEMU KCP package. The other recommended deps are libspice, usbredir, and libvirglrenderer. You can install all of them like this:

```
kcp -u
kcp -i libspice
kcp -i usbredir
kcp -i libslirp
kcp -i libvirglrenderer
```
