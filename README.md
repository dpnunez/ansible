If you want your Ansible playbook to work on both PCs and Macs, you might need to consider platform-specific tasks and configurations. Here's an updated README.md to reflect this

# Ansible personal environment

Welcome to the Ansible configuration for setting up a new PC/Mac environment swiftly. This project is aimed at automating the setup process for a new computer environment using Ansible, allowing you to get up and running with your preferred configuration as quickly as possible.

## Overview

This Ansible playbook is designed to be platform-agnostic, enabling seamless setup on both PCs and Macs. It includes configurations for various common tools and packages that you may need, tailored for cross-platform compatibility.

## Prerequisites

Before running the Ansible playbook, ensure that you have the following prerequisites installed:

- Ansible
- Git

## Features
- [x] Install ssh key's
- [x] Install Node (via NVM)
- [x] Setup ZSH
- [x] Setup Oh-my-zsh
- [ ] Conditions to MacOS (https://opensource.com/article/22/6/install-software-macos-ansible-homebrew future guide)
- [ ] Install Brew
- [x] Install basic node packages
- [ ] Add .dotfiles (when needed)

 
## Usage

To use this Ansible playbook:

1. Run the following command on your PC/Mac terminal:

    ```bash
    ansible-pull -U [URL_of_this_repository]
    ```

    Replace `[URL_of_this_repository]` with the URL of this repository.

2. You'll be prompted to enter the decryption key for the vault files. Provide the key to proceed with the setup.

3. Sit back and relax while Ansible sets up your PC/Mac environment.

## Testing

To test the configurations provided in this repository, a Dockerfile is available. Follow these steps to test:

1. Build the Docker image:

    ```bash
    ./build-docker
    ```

2. Run the Docker container:

    ```bash
    ./run-docker
    ```

3. Run ansible locally or doing ansible-pull as described above

    locally:
    ```bash
    ansible-playbook local.yml --ask-vault-pass
    ```

    remote:
    ```bash
    ansible-pull -U [URL_of_this_repository]
    ```
## Customization

Feel free to customize this Ansible playbook to suit your needs:

- Modify the `roles` directory to add or remove roles/tasks.
- Edit the variables in the `vars` directory to tailor configurations to your preferences.
- Include additional configuration files or scripts as required.

---

Feel free to reach out if you have any questions or need further assistance with setting up your PC/Mac environment using Ansible. Happy automating!
