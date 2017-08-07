# Ansible Role: Beetbox Modx

[![CircleCI](https://circleci.com/gh/beetboxvm/ansible-role-beetbox-modx.svg?style=svg)](https://circleci.com/gh/beetboxvm/ansible-role-beetbox-modx)

An Ansible role that creates and installs a Modx project on beetbox.

## Requirements

This role is specifically developed as an extension to beetbox -- https://github.com/drupalmel/beetbox

## Role Variables

Available variables are listed below, along with default values:

Checkout Modx project.

    modx_checkout: no
    
Modx project git respository.
    
    modx_repo: "http://github.com/modxcms/revolution.git"
    
Modx project version. This can be the full 40-character SHA-1 hash, the literal string HEAD, a branch name, or a tag name.
    
    modx_version: "HEAD"
    
Modx checkout depth. git is history truncated to the specified number or revisions
    
    modx_checkout_depth: 1

Install Modx project.

    modx_install_site: no
    
Modx admin account name.
    
    modx_account_name: admin
    
Modx admin account password.    
    
    modx_account_pass: admin
    
Modx admin account email.    
    
    modx_account_mail: "email@address.com"
    
Modx extra install options...    
    
    modx_manager_language: en
    modx_database_connection_charset: "utf8"
    modx_database_charset: "utf8"
    modx_database_collation: "utf8_general_ci"
    modx_https_port: 443
    modx_cache_disabled: 0
    modx_table_prefix: "modx_"
    modx_mgr_url: "/manager/"
    modx_connectors_url: "/connectors/"
    modx_web_url: "/"
    modx_remove_setup_directory: 0


# beetbox

https://github.com/beetboxvm/beetbox

## Requirements

* [Composer](https://getcomposer.org/download/)
* [Vagrant](https://www.vagrantup.com/) >= 1.8
* [Virtualbox](https://www.virtualbox.org/)
* [Vagrant Hostsupdater](https://github.com/cogitatio/vagrant-hostsupdater)
* [Vagrant Auto-network](https://github.com/oscar-stack/vagrant-auto_network)

## Quickstart

  1. Open terminal (or [git bash](https://msysgit.github.io/) for windows users) and run the following commands --

  ```
  git clone https://github.com/beetboxvm/ansible-role-beetbox-modx.git modx && cd $_
  composer require --dev beet/box
  vagrant up
  ```

  2. Go to http://modx.local/

  ```
  username: admin
  password: admin
  ```

## License

MIT
