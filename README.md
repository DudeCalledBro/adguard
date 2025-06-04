# Adguard Home

[![CI](https://github.com/DudeCalledBro/adguard/actions/workflows/ci.yml/badge.svg)](https://github.com/DudeCalledBro/adguard/actions/workflows/ci.yml)

In this repository, I am developing and refining the Ansible code for deploying Adguard Home, which I have chosen as a replacement for my previous Pi-hole setup. This transition represents a significant upgrade in my home network's ad-blocking and privacy protection capabilities.

## Prerequisites

- Ensure you have Ansible installed (e.g. `pip3 install ansible`)
- Ensure Docker is installed (you may want to checkout my [ansible-docker-role](https://github.com/DudeCalledBro/ansible-role-docker))

## Setup

Before running the playbook, you'll need to configure the deployment by setting up the necessary inventory and configuration files.

1. Copy the example inventory file to `inventory.yml`:

    ```bash
    cp example.inventory.yml inventory.yml
    ```

2. Run the Ansible playbook to deploy Adguard:

    ```bash
    ansible-playbook main.yml
    ```

## License

Copyright © 2025 Niclas Spreng

Licensed under the [MIT license](LICENSE).
