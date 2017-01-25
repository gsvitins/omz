# omz

[![Build Status](https://travis-ci.org/gsvitins/omz.svg?branch=master)](https://travis-ci.org/gsvitins/omz)
[![Ansible Galaxy](https://img.shields.io/badge/galaxy-gsvitins.omz-lightgrey.svg)](https://galaxy.ansible.com/gsvitins/omz/)

Ansible role to install zsh and setup [oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh) freamework.
It can  be used to setup zsh shell for multiple users at once, including root.
It uses [oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh)  framework as base for zsh configs/themes/plugins/etc.

Role variables
--------------
```yaml
    omz_users: []
    omz_root: true
    omz_chsh: true
    zsh_path: "/bin/zsh"
    omz_theme: "candy"
    omz_case_sensitive_completion: false
    omz_hyphen_insensitive_completion: false
    omz_disable_auto_update: false
    omz_auto_update_interval: 30
    omz_disable_ls_colors: false
    omz_disable_auto_title: false
    omz_enable_auto_correction: true
    omz_completion_waiting_dots: true
    omz_history_stamps: "yyyy-mm-dd"
    omz_plugins: "docker git vagrant vi-mode nmap rsync"
    omz_language: "en_US.UTF-8"
```
Examples
--------
```yaml
- hosts: all
  roles:
      - { role: omz,
          omz_users: [user1, user2],
          omz_theme: "cloud",
          omz_completion_waiting_dots: false
        }
```
License
-------
MIT License

Dependencies
------------
None
