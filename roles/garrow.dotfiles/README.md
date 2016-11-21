# Ansible Role: Dotfiles

A fork of https://github.com/geerlingguy/ansible-role-dotfiles this installs *my* dotfiles, but uses my dotfiles `make` script to install itself.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    dotfiles_repo: "https://github.com/garrow/dotfiles.git"

The git repository to use for retrieving dotfiles. I expect a `Makefile` for the dotfiles to install themselves.

    dotfiles_repo_accept_hostkey: no

Add the hostkey for the repo url if not already added. If ssh_opts contains "-o StrictHostKeyChecking=no", this parameter is ignored.

    dotfiles_repo_local_destination: "~/.dotfiles"

The local path where the `dotfiles_repo` will be cloned.

## Dependencies

None

## Example Playbook

    - hosts: localhost
      roles:
        - { role: garrow.dotfiles }

## License

MIT / BSD

## Author Information

A 2016 fork of [Jeff Geerling](http://jeffgeerling.com/) https://github.com/geerlingguy/ansible-role-dotfiles by Garrow Bedrossian.
