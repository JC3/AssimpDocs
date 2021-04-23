# Assimp Documentation

**Library Version:** 5.0.1 (master @ cd42b995)

This is an updated set of libassimp documentation that I've built. I was
*very* liberal with the source directories I chose to include, so this may
or may not contain more than is necessary.

## What's Here?

- *html/index.html*: HTML documentation can be accessed from here.
- *AssimpDoc.chm*: A Windows HTML Help version.
- *Doxyfile*: The Doxygen file used as input (see below).
- *LICENSE*, *CREDITS*: Assimp's legal stuff.

## Where Did This Come From?

I made some updates and tweaks to *Doxyfile.in* from the *doc* subdirectory
of the official assimp source. The *Doxyfile* here is what I used. If you 
want to use it to regenerate the documentation:

1. Place this *Doxyfile* into the assimp source's *doc* directory.
2. Try to keep the *PROJECT_NUMBER* setting updated.
3. Run Doxygen from there.

The following directories from the assimp source tree were used as input:

- */code*
- */include*
- */doc*
- */BINARIES/x64* -- This was my personal 64-bit MSVC build output. But I
  think it should be good enough. 

The following directories from the assimp source tree were used as the
image file paths:

- */doc/AssimpDoc_Html* -- I don't actually know what the "correct" path
  to use was, but the crazy dragon graphic was here post-build, and it
  worked, and now it's here, so... 

Aside from manually replacing cmake vars, I made the following tweaks to
the Doxygen configuration file:

- Updated version number (was "v4.1. (December 2018)")
- A few config options changed, but the "interesting" ones are:
  - ALWAYS_DETAILED_SEC=YES
  - INLINE_INHERITED_MEMB=YES
  - INTERNAL_DOCS=YES
  - SORT_MEMBER_CTORS_1ST=YES
  - SEARCH_ENGINE=YES (for HTML output)
  - BINARY_TOC=YES (for CHM output)

## Why?

The original docs seemed very old and I did not trust them. That's about it.
