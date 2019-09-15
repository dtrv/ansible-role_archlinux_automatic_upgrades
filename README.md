archlinux automatic upgrades
=========

Install script and timer to automatic upgrade arch linux and reboot if necessary.

If docker is installed and a running [watchtower](https://containrrr.github.io/watchtower/)
container is found - it will be stopped before `pacman -Syu` and restarted before
system reboot.

Requirements
------------

All applications running on the host should be rebootable.  
You need to take steps so that the automatic upgrade does not interfere with other
upgrade systems because this could bring your arch linux in an unpredictable state.

Role Variables
--------------

| Parameter         | Choices/Defaults  | Comments |
| ----------------- | ----------------- | -------- |
| reboot_timeout    | 60                | seconds to wait after informing all users and reboot |
| timer_on_calendar | `'*-*-* 5:55:55'` | systemd realtime timer argument for `OnCalendar` |


Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
        - role: archlinux_automatic_upgrades
          reboot_timeout: 10
          timer_on_calendar: '*-*-* 1:00:00'


License
-------

MIT

Author Information
------------------

None.
