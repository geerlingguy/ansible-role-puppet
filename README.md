# Ansible Role: Puppet

[![Build Status](https://travis-ci.org/geerlingguy/ansible-role-puppet.svg?branch=master)](https://travis-ci.org/geerlingguy/ansible-role-puppet)

An Ansible Role that installs [Puppet](https://www.docker.com) on Linux.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    puppet_package: puppetserver

The package to be installed.

    puppet_service: puppetserver
    puppet_service_enabled: no
    puppet_service_manage: no

The service that should be run on this server. By default, this role will not manage a Puppet service, and will not enable it at boot time.

    puppet_bin_path: /opt/puppetlabs/bin

The path to all the Puppet Labs binaries (after the package is installed).

    # Used only for Debian/Ubuntu.
    puppet_apt_deb: "https://apt.puppetlabs.com/puppetlabs-release-pc1-{{ ansible_distribution_release }}.deb"

The .deb file for installation on Debian-based OSes.

    # Used only for RedHat/CentOS.
    puppet_yum_rpm: https://yum.puppetlabs.com/el/7/products/x86_64/puppetlabs-release-7-12.noarch.rpm

The .rpm file for installation on RedHat-based OSes.

## Dependencies

None.

## Example Playbook

    - hosts: all
      roles:
        - geerlingguy.puppet

## License

MIT / BSD

## Author Information

This role was created in 2017 by [Jeff Geerling](https://www.jeffgeerling.com/), author of [Ansible for DevOps](https://www.ansiblefordevops.com/).
