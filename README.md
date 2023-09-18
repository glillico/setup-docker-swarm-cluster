# Install and Configure Docker Swarm

An Ansible playbook that installs [Docker](https://www.docker.com) and configures the nodes in swarm mode.

## Requirements

This playbook relies on the following ansible roles.

  - [geerlingguy.docker](https://github.com/geerlingguy/ansible-role-docker/ )

## Usage

  - Clone this repository.
    - `$ git clone https://github.com/glillico/setup-docker-swarm-cluster.git`
  - Change to the repositories directory.
    - `$ cd setup-docker-swarm-cluster`
  - Install required roles.
    - `% ansible-galaxy role install -r requirements.yml`
  - Copy the `example.inventory.yml` file to `inventory.yml`.
  - Edit the `inventory.yml` file.
    - Add your nodes to the relavent groups (manager/worker).
    - Change the value of `ansible_user` to be that of your ansible user.
  - Copy the `example.config.yml` file to `config.yml`.
  - Edit the `config.yml` file.
    - Change the value of `docker_users` to be the username(s) that will be added to the `docker` group.
  - Run the playbook.
    - `ansible-playbook main.yml`

## License

MIT

## Author Information

Created in 2023 by Graham Lillico.
