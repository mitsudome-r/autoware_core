^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package autoware_motion_velocity_planner
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1.8.0 (2026-05-01)
------------------
* chore: align package versions to 1.7.0 and reset changelogs
* Merge remote-tracking branch 'origin/main' into tmp/bot/bump_version_base
* test(autoware_motion_velocity_planner): add unit tests (`#518 <https://github.com/mitsudome-r/autoware_core/issues/518>`_)
  * test(autoware_motion_velocity_planner): add unit tests
  * style(pre-commit): autofix
  * fix(autoware_motion_velocity_planner): adapt tests to current codebase
  - Fix service includes: srv moved from autoware_motion_velocity_planner
  to autoware_internal_planning_msgs
  - Sync test configs with production configs (motion_velocity_planner,
  obstacle_stop, velocity_smoother params diverged significantly)
  - Add yaml-cpp link dependency for test target
  - Resolve CMakeLists.txt conflict (ament_auto_package rename)
  * style(pre-commit): autofix
  * perf(autoware_motion_velocity_obstacle_stop_module): optimize unit test logic
  Co-authored-by: Mete Fatih Cırıt <mfc@autoware.org>
  ---------
  Co-authored-by: pre-commit-ci[bot] <66853113+pre-commit-ci[bot]@users.noreply.github.com>
  Co-authored-by: Mete Fatih Cırıt <mfc@autoware.org>
* Contributors: NorahXiong, github-actions
