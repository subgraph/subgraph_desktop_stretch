# subgraph_desktop_stretch

This is the blue-print for building Subgraph OS installable/live ISOs based
on Debian testing (currently stretch).

The config is generated from live-build 5.x, which is currently in alpha.

## Status

1. debian-installer is not ready for stretch yet, installable ISOs depend on 
this. ISOs should run in live-mode.

2. Subgraph APT repositories are currently not stable or public yet, so it is 
also not currently possible to build SGOS using just this config because it
is missing repository links and Subgraph-specific packages. A lot of things
are added dynamically at build time at this phase while we iron out everything.

3. The list of third-party packages that will ship with the ISO is currently
in flux as we are evaluating what we would like to include and building
metapackages where it is appropriate. 

4. ISOs will not ship until our public repositories are set up and it is
possible to run `apt-get update/upgrade' to download security (and other 
updates). When complete, our aim is that people can use this live-build config
to build their own ISOs.

