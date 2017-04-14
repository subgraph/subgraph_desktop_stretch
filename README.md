# subgraph_desktop_stretch

This is the blue-print for building Subgraph OS installable/live ISOs based
on Debian Testing.

## Build pre-requisites

The following Debian packages need to be installed in your build environment 
in order to build an ISO:

```
$ sudo apt-get install live-build live-config live-boot live-boot-initramfs-tools
```

We do suggest you build from a VM or container. 

`apt-cacher-ng` may also help speed up builds -- but setting it up is left as 
an exercise for the avid live-builder.

We also strongly recommend that you familiarize yourself with the 
[live-build manual](https://debian-live.alioth.debian.org/live-manual/stable/manual/html/live-manual.en.html).

## Building an ISO

To build an ISO, run the following commands:
```
$ lb clean --purge
$ lb config
$ lb build
```

## Troubleshooting

In theory, the configuration contained in this repo will build a complete ISO.
However, there may be cases where live-build fails to successfully complete a 
build.

The build may fail for a number of reasons:

- Dependencies removed from Debian
- Debian repo probz
- `debian-installer` is not building (therefore, unavailable for installation 
into the ISO)
- Failure to anoint your keyboard with bat guano (or whatever you normally 
do to get your mojo workin')

- Etc.

We are also subject to these variables. We don't maintain the `live-build` 
software, so barring any bugs in our configuration and our packages, build 
failures are not something we exert much control over. For this reason, we don't
officially support people building third-party ISO builds. Chances are if
there is a problem we can control, we already know about it and will commit
changes to this repo or packages in our APT repo.

If you do encounter difficulties, you may be able to determine the cause by 
consulting one of the following resources:

- The Debian [live-build bug tracker](https://bugs.debian.org/cgi-bin/pkgreport.cgi?src=live-build) 
- The [debian-live mailing list](https://lists.debian.org/debian-live/)
- Your worldview-specific expert of choice in matters of superstition

## Bugs

Of course, if you have done the leg-work and determined that there was a bug
in something we do control, we will be happy to fix it. But we would appreciate
if all other avenues of inquiry have been exhausted first. Only report it to us
if you are highly confident that it is something we can fix.

