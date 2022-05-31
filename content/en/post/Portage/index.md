---
title: Portage (software)
subtitle: Portage is a package management system

# Summary for listings and search engines
summary: Portage is a package management system originally created for and used by Gentoo Linux and also by Chrome OS, Calculate, Sabayon, and Funtoo Linux among others. Portage is based on the concept of ports collections. Gentoo is sometimes referred to as a meta-distribution due to the extreme flexibility of Portage, which makes it operating-system-independent. The Gentoo/Alt project is concerned with using Portage to manage other operating systems, such as BSDs, macOS and Solaris. The most notable of these implementations is the Gentoo/FreeBSD project.
# Link this post with a project
projects: []

# Date published
date: '2020-12-13T00:00:00Z'

# Date updated
lastmod: '2020-12-13T00:00:00Z'

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
image:
  caption: '[**Logo**](https://www.google.com/url?sa=i&url=https%3A%2F%2Feternalhost.net%2Fblog%2Fsistemnoe-administrirovanie%2Fpaketnye-menedzhery-linux&psig=AOvVaw0TCGE1EtjcR_oaR8fyprLw&ust=1654121956743000&source=images&cd=vfe&ved=0CAkQjRxqFwoTCMDAx8_iivgCFQAAAAAdAAAAABAD)'
  focal_point: ''
  placement: 2
  preview_only: false

authors:
  - admin

tags:
  - Academic

categories:
  - Demo
---


## Overview
<hr>

**Accessing Portage**

Porthole graphical frontend.
Portage is similar to the BSD-style package management known as ports, and was originally designed with FreeBSD's ports in mind. Portage is written in the Python programming language, and is the main utility that defines Gentoo. Although the system itself is known as Portage, it consists of two main parts, the ebuild system and emerge. The ebuild system takes care of the actual work of building and installing packages, while emerge provides an interface to ebuild: managing an ebuild repository, resolving dependencies and similar issues. (These two therefore have roughly the same relation as rpm has with yum, or dpkg has with APT.)

A GTK+-based GUI, Porthole, is available for working with Portage. There is also the Himerge GUI, which stands for "Haskell Interface for eMerge".

**Functions provided**

Portage is characterized by its main function: compiling from source code the packages the user wishes to install. In doing so it allows customization of compiler and target-application options to fit the system's specifications and the user's own wishes. Functionalities related to system management include: allowing parallel package-version installation, tracking cross-package dependencies, managing a database of installed packages, providing a local ebuild repository, and synchronizing of the local Portage tree with remote repositories. Functionalities related to individual package installation include: specifying compilation settings for the target machine and choosing package components.

Portage distinguishes between three levels of stability in ebuilds: stable (e.g., the software works as intended with no known security issues at time of release), keyword masked (mainly for packages that have not been sufficiently tested on the target system architecture to be considered stable) and hard masked (broken or very insecure) packages.


## Features
<hr>

**Emerge**

Unmerge of SpaceFM file manager
The emerge command-line tool is the heart of Portage. The command is customizable with many options and modifiers. The emerge tool is the most important utility for accessing the features of Portage from the command line.

The program calculates and manages dependencies, executes ebuilds and maintains the local Portage tree and database of installed packages. The compilation settings used by ebuilds can be changed through the CFLAGS environment variable, based on the specifications of the individual computer and on the user's desire for optimization. The emerge utility executes ebuilds in a sandbox environment. This way the system is protected from software executed by the ebuild and resulting binaries are only merged after a successful build and sandboxed install.

What emerge installs as dependencies is affected by the USE flag-settings. They decide which optional features will be included when installing or upgrading an application. The emerge command can also be used to download and install precompiled binary files.

**USE flags**

Portage during system update
The Portage system offers the use of "USE flags", which allows users to indicate which software features they would like to include (and exclude) while building packages. For example, there is a USE flag to include DVD support, where available, in packages compiled with the flag enabled. The USE flags affect which dependencies are required, generally affecting which optional features will be built into a given program when it is compiled. For example, in packages which use a configure script, the USE flag feature would translate to ./configure --with-feature.

The specification of USE flags is the usual way to configure programs on Gentoo. USE flags may be set manually, or via user-friendly tools such as 'ufed' (USE flag editor), which lists flags along with their description. A list of available USE flags is available at the Gentoo website's USE Flag Index.

**Emerge**

Unmerge of SpaceFM file manager
The emerge command-line tool is the heart of Portage. The command is customizable with many options and modifiers. The emerge tool is the most important utility for accessing the features of Portage from the command line.

The program calculates and manages dependencies, executes ebuilds and maintains the local Portage tree and database of installed packages. The compilation settings used by ebuilds can be changed through the CFLAGS environment variable, based on the specifications of the individual computer and on the user's desire for optimization. The emerge utility executes ebuilds in a sandbox environment. This way the system is protected from software executed by the ebuild and resulting binaries are only merged after a successful build and sandboxed install.

What emerge installs as dependencies is affected by the USE flag-settings. They decide which optional features will be included when installing or upgrading an application. The emerge command can also be used to download and install precompiled binary files.

**USE flags**

Portage during system update
The Portage system offers the use of "USE flags", which allows users to indicate which software features they would like to include (and exclude) while building packages. For example, there is a USE flag to include DVD support, where available, in packages compiled with the flag enabled. The USE flags affect which dependencies are required, generally affecting which optional features will be built into a given program when it is compiled. For example, in packages which use a configure script, the USE flag feature would translate to ./configure --with-feature.

The specification of USE flags is the usual way to configure programs on Gentoo. USE flags may be set manually, or via user-friendly tools such as 'ufed' (USE flag editor), which lists flags along with their description. A list of available USE flags is available at the Gentoo website's USE Flag Index.

**ebuild**
Gentoo does not, by default, use binary packages as other package management systems do (like pacman or apt), employing instead a format known as the ebuild. Whereas RPM binaries are precompiled binaries, ebuilds are shell scripts with variables and functions which contain a description of the software, and instructions on how to obtain, configure, compile, and install it, more closely akin to (but more powerful than) the .spec files distributed in SRPMs.[8] There are over 19,000 ebuilds available, the majority of which are distributed by the Gentoo mirrors. New and updated ebuilds can be obtained by synchronizing the local ebuild repository with the mirrors. This is done by executing the command emerge --sync. Historically, Gentoo has provided pre-compiled binary packages for many common programs, especially those which are lengthy to compile, such as Mozilla Firefox and OpenOffice.org. These are still installed with emerge, just by appending a "-bin" to the package name to instead install the binary version.

**Binary packages**

Gentoo does have a binary packaging format, which is a .tbz2 file (tar with bzip2 compression) with additional metadata. This feature enables the building of binary packages on one system (using Portage's buildpkg or quickpkg) followed by quick installation on other, identical systems (with Portage's getbinpkg or emerge -K). See Portage Features in the Gentoo Linux Handbook for more information.

**Masking**

Masking is how Gentoo determines which packages are suitable for a system. Ebuilds designed for different architectures or experimental software are usually masked in a manner which prevents a stable system from installing them without user intervention.

Packages that generally just require some testing but will often work fine are said to be keyword masked (i.e. they are available for systems with an ACCEPT_KEYWORDS make.conf entry starting with the character ~, such as ~x86, ~amd64, ~ppc). The standard way to unmask an individual keyword masked package is by adding a file with the full package name and keyword to /etc/portage/package.accept_keywords/. Users can make subdirectories here as well, allowing for custom organization. For example, if a masked package had multiple masked dependencies, the user could make a directory with the name of the original masked package, and put all the mask files for the package and its dependencies in that directory. This scheme replaces the older scheme of having /etc/portage/package.accept_keywords as a text file list.

Packages with known problems or not considered mature enough to be candidates for stable are hard masked by one of the various package.mask files in /usr/portage/profiles, and such entries are generally accompanied by a comment from developers explaining the reason for the mask.



