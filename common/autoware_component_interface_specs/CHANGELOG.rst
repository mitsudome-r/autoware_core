^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package autoware_component_interface_specs
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Forthcoming
-----------
* chore: align package versions to 1.7.0 and reset changelogs
* Merge remote-tracking branch 'origin/main' into tmp/bot/bump_version_base
* refactor(autoware_core): add USE_SCOPED_HEADER_INSTALL_DIR to common and testing packages (`#967 <https://github.com/mitsudome-r/autoware_core/issues/967>`_)
  Co-authored-by: github-actions <github-actions@github.com>
  Co-authored-by: Junya Sasaki <j2sasaki1990@gmail.com>
* fix(component_interface_specs): change ControlCommand QoS to volatile (`#833 <https://github.com/mitsudome-r/autoware_core/issues/833>`_)
  * fix(component_interface_specs): change ControlCommand QoS durability to volatile
  Change the QoS durability of ControlCommand from TRANSIENT_LOCAL to
  VOLATILE.
  * test(component_interface_spec): update ControlCommand QoS durability to volatile on test
  ---------
  Co-authored-by: Takahisa.Ishikawa <takahisa.ishikawa@tier4.jp>
* Contributors: Takahisa Ishikawa, Vishal Chauhan, github-actions
