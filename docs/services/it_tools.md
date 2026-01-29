<!--
SPDX-FileCopyrightText: 2020 - 2024 MDAD project contributors
SPDX-FileCopyrightText: 2020 - 2024 Slavi Pantaleev
SPDX-FileCopyrightText: 2020 Aaron Raimist
SPDX-FileCopyrightText: 2020 Chris van Dijk
SPDX-FileCopyrightText: 2020 Dominik Zajac
SPDX-FileCopyrightText: 2020 Mickaël Cornière
SPDX-FileCopyrightText: 2022 François Darveau
SPDX-FileCopyrightText: 2022 Julian Foad
SPDX-FileCopyrightText: 2022 Warren Bailey
SPDX-FileCopyrightText: 2023 Antonis Christofides
SPDX-FileCopyrightText: 2023 Felix Stupp
SPDX-FileCopyrightText: 2023 Julian-Samuel Gebühr
SPDX-FileCopyrightText: 2023 Nikita Chernyi
SPDX-FileCopyrightText: 2023 Pierre 'McFly' Marty
SPDX-FileCopyrightText: 2024 - 2025 Suguru Hirahara

SPDX-License-Identifier: AGPL-3.0-or-later
-->

# IT-Tools

The playbook can install and configure [IT-Tools](https://sharevb-it-tools.vercel.app/) for you.

IT-Tools is a self-hosted web app offering useful tools for developer and people working in IT.

See the project's [documentation](https://github.com/sharevb/it-tools/blob/main/README.md) to learn what IT-Tools does and why it might be useful to you.

For details about configuring the [Ansible role for IT-Tools](https://codeberg.org/daguwar/ansible-role-it_tools), you can check them via:
- 🌐 [the role's documentation](https://codeberg.org/daguwar/ansible-role-it_tools/src/branch/main/docs/configuring-it_tools.md) online
- 📁 `roles/galaxy/echoip/docs/configuring-it_tools.md` locally, if you have [fetched the Ansible roles](../installing.md)

## Dependencies

This service requires the following other services:

- a [Traefik](traefik.md) reverse-proxy server

## Adjusting the playbook configuration

To enable this service, add the following configuration to your `vars.yml` file and re-run the [installation](../installing.md) process:

```yaml
########################################################################
#                                                                      #
# it_tools                                                             #
#                                                                      #
########################################################################

it_tools_enabled: true

it_tools_hostname: ittools.example.com

########################################################################
#                                                                      #
# /it_tools                                                            #
#                                                                      #
########################################################################
```

## Usage

After running the command for installation, the it_tools instance becomes available at the URL specified with `it_tools_hostname`. With the configuration above, the service is hosted at `https://ittools.example.com`.


## Troubleshooting

See [this section](https://codeberg.org/daguwar/ansible-role-it_tools/src/branch/main/docs/configuring-it_tools.md#troubleshooting) on the role's documentation for details.
