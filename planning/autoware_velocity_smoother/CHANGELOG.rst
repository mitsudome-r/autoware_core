^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package autoware_velocity_smoother
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Forthcoming
-----------
* chore: align package versions to 1.7.0 and reset changelogs
* Merge remote-tracking branch 'origin/main' into tmp/bot/bump_version_base
* feat(trajectory): refactor velocity_smoother (analytical_jerk_constrained_smoother) to experimental trajectory (`#762 <https://github.com/mitsudome-r/autoware_core/issues/762>`_)
  * feat refactor analytical_jerk_constrained_smoother
  * fix curvature and added shield
  * fix: use clamp and added 0 acc for max velocity
  * lint fix
  * fix: update dv_before and use trajectory_base
  * fix review
  ---------
  Co-authored-by: Mamoru Sobue <hilo.soblin@gmail.com>
* feat(velocity_smoother): migrate velocity_planning_utils and trajectory_utils to use continous Trajectory<TrajectoryPoint> (`#749 <https://github.com/mitsudome-r/autoware_core/issues/749>`_)
  * initial commit, feat: modified trajectory_utils.cpp to continous_traj
  * fix:pre-commit
  * refactor: calcStopVelocityWithConstantJerkAccLimit, added test. refactor: calcVelocityProfileWithConstantJerkAndAccelerationLimit
  * feat: converted calcstopdistance, added searchzerovelocityposition
  * style(pre-commit): autofix
  * remove findzeroposition, make another PR
  * fix: change function name to search_zero_velocity_position
  * removed unused searchvelocityidx in the header
  * fix: missing header
  * fix: remove duplicate using
  * added conditional for velocity build and condition for debug loop
  * style(pre-commit): autofix
  * fixed build
  * fix curvature calculation
  * fix include
  * revert test deletion
  * fix cmake
  * fixed some comments
  * use curvature()
  * fixed calcVelocityProfileWithConstantJerkAndAccelerationLimit
  * remove unecessary boundary workaround for curvature()
  * revert calcVelocityProfileWithConstantJerkAndAccelerationLimit
  * removed unecessary build in calcVelocityProfileWithConstantJerkAndAccelerationLimit
  * fix: extractPathAroundPosition
  * feat: removed the use of build on fallback, merge profile for build
  ---------
  Co-authored-by: pre-commit-ci[bot] <66853113+pre-commit-ci[bot]@users.noreply.github.com>
  Co-authored-by: Mete Fatih Cırıt <mfc@autoware.org>
  Co-authored-by: Mamoru Sobue <hilo.soblin@gmail.com>
* fix(autoware_velocity_smoother): fix bugprone-narrowing-conversions warnings (`#919 <https://github.com/mitsudome-r/autoware_core/issues/919>`_)
  * fix(autoware_velocity_smoother): fix bugprone-narrowing-conversions warnings
  * style(pre-commit): autofix
  ---------
  Co-authored-by: pre-commit-ci[bot] <66853113+pre-commit-ci[bot]@users.noreply.github.com>
  Co-authored-by: Junya Sasaki <j2sasaki1990@gmail.com>
* chore: organize maintainer (`#859 <https://github.com/mitsudome-r/autoware_core/issues/859>`_)
* Contributors: Giovanni Muhammad Raditya, NorahXiong, Satoshi OTA, github-actions
