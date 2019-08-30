Ansible Role: monit
=========

Deploy `Monit` with scripts for notification about problems via `Telegram` and `Mattermost` on RedHat/CentOS or Debian/Ubuntu.

Requirements
------------

None.

Role Variables
--------------
Available variables are listed below, along with default values (see `defaults/main.yml`):

Variable | Description
---------|---------
 `mattermost_url` | URL of the Mattermost (e.g. `mattermost.example.com`)
 `mattermost_ssl` | Boolean. Use `http://` when it set as `Fasle` or `https://` when `True`. False by defaults.
 `mattermost_webhook` | Incoming webhook for mattermost (e.g. `riq39tf6nd8a8b7hme93rcsoto` )
 `mattermost_channel` | The name of the Mattermost channel where Monit will send alerts
 `mattermost_notifications` | String for notification of responsible persons (Mattermost usernames, e.g. `"vbubunov, uname1, ..."`)
 `tg_token` | Telegram token
 `tg_chatID` | Telegram chat ID (e.g. `-226404626`)
 `tg_notifications` | String for notification of responsible persons (Telegram usernames, e.g. `"@LainEverywhere, @Username1, ..."`)
 
Dependencies
------------

None.

Example Playbook
----------------

    - hosts: servers
      vars:
      // Plase your vars here
      roles:
         - { role: monit }

License
-------

BSD

Author Information
------------------

This role was created in 2019 by [Vlad Bubnov](https://github.com/Faust13).
