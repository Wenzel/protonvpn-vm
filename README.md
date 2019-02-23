# protonvpn-vm

[![Join the chat at https://gitter.im/kvm-vmi/Lobby](https://badges.gitter.im/trailofbits/algo.svg)](https://gitter.im/oswatcher/Lobby)
[![standard-readme compliant](https://img.shields.io/badge/readme%20style-standard-brightgreen.svg?style=flat-square)](https://github.com/RichardLitt/standard-readme)

> Preconfigured ProtonVPN setup in a virtual machine

## Table of Contents

- [Overview](#overview)
- [Requirements](#requirements)
- [Usage](#usage)
- [Maintainers](#maintainers)
- [Contributing](#contributing)
- [License](#license)

## Overview

This repo preconfigures your ProtonVPN account in a virtual machine.

- **no configuration**: all ProtonVPN's servers are configured with your credentials (single server/country/secure core)
- **safety**: if the VM's VPN link goes down, your trafic is automatically blocked
  until the link goes back online
- **privacy**: randomize your internet trafic on multiple servers at the same time

## Requirements

- [Packer](https://packer.io/)
- [Ansible](https://www.ansible.com/) >= `2.7.0`

## Usage

Install `ansible` from your distribution's packages.

If you need a more up-to-date version, use `virtualenv`:

    virtualenv venv
    source venv/bin/activate
    (venv) pip install ansible


Build the vm

    packer build -var-file ubuntu-bionic.json ubuntu.json


Log into the VM with the credentials `vagrant/vagrant`


Connect to an `OpenVPN` server:

    sudo openvpn configs/udp/country/ch.protonvpn.com.udp.ovpn

## TODO

How to redirect host trafic to the VM ?

https://github.com/Wenzel/protonvpn-vm/issues/5

## Maintainers

[@Wenzel](https://github.com/Wenzel)

## Contributing

PRs accepted.

Small note: If editing the Readme, please conform to the [standard-readme](https://github.com/RichardLitt/standard-readme) specification.

## License

[GNU General Public License v3.0](https://github.com/Wenzel/oswatcher/blob/master/LICENSE)
