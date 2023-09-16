# Install and Configure Docker Swarm

An Ansible playbook that installs [Docker](https://www.docker.com) and configures the nodes in swarm mode.

## Requirements

This playbook relies on the following ansible roles.

* geerlingguy.docker

## Usage

  - Clone this repository.
    - `$ git clone https://github.com/glillico/setup-docker-swarm-cluster.git`
  - Change to the repositories directory.
    - `$ cd setup-docker-swarm-cluster`
  - Install required roles.
    - `% ansible-galaxy role install -r requirements.yml`
  - Edit the `inventory.yml` file.
    - Add your nodes to the relavent groups (manager/worker).
    - Change `ANSIBLE_USER_NAME` to be that of your ansible user.
  - Edit the `main.yml` file.
    - Change `DOCKER_USER_NAME` to be the username that will be added to the `docker` group.
  - Run the playbook.
    - `ansible-playbook main.yml`

## License

MIT

## Author Information

Created in 2023 by Graham Lillico.
