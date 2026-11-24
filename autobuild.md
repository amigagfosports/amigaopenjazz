# Autobuild

How LumaVAULT's nightly build (bigguy, 23:00 to 06:00) builds this repository. The form is in lumavault-server
`docs/AUTOBUILD.md`.

## amigaopenjazz

The port, built from main by its own `package/build-amiga.sh` with the nightly's GFOpenAmigaGCC stove (open9, given
as `STOVE`), the way the open9 rebuild (GF-109) built vgit-a1626f4-amigaos3-rc1 on 23 November in 33 seconds. The script makes its
archive in `build-amiga-package/`, which is what the nightly keeps. Weekly, because a port moves slowly: change it
to `nightly` while the port is being worked on, or `never` to take it off the list.

- frequency: weekly
- kind: app
- script: package/build-amiga.sh
- keep: build-amiga-package/*.lha build-amiga-package/*.readme
- minutes: 30
