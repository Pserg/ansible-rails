# Ansible: Ruby on Rails Server
Use this ansible playbook to setup a fresh server with the following components:

* Nginx
* Puma App Server
* Certbot (Let's Encrypt)
* MySQL or Postgresql
* Memcached
* Redis
* Sidekiq
* Monit (to keep Puma and Sidekiq runnig)
* Elasticsearch
* ruby-install
* chruby
* Directories to deploy Rails with Capistrano and Puma App Server (see below)
* Swapfile (useful for small DO instances)
* Locales
* Tools (tmux, vim, htop, git, wget, curl, nodejs, yarn etc.)

## Prerequisites & Config

1. Rename ```hosts.example``` to ```hosts``` and modify the contents.
2. Rename ```group_vars/all.example``` to ```group_vars/all``` and modify the contents.

	There are a bunch of things you can set in ```group_vars/all```. Don't forget to add your host address to ```hosts```.

## Install Playbook

Run ```ansible-playbook site.yml -i hosts```.
