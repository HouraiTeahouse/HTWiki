
# Objective

This guide is intended for those making direct contributions to the project
(i.e. editing the game source files directly) and merging those changes with the
existing project. If you plan on writing code, laying out scenes, designing
charactrer hitboxes etc, this guide will cover how to set up your local
enviroment to work on the game.

If you do not plan on making direct contributions to the project's code or file
structure, we suggest you join [our Discord](https://discord.gg/VuZhs9V)
instead. Asset contributions such as 2D art, 3D models, animations, etc. are
usually sent via chat and stored on the public Google Drive maintained by Hourai
Teahouse. If this is your venue of contribution, the rest of this guide does not
pretain to you and you can safely ignore it.

# Requirements
 
 * A Git Client (see [Setting Up Git](./setting-up-git.md) for more information)
 * Unity3D (version 2018.2.0, using [Unity Hub](https://forum.unity.com/threads/unity-hub-preview-0-18-1-is-now-available.539353/) is highly advised.)

# Setting up the Project

## Creating a GitHub account

The official venue of accepting direct contributions to the project is through
direct commits to the official repository or via GitHub Pull Requests from external
contributors. If you do not already have a GitHub account, you will be required
to [make one](https://github.com/join).

## Setting up your remote repo

If you are a member of the Hourai Teahouse GitHub organization, you are allowed
to directly commit to the official repository, skip this step.

If you are an external contributor, it is suggested that you
[fork](https://help.github.com/articles/fork-a-repo/) the repo onto your own
account.

## Setting up your local files

To get the local files, you'll need to **git clone** the remote repository (the
official one or the fork you have created).

**NOTE:** Fantasy Crescendo, as of writing, currently depends on using many **git
submodules** to manage dependencies. This is a suboptimal solution for
dependency management, but is currently the only available choice we have, even
if it complicates the setup process for the project. Sometime in the future we
will be migrating to the [Unity Package
Manager](https://docs.unity3d.com/Packages/com.unity.package-manager-ui@1.8/manual/index.html)
when it supports 3rd party remote packages, which will remove the need to manage
these submodules.

**Via GitHub for Desktop**

TODO(Gabo7): Document.

**Via Command Line**

This assumes you are using a \*nix (Linux/macOS) style terminal. Windows users
are suggested to use either [Windows Subsystem for
Linux](https://docs.microsoft.com/en-us/windows/wsl/install-win10) (requires
Windows 10) or [GitBash](https://git-scm.com/downloads) 

```bash
git clone https://github.com/HouraiTeahouse/FantasyCrescendo # Clone the
repository
cd FantasyCrescendo # Change directory to the cloned repo
git submodule init --recursive
```
