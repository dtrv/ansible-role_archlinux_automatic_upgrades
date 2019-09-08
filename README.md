archlinux automatic upgrades
=========

Install script and timer to automatic upgrade arch linux and reboot if necessary.

Requirements
------------

None.

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
