Role Name
=========

Create and manage Systemd timers

Requirements
------------

The Linux system which is systemd based

Role Variables
--------------

For full example see [vars.yml](molecule/default/vars.yml)
```yaml
red55_systemd_timers:
  - name: "red55.test.1"
    description: "Test Timer"
    exec: "/bin/echo 'Hello, World!'"
    user: root
    group: root
    runtime_dir: "red55.test.1"
    working_dir: "/tmp"
    env:
      TEST_ENV_VAR: "1"
    timer:
      accuracy_sec: "1min"
      persistent: true
      active_sec: "1min"
      boot_sec: "1min"
      startup_sec: "1min"
      randomized_delay_sec: "1min"
      unit_active_sec: "1min"
      unit_inactive_sec: "1min"
      calendar: "Mon *-*-* 00:00:00"
```
Dependencies
------------

There are no special dependencies.

Example Playbook
----------------

See [converge.yml](molecule/default/converge.yml)

License
-------

[BSD Zero Clause License](https://spdx.org/licenses/0BSD.html)
