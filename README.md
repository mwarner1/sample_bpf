# sample_bpf
Sample BPF code that works without issue on Mac OS X (a BSD derivative), but fails on Solaris 11.2.

On Mac OS X, clang is the compiler.
On Solaris, it's Solaris Studio 12.3 (you'll need to pass -D__SOLARIS__ to get it to compile).

NOTE: This code has an infinite loop on Solaris (see line 257) because of the EINTR.

This has me banging my head on solid objects. Insights appreciated as to why Solaris produces an EINTR (Interrupted System Call) whereas the Mac sails right through.
