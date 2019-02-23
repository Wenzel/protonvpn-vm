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

This VM comes with all ProtonVPN servers configuration installed and preconfigured
with your account in an easy to deploy virtual machine.

Server configuration files installed (`TCP`/`UDP`):

- country
- Secure Core
- single server

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

## Maintainers

[@Wenzel](https://github.com/Wenzel)

## Contributing

PRs accepted.

Small note: If editing the Readme, please conform to the [standard-readme](https://github.com/RichardLitt/standard-readme) specification.

## License

[GNU General Public License v3.0](https://github.com/Wenzel/oswatcher/blob/master/LICENSE)
