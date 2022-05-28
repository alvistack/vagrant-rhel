# Vagrant Box Packaging for RHEL

<img src="/alvistack.svg" width="75" alt="AlviStack">

[![GitLab pipeline status](https://img.shields.io/gitlab/pipeline/alvistack/vagrant-rhel/master)](https://gitlab.com/alvistack/vagrant-rhel/-/pipelines)
[![GitHub tag](https://img.shields.io/github/tag/alvistack/vagrant-rhel.svg)](https://github.com/alvistack/vagrant-rhel/tags)
[![GitHub license](https://img.shields.io/github/license/alvistack/vagrant-rhel.svg)](https://github.com/alvistack/vagrant-rhel/blob/master/LICENSE)
[![Vagrant Box download](https://img.shields.io/badge/dynamic/json?label=alvistack%2Frhel-9&query=%24.boxes%5B%3A1%5D.downloads&url=https%3A%2F%2Fapp.vagrantup.com%2Fapi%2Fv1%2Fsearch%3Fq%3Dalvistack%2Frhel-9)](https://app.vagrantup.com/alvistack/boxes/rhel-9)

Red Hat Enterprise Linux (often abbreviated to RHEL) is a Linux distribution developed by Red Hat for the commercial market. Red Hat Enterprise Linux is released in server versions for x86-64, Power ISA, ARM64, and IBM Z and a desktop version for x86-64. All of Red Hat's official support and training, together with the Red Hat Certification Program, focuses on the Red Hat Enterprise Linux platform.

Learn more about RHEL: <https://www.redhat.com/en/technologies/linux-platforms/enterprise-linux>

## Supported Boxes and Respective Packer Template Links

  - [`alvistack/rhel-9`](https://app.vagrantup.com/alvistack/boxes/rhel-9)
      - [`packer/rhel-9-libvirt/packer.json`](https://github.com/alvistack/vagrant-rhel/blob/master/packer/rhel-9-libvirt/packer.json)
      - [`packer/rhel-9-virtualbox/packer.json`](https://github.com/alvistack/vagrant-rhel/blob/master/packer/rhel-9-virtualbox/packer.json)
  - [`alvistack/rhel-8`](https://app.vagrantup.com/alvistack/boxes/rhel-8)
      - [`packer/rhel-8-libvirt/packer.json`](https://github.com/alvistack/vagrant-rhel/blob/master/packer/rhel-8-libvirt/packer.json)
      - [`packer/rhel-8-virtualbox/packer.json`](https://github.com/alvistack/vagrant-rhel/blob/master/packer/rhel-8-virtualbox/packer.json)
  - [`alvistack/rhel-7`](https://app.vagrantup.com/alvistack/boxes/rhel-7)
      - [`packer/rhel-7-libvirt/packer.json`](https://github.com/alvistack/vagrant-rhel/blob/master/packer/rhel-7-libvirt/packer.json)
      - [`packer/rhel-7-virtualbox/packer.json`](https://github.com/alvistack/vagrant-rhel/blob/master/packer/rhel-7-virtualbox/packer.json)

## Overview

  - Packaging with [Packer](https://www.packer.io/)
  - Minimal [Vagrant base box implementation](https://www.vagrantup.com/docs/boxes/base)
  - Support [QEMU Guest Agent](https://wiki.qemu.org/Features/GuestAgent)
  - Support [VirtualBox Guest Additions](https://www.virtualbox.org/manual/ch04.html)
  - Support [Vagrant synced folder with rsync](https://www.vagrantup.com/docs/synced-folders/rsync)
  - Support [Vagrant provisioner with Ansible](https://www.vagrantup.com/docs/provisioning/ansible)
  - Standardize disk partition with GPT
  - Standardize file system mount with UUID
  - Standardize network interface with `eth0`

### Quick Start

Once you have [Vagrant](https://www.vagrantup.com/docs/installation) and [VirtaulBox](https://www.virtualbox.org/) installed, run the following commands under your [project directory](https://learn.hashicorp.com/tutorials/vagrant/getting-started-project-setup?in=vagrant/getting-started):

    # Initialize Vagrant
    vagrant init alvistack/rhel-9
    
    # Start the virtual machine
    vagrant up
    
    # SSH into this machine
    vagrant ssh
    
    # Terminate the virtual machine
    vagrant destroy --force

### Molecule

You could also run our [Molecule](https://molecule.readthedocs.io/en/stable/) test cases if you have [Vagrant](https://www.vagrantup.com/) and [Libvirt](https://libvirt.org/) installed, e.g.

    # Run Molecule on RHEL 9
    molecule converge -s rhel-9-libvirt

Please refer to [.gitlab-ci.yml](.gitlab-ci.yml) for more information on running Molecule.

## Versioning

### `YYYYMMDD.Y.Z`

Release tags could be find from [GitHub Release](https://github.com/alvistack/vagrant-rhel/tags) of this repository. Thus using these tags will ensure you are running the most up to date stable version of this image.

### `YYYYMMDD.0.0`

Version tags ended with `.0.0` are rolling release rebuild by [GitLab pipeline](https://gitlab.com/alvistack/vagrant-rhel/-/pipelines) in weekly basis. Thus using these tags will ensure you are running the latest packages provided by the base image project.

## License

  - Code released under [Apache License 2.0](LICENSE)
  - Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)

## Author Information

  - Wong Hoi Sing Edison
      - <https://twitter.com/hswong3i>
      - <https://github.com/hswong3i>
