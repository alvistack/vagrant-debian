# Vagrant Box Packaging for Debian

<a href="https://alvistack.com" title="AlviStack" target="_blank"><img src="/alvistack.svg" height="75" alt="AlviStack"></a>

[![GitLab pipeline
status](https://img.shields.io/gitlab/pipeline/alvistack/vagrant-debian/master)](https://gitlab.com/alvistack/vagrant-debian/-/pipelines)
[![GitHub
tag](https://img.shields.io/github/tag/alvistack/vagrant-debian.svg)](https://github.com/alvistack/vagrant-debian/tags)
[![GitHub
license](https://img.shields.io/github/license/alvistack/vagrant-debian.svg)](https://github.com/alvistack/vagrant-debian/blob/master/LICENSE)
[![Vagrant Box
download](https://img.shields.io/badge/dynamic/json?label=alvistack%2Fdebian-12&query=%24.boxes%5B%3A1%5D.downloads&url=https%3A%2F%2Fapp.vagrantup.com%2Fapi%2Fv1%2Fsearch%3Fq%3Dalvistack%2Fdebian-12)](https://app.vagrantup.com/alvistack/boxes/debian-12)

Debian is an operating system which is composed primarily of free and
open-source software, most of which is under the GNU General Public
License, and developed by a group of individuals known as the Debian
project. Debian is one of the most popular Linux distributions for
personal computers and network servers, and has been used as a base for
several other Linux distributions.

Learn more about Debian: <https://debian.org/>

## Supported Boxes and Respective Packer Template Links

- [`alvistack/debian-testing`](https://app.vagrantup.com/alvistack/boxes/debian-testing)
  - [`packer/debian-testing-libvirt/packer.json`](https://github.com/alvistack/vagrant-debian/blob/master/packer/debian-testing-libvirt/packer.json)
  - [`packer/debian-testing-virtualbox/packer.json`](https://github.com/alvistack/vagrant-debian/blob/master/packer/debian-testing-virtualbox/packer.json)
- [`alvistack/debian-12`](https://app.vagrantup.com/alvistack/boxes/debian-12)
  - [`packer/debian-12-libvirt/packer.json`](https://github.com/alvistack/vagrant-debian/blob/master/packer/debian-12-libvirt/packer.json)
  - [`packer/debian-12-virtualbox/packer.json`](https://github.com/alvistack/vagrant-debian/blob/master/packer/debian-12-virtualbox/packer.json)
- [`alvistack/debian-11`](https://app.vagrantup.com/alvistack/boxes/debian-11)
  - [`packer/debian-11-libvirt/packer.json`](https://github.com/alvistack/vagrant-debian/blob/master/packer/debian-11-libvirt/packer.json)
  - [`packer/debian-11-virtualbox/packer.json`](https://github.com/alvistack/vagrant-debian/blob/master/packer/debian-11-virtualbox/packer.json)

## Overview

- Packaging with [Packer](https://www.packer.io/)
- Minimal [Vagrant base box
  implementation](https://www.vagrantup.com/docs/boxes/base)
- Support [QEMU Guest
  Agent](https://wiki.qemu.org/Features/GuestAgent)
- Support [VirtualBox Guest
  Additions](https://www.virtualbox.org/manual/ch04.html)
- Support [Vagrant synced folder with
  rsync](https://www.vagrantup.com/docs/synced-folders/rsync)
- Support [Vagrant provisioner with
  Ansible](https://www.vagrantup.com/docs/provisioning/ansible)
- Standardize disk partition with GPT
- Standardize file system mount with UUID
- Standardize network interface with `eth0`

### Quick Start

Once you have [Vagrant](https://www.vagrantup.com/docs/installation) and
[VirtaulBox](https://www.virtualbox.org/) installed, run the following
commands under your [project
directory](https://learn.hashicorp.com/tutorials/vagrant/getting-started-project-setup?in=vagrant/getting-started):

    # Initialize Vagrant
    vagrant init alvistack/debian-12

    # Start the virtual machine
    vagrant up

    # SSH into this machine
    vagrant ssh

    # Terminate the virtual machine
    vagrant destroy --force

### Molecule

You could also run our
[Molecule](https://molecule.readthedocs.io/en/stable/) test cases if you
have [Vagrant](https://www.vagrantup.com/) and
[Libvirt](https://libvirt.org/) installed, e.g.

    # Run Molecule on Debian 12
    molecule converge -s debian-12-libvirt

Please refer to [.gitlab-ci.yml](.gitlab-ci.yml) for more information on
running Molecule.

## Versioning

### `YYYYMMDD.Y.Z`

Release tags could be find from [GitHub
Release](https://github.com/alvistack/vagrant-debian/tags) of this
repository. Thus using these tags will ensure you are running the most
up to date stable version of this image.

### `YYYYMMDD.0.0`

Version tags ended with `.0.0` are rolling release rebuild by [GitLab
pipeline](https://gitlab.com/alvistack/vagrant-debian/-/pipelines) in
weekly basis. Thus using these tags will ensure you are running the
latest packages provided by the base image project.

## License

- Code released under [Apache License 2.0](LICENSE)
- Docs released under [CC BY
  4.0](http://creativecommons.org/licenses/by/4.0/)

## Author Information

- Wong Hoi Sing Edison
  - <https://twitter.com/hswong3i>
  - <https://github.com/hswong3i>
