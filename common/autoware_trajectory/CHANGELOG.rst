^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package autoware_trajectory
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1.8.0 (2026-05-01)
------------------
* chore: align package versions to 1.7.0 and reset changelogs
* Merge remote-tracking branch 'origin/main' into tmp/bot/bump_version_base
* feat(autoware_trajectory): add max utilities (`#1051 <https://github.com/mitsudome-r/autoware_core/issues/1051>`_)
  * feat(autoware_trajectory): add max utilities
  * feat(autoware_trajectory): refactor max_at_bases to use compute_point and simplify logic
  ---------
* feat(autoware_trajectory): add param constraints (`#1047 <https://github.com/mitsudome-r/autoware_core/issues/1047>`_)
  * feat(autoware_trajectory): add azimuth, elevation, and curvature computation methods
  * feat(autoware_trajectory): add param constraints
  * feat(autoware_trajectory): add test for finding high curvature intervals
  ---------
* feat(autoware_trajectory): add azimuth, elevation, and curvature computation methods (`#1048 <https://github.com/mitsudome-r/autoware_core/issues/1048>`_)
* feat(autoware_trajectory): add align_orientation option to pretty_build and remove auto execution from constructor (`#1049 <https://github.com/mitsudome-r/autoware_core/issues/1049>`_)
  * feat(autoware_trajectory): add align_orientation option to pretty_build and remove auto execution from constructor
  * feat(autoware_trajectory): add align_orientation utility and integrate with pretty_build
  * Revert "feat(autoware_trajectory): add align_orientation option to pretty_build and remove auto execution from constructor"
  This reverts commit 37f2796992e17576c7a47297c8d182b793098ba1.
  * refactor(autoware_trajectory): remove unused align_orientation include from pretty_build
  ---------
* docs(autoware_trajectory): update README with TemporalTrajectory class and duplicate handling details (`#1045 <https://github.com/mitsudome-r/autoware_core/issues/1045>`_)
  * feat(autoware_trajectory): control test plotting via ENABLE_TEST_PLOT env var
  * refactor(autoware_trajectory): introduce granular epsilon constants and parameterize interpolators
  * feat(autoware_trajectory): add PCHIP interpolation implementation and example
  * refactor(autoware_trajectory): simplify crossed_with_polygon function by removing unused parameters and adjusting test cases
  * feat(autoware_trajectory): add single-point value assignment to InterpolatedArray
  * feat(autoware_trajectory): add TemporalTrajectory class
  * feat(autoware_trajectory): add temporal trajectory utilities
  * docs(autoware_trajectory): update README with TemporalTrajectory class and duplicate handling details
  ---------
* feat(autoware_trajectory): add temporal trajectory utilities (`#1044 <https://github.com/mitsudome-r/autoware_core/issues/1044>`_)
  * feat(autoware_trajectory): control test plotting via ENABLE_TEST_PLOT env var
  * refactor(autoware_trajectory): introduce granular epsilon constants and parameterize interpolators
  * feat(autoware_trajectory): add PCHIP interpolation implementation and example
  * refactor(autoware_trajectory): simplify crossed_with_polygon function by removing unused parameters and adjusting test cases
  * feat(autoware_trajectory): add single-point value assignment to InterpolatedArray
  * feat(autoware_trajectory): add TemporalTrajectory class
  * feat(autoware_trajectory): add temporal trajectory utilities
  ---------
* feat(autoware_trajectory): add TemporalTrajectory class (`#1043 <https://github.com/mitsudome-r/autoware_core/issues/1043>`_)
  * feat(autoware_trajectory): control test plotting via ENABLE_TEST_PLOT env var
  * refactor(autoware_trajectory): introduce granular epsilon constants and parameterize interpolators
  * feat(autoware_trajectory): add PCHIP interpolation implementation and example
  * refactor(autoware_trajectory): simplify crossed_with_polygon function by removing unused parameters and adjusting test cases
  * feat(autoware_trajectory): add single-point value assignment to InterpolatedArray
  * feat(autoware_trajectory): add TemporalTrajectory class
  ---------
* feat(autoware_trajectory): add single-point value assignment to InterpolatedArray (`#1042 <https://github.com/mitsudome-r/autoware_core/issues/1042>`_)
  * feat(autoware_trajectory): control test plotting via ENABLE_TEST_PLOT env var
  * refactor(autoware_trajectory): introduce granular epsilon constants and parameterize interpolators
  * feat(autoware_trajectory): add PCHIP interpolation implementation and example
  * refactor(autoware_trajectory): simplify crossed_with_polygon function by removing unused parameters and adjusting test cases
  * feat(autoware_trajectory): add single-point value assignment to InterpolatedArray
  ---------
* refactor(autoware_trajectory): simplify crossed_with_polygon function by removing unused parameters and adjusting test cases (`#1041 <https://github.com/mitsudome-r/autoware_core/issues/1041>`_)
  * feat(autoware_trajectory): control test plotting via ENABLE_TEST_PLOT env var
  * refactor(autoware_trajectory): introduce granular epsilon constants and parameterize interpolators
  * feat(autoware_trajectory): add PCHIP interpolation implementation and example
  * refactor(autoware_trajectory): simplify crossed_with_polygon function by removing unused parameters and adjusting test cases
  ---------
* feat(autoware_trajectory): add PCHIP interpolation implementation and example (`#1040 <https://github.com/mitsudome-r/autoware_core/issues/1040>`_)
  * feat(autoware_trajectory): control test plotting via ENABLE_TEST_PLOT env var
  * refactor(autoware_trajectory): introduce granular epsilon constants and parameterize interpolators
  * feat(autoware_trajectory): add PCHIP interpolation implementation and example
  * fix(autoware_trajectory): include missing iostream header for input/output operations
  ---------
* refactor(autoware_trajectory): introduce granular epsilon constants and parameterize interpolators (`#1039 <https://github.com/mitsudome-r/autoware_core/issues/1039>`_)
  * feat(autoware_trajectory): control test plotting via ENABLE_TEST_PLOT env var
  * refactor(autoware_trajectory): introduce granular epsilon constants and parameterize interpolators
  ---------
* feat(autoware_trajectory): control test plotting via ENABLE_TEST_PLOT env var (`#1038 <https://github.com/mitsudome-r/autoware_core/issues/1038>`_)
* test(autoware_trajectory): rename gtest cases to PascalCase (`#1024 <https://github.com/mitsudome-r/autoware_core/issues/1024>`_)
  Normalize test suite and test names across trajectory test files to use
  PascalCase naming.
  This keeps naming consistent with project conventions and improves test
  readability in gtest output without changing test behavior.
* refactor(autoware_trajectory): replace unreachable trajectory throws with asserts (`#1020 <https://github.com/mitsudome-r/autoware_core/issues/1020>`_)
  Swap defensive runtime exceptions for `assert` checks in trajectory
  interpolation, closest-point lookup, and pose orientation setup where
  failure is considered impossible under documented preconditions.
  Also update interpolator interface comments to describe required build
  state and clamped out-of-range behavior more explicitly.
* feat(autoware_trajectory): add offset trajectory utility (`#1013 <https://github.com/mitsudome-r/autoware_core/issues/1013>`_)
  * feat(autoware_trajectory): add offset trajectory utility
  * test(autoware_trajectory): add test for single point combined offset calculation
  * feat(autoware_trajectory): support 3d offset using full pose orientation
  Apply trajectory offsets with full quaternion rotation instead of yaw
  only so roll, pitch, and vertical offsets are respected. Update the
  utility documentation and extend tests to cover pitched and fully
  oriented trajectory points.
  * test(autoware_trajectory): consolidate offset trajectory test fixtures
  Simplify the offset test helpers by using a single trajectory point
  factory that covers position and full orientation inputs.
  This keeps the test setup consistent across yaw-only and 3D pose cases
  while preserving coverage for combined offset behavior.
  * docs(autoware_trajectory): simplify offset example trajectory setup
  Trim the example to focus on generating and visualizing offset
  trajectories from position-only points.
  Use trajectory direction alignment to derive orientations instead of
  manually assigning yaw and remove unused velocity diagnostics to keep
  the sample easier to follow.
  * docs(autoware_trajectory): add add_offset image to README
  * fix(autoware_trajectory): assert offset rebuild succeeds
  Replace the unused build result suppression with a runtime assertion on
  `build()` success when reconstructing the offset trajectory.
  This makes the invariant explicit and catches unexpected failures in a
  code path that should always preserve valid point ordering and count.
  * docs(autoware_trajectory): embed add_offset example in README
  Replace the inline `add_offset` usage snippet with a sourced excerpt from
  `example_add_offset.cpp` so the documentation stays aligned with the
  maintained example code.
  * chore(autoware_trajectory): harden add_offset example execution
  Wrap the `example_add_offset` demo in exception handling so failures from
  the embedded Python plotting setup are surfaced more cleanly.
  Update the README snippet reference to match the revised example source
  location.
  ---------
* refactor(autoware_trajectory): add effective_lanelet_id helper to ReferencePoint (`#1010 <https://github.com/mitsudome-r/autoware_core/issues/1010>`_)
* refactor(autoware_trajectory): fix clang-tidy warnings in footprint utils (`#1006 <https://github.com/mitsudome-r/autoware_core/issues/1006>`_)
  * refactor(autoware_trajectory): rename binary search functions for clarity
  * refactor(autoware_trajectory): fix clang-tidy warnings in footprint utils
  ---------
  Co-authored-by: Ryohsuke Mitsudome <43976834+mitsudome-r@users.noreply.github.com>
* fix(autoware_trajectory): add Takumi Odashima as a maintainer (`#1007 <https://github.com/mitsudome-r/autoware_core/issues/1007>`_)
* refactor(autoware_trajectory): rename binary search functions for clarity (`#1005 <https://github.com/mitsudome-r/autoware_core/issues/1005>`_)
  * refactor(autoware_trajectory): rename binary search functions for clarity
  * docs(autoware_trajectory): add max_iter parameter documentation
  * fix(autoware_trajectory): simplify termination condition in binary search functions
  ---------
* feat(autoware_trajectory): handle sparse points with interpolator fallback (`#994 <https://github.com/mitsudome-r/autoware_core/issues/994>`_)
  * feat(trajectory): handle sparse points with interpolator fallback
  * feat(autoware_trajectory): skip orientation alignment when insufficient points are available
  * feat(autoware_trajectory): add minimum distance threshold check for trajectory building
  * refactor(autoware_trajectory): reorganize and rename test cases for clarity and consistency
  * fix(autoware_trajectory): cover restore for degenerate trajectories
  * refactor(autoware_trajectory): simplify restore output
  * fix(autoware_path_generator): align degenerate trajectory handling
  * feat(autoware_trajectory): enhance fallback interpolator functionality and improve documentation
  * refactor(trajectory): replace array indexing with at() for safer access
  * feat(autoware_trajectory): add error handling for empty bases in start, end, and range methods
  * fix(autoware_trajectory): guard degenerate interpolation math
  * refactor(autoware_trajectory): simplify point restoration logic and improve test clarity
  * refactor(autoware_trajectory): remove unused includes and improve code clarity
  * chore: add missing includes for string and utility in example and test files
  * fix(autoware_trajectory): initialize point coordinates in buildCroppedTrajectory test
  * revert shift changes
  * fix
  ---------
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
* refactor(autoware_trajectory): clean up test target dependencies (`#990 <https://github.com/mitsudome-r/autoware_core/issues/990>`_)
  * fix(autoware_trajectory): clean up test target dependencies
  * refactor(autoware_trajectory): remove URL
  * fix(autoware_trajectory): add temporary fix to build with jazzy
  ---------
* fix(autoware_trajectory): fix bugprone-narrowing-conversions warnings (`#920 <https://github.com/mitsudome-r/autoware_core/issues/920>`_)
* fix(autoware_trajectory): wrap examples into BUILD_TESTING in `CMakeLists.txt` (`#885 <https://github.com/mitsudome-r/autoware_core/issues/885>`_)
  * wrap examples into build_testing
  * add 'BUILD_TESTING' for clarity
  * Revert "add 'BUILD_TESTING' for clarity"
  This reverts commit 73c1deb70089f43fc731ad92c69f873524a738a7.
  ---------
  Co-authored-by: Junya Sasaki <j2sasaki1990@gmail.com>
* feat(autoware_trajectory): define set stopline in Trajectory class (`#806 <https://github.com/mitsudome-r/autoware_core/issues/806>`_)
* feat(trajectory): add util function that returns first index satisfying constraint (`#881 <https://github.com/mitsudome-r/autoware_core/issues/881>`_)
* build(autoware_trajectory): add missing include (`#853 <https://github.com/mitsudome-r/autoware_core/issues/853>`_)
  fix(autoware_trajectory): add missing include
  std::clamp() added in `#791 <https://github.com/mitsudome-r/autoware_core/issues/791>`_ needs to include <algorithm>. Without it,
  GCC 14 complains with "error: 'clamp' is not a member of 'std'".
  Co-authored-by: Junya Sasaki <j2sasaki1990@gmail.com>
* feat(autoware_lanelet2_extension): replace remaining lanelet2_extension utilities functions (`#842 <https://github.com/mitsudome-r/autoware_core/issues/842>`_)
  * replace getArcCoordinates usage
  * replace combineLaneletsShape
  * remove null return for get_dirty_expanded_lanelet
  * change get_dirty_expanded_lanelet(s) positive right_offset (and negative left_offset) handler
  ---------
  Co-authored-by: Mamoru Sobue <hilo.soblin@gmail.com>
* Contributors: Giovanni Muhammad Raditya, Mete Fatih Cırıt, Michal Sojka, Mitsuhiro Sakamoto, NorahXiong, Sarun MUKDAPITAK, Taeseung Sohn, Yukinari Hisaki, github-actions
