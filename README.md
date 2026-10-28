# NONOS package mirror (GitHub Pages)

It is served as plain HTTP on port 80 at `mirror.nonos.software`, a
custom domain whose CNAME is non-os.github.io, with "Enforce HTTPS" OFF.
The installer GETs:

    http://mirror.nonos.software/linux/<blake3>.tar

It holds every byte to the BLAKE3 the signed Marketplace listing pins,
so the host needs no trust. The files are:

- SimpleX Chat's terminal client;
- DarkFi's drk, darkirc, darkfid and chat app.

`linux/NAMES` maps each hash to its package.

**After sealing,** copy the seal's `<out>/packages/*.tar` into `linux/`
as well: the in-tree tools (tclsh, mruby, rg, fd, gojq, perl, nano,
make, openssl). Then push.

**Limits:** 100 MB per file, the largest here being 79.5 MB, and about
1 GB per site.
