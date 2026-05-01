^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package autoware_motion_velocity_planner_common
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1.8.0 (2026-05-01)
------------------
* chore: align package versions to 1.7.0 and reset changelogs
* Merge remote-tracking branch 'origin/main' into tmp/bot/bump_version_base
* fix(motion_velocity_planner): fix Unnecessary Copy Assignment Movable (`#813 <https://github.com/mitsudome-r/autoware_core/issues/813>`_)
* fix(autoware_motion_velocity_planner_common): fix bugprone-unchecked-optional-access warnings (`#895 <https://github.com/mitsudome-r/autoware_core/issues/895>`_)
* fix(autoware_motion_velocity_planner_common): fix bugprone-narrowing-conversions warnings (`#928 <https://github.com/mitsudome-r/autoware_core/issues/928>`_)
  * fix(autoware_motion_velocity_planner_common): fix bugprone-narrowing-conversions warnings
  * style(pre-commit): autofix
  ---------
  Co-authored-by: pre-commit-ci[bot] <66853113+pre-commit-ci[bot]@users.noreply.github.com>
* fix(autoware_motion_velocity_planner_common): avoid -Wmaybe-uninitialized warning on arm64 with ROS Jazzy (`#948 <https://github.com/mitsudome-r/autoware_core/issues/948>`_)
* fix(motion_velocity_planner_common): suppress maybe-uninitialized warning on NVIDIA DRIVE AGX Thor (`#877 <https://github.com/mitsudome-r/autoware_core/issues/877>`_)
* Contributors: Esteve Fernandez, NorahXiong, Ryuta Kambe, github-actions
