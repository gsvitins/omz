# omz
=====
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

Copyright (c) 2017

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
