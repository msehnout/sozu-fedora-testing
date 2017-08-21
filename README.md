# Sozu proxy testing with Vagrant

It downloads Sozu from my Copr repository and that's it for now.

The package build is somewhat tricky. First of all the latest release does not have files necessary for packaging, so I had to create the tarball myself. Second important thing is that spec file require "rust-packaging" which is not in Fedora repositories, so you have to add a repository containing this package by hand when setting chroots in Copr.

## Usage

```
$ vagrant up
$ vagrant ssh
```
Inside the box:
```
# sozu start --config /etc/sozu/sozu.toml
```
