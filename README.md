# Adguard Home

[![CI](https://github.com/DudeCalledBro/adguard/actions/workflows/ci.yml/badge.svg)](https://github.com/DudeCalledBro/adguard/actions/workflows/ci.yml)

In this repository, I am developing and refining the Ansible code for deploying Adguard Home, which I have chosen as a replacement for my previous Pi-hole setup. This transition represents a significant upgrade in my home network's ad-blocking and privacy protection capabilities.

## Prerequisites

- Ensure you have Ansible installed (e.g. `pip3 install ansible`)
- Ensure Docker is installed (you may want to checkout my [ansible-docker-role](https://github.com/DudeCalledBro/ansible-role-docker))

## Setup

Follow these steps to set up your automated Adguard Home deployment:

### Setting Up Your Inventory

1. Navigate to the inventories directory:

    ```bash
    cd inventories
    ```

2. Create a copy of the example hosts file:

    ```bash
    cp example.hosts.yml hosts.yml
    ```

3. Edit the `hosts.yml` file to match your homelab setup:

    ```bash
    vim hosts.yml
    ```

    Customize the file according to your network layout. For example:

    ```yaml
    all:
      hosts:
        server1:
          ansible_host: 192.168.1.10
    ```

    **Notice!** Customize your deployment by overriding default role settings in group or host-specific variable files to precisely configure your Adguard Home setup.

4. Run the Ansible playbook to deploy Adguard:

    ```bash
    ansible-playbook main.yml
    ```

## License

Copyright © 2025 Niclas Spreng

Licensed under the [MIT license](LICENSE).
