^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package autoware_behavior_velocity_stop_line_module
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1.8.0 (2026-05-01)
------------------
* chore: align package versions to 1.7.0 and reset changelogs
* Merge remote-tracking branch 'origin/main' into tmp/bot/bump_version_base
* fix(autoware_behavior_velocity_stop_line_module): fix bugprone-unchecked-optional-access (`#900 <https://github.com/mitsudome-r/autoware_core/issues/900>`_)
  * fix(autoware_behavior_velocity_stop_line_module): fix bugprone-unchecked-optional-access warnings
  * feat(autoware_behavior_velocity_stop_line_module): improve code robustness
  Co-authored-by: Ryohsuke Mitsudome <43976834+mitsudome-r@users.noreply.github.com>
  * feat(autoware_behavior_velocity_stop_line_module): improve code robustness by optional value check and setting
  Co-authored-by: Ryohsuke Mitsudome <43976834+mitsudome-r@users.noreply.github.com>
  * fix(autoware_behavior_velocity_stop_line_module): fix wrong variable name
  Co-authored-by: Mete Fatih Cırıt <mfc@autoware.org>
  ---------
* test(autoware_behavior_velocity_stop_line_module): add test cases (`#486 <https://github.com/mitsudome-r/autoware_core/issues/486>`_)
* chore(planning, bvp): remove unused lanelet2_extension header (`#902 <https://github.com/mitsudome-r/autoware_core/issues/902>`_)
  * remove unused lanelet2_extension in bvp modules
  * remove unused lanelet2_extension in planning components
  ---------
* feat(autoware_trajectory): define set stopline in Trajectory class (`#806 <https://github.com/mitsudome-r/autoware_core/issues/806>`_)
* chore: organize maintainer (`#858 <https://github.com/mitsudome-r/autoware_core/issues/858>`_)
* Contributors: NorahXiong, Sarun MUKDAPITAK, Satoshi OTA, github-actions
