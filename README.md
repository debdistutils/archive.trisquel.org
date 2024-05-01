# Git LFS mirror of `archive.trisquel.org`

This git repository contains a mirror of
[archive.trisquel.org](https://archive.trisquel.org/), with external
objects stored using [Git LFS](https://git-lfs.com/).

This repository was created using rsync from
`rsync.trisquel.info::trisquel.packages` on 2024-04-27.  The goal is
to keep it in sync with `archive.trisquel.org` going forward.

## Cloning

The Git LFS objects are not available via GitLab, therefor to clone
this repository successfully you will need to disable Git LFS smudging
using the `GIT_LFS_SKIP_SMUDGE=1` environment variable like this:

```
GIT_LFS_SKIP_SMUDGE=1 git clone https://gitlab.com/debdistutils/archives/trisquel/archive.trisquel.org.git
```

# Signature Verification

Commits are signed using [my PGP
key](https://blog.josefsson.org/2019/03/21/openpgp-2019-key-transition-statement/)
with fingerprint:

```
pub   ed25519 2019-03-20 [SC]
      B1D2 BD13 75BE CB78 4CF4  F8C4 D73C F638 C53C 06BE
```

You may view git log and verify commit signatures them as follows:

```
git log --show-signature
```

To verify a single commit use something like this:

```
$ git verify-commit 7de587e3c39692d0ed429899b65b3781c3e30d6b
gpg: Signature made Wed May  1 02:38:38 2024 CEST
gpg:                using EDDSA key A3CC9C870B9D310ABAD4CF2F51722B08FE4745A2
gpg: Good signature from "Simon Josefsson <simon@josefsson.org>" [ultimate]
$ 
```

## Contact

The maintainer is [Simon Josefsson](https://blog.josefsson.org/).
