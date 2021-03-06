# Vagrant Box Packaging for RHEL

## YYYYMMDD.Y.Z - TBC

### Major Changes

## 20210718.1.1 - 2021-07-18

### Major Changes

  - Upgrade minimal Ansible community package support to 4.2.0

## 20210602.1.1 - 2021-06-02

### Major Changes

  - Initialize with `verify.yml` with first start
  - Support RHEL 8.4
  - Upgrade minimal Ansible support to 4.0.0

## 20210313.1.1 - 2021-03-13

### Major Changes

  - Bugfix [ansible-lint
    `namespace`](https://github.com/ansible-community/ansible-lint/pull/1451)
  - Bugfix [ansible-lint
    `no-handler`](https://github.com/ansible-community/ansible-lint/pull/1402)
  - Bugfix [ansible-lint
    `unnamed-task`](https://github.com/ansible-community/ansible-lint/pull/1413)

## 20210224.1.0 - 2021-02-24

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
