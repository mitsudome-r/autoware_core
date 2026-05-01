^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package autoware_path_generator
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1.8.0 (2026-05-01)
------------------
* chore: align package versions to 1.7.0 and reset changelogs
* Merge remote-tracking branch 'origin/main' into tmp/bot/bump_version_base
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
* chore(path_generator): remove deprecated function (`#847 <https://github.com/mitsudome-r/autoware_core/issues/847>`_)
  * use route_manager
  * fix tests
  * update planner data in initialize_route_manager()
  * remove unused utility functions
  * restore old interface for static_centerline_generator
  * remove planner_data
  * remove unused header and old function
  * restore old class and function
  * add null check
  * remove deprecated class and function
  This reverts commit d4f976184ddad5cfc5e67254b96a922d2561d360.
  * fix format
  * fix deprecated
  * fix
  ---------
  Co-authored-by: Mamoru Sobue <mamoru.sobue@tier4.jp>
  Co-authored-by: Mamoru Sobue <hilo.soblin@gmail.com>
* fix(path_generator): prevent path truncation before current lanelet (`#979 <https://github.com/mitsudome-r/autoware_core/issues/979>`_)
  Fix path generator truncation before current lane
* fix(autoware_path_generator): fix bugprone-narrowing-conversions warnings (`#921 <https://github.com/mitsudome-r/autoware_core/issues/921>`_)
  * fix(autoware_path_generator): fix bugprone-narrowing-conversions warnings
  * style(pre-commit): autofix
  ---------
  Co-authored-by: pre-commit-ci[bot] <66853113+pre-commit-ci[bot]@users.noreply.github.com>
* chore(planning, bvp): remove unused lanelet2_extension header (`#902 <https://github.com/mitsudome-r/autoware_core/issues/902>`_)
  * remove unused lanelet2_extension in bvp modules
  * remove unused lanelet2_extension in planning components
  ---------
* fix(autoware_path_generator): remove unused variable path_points_with_lane_id (`#954 <https://github.com/mitsudome-r/autoware_core/issues/954>`_)
  The variable was declared but never read or written to beyond initialization.
  Detected by cppcheck [unreadVariable].
  Co-authored-by: ryuta.kambe <ryuta.kambe@npc2302009.local>
  Co-authored-by: Claude Sonnet 4.6 <noreply@anthropic.com>
* fix(lanelet2_utils): change is_in_lanelet argument order (`#890 <https://github.com/mitsudome-r/autoware_core/issues/890>`_)
* fix(autoware_path_generator): remove getArcCoordinates (`#891 <https://github.com/mitsudome-r/autoware_core/issues/891>`_)
  replace remaining getArcCoordinates
* feat(lanelet2_extension): port lanelet2_extension utilities functions (final)  (`#838 <https://github.com/mitsudome-r/autoware_core/issues/838>`_)
  Co-authored-by: pre-commit-ci[bot] <66853113+pre-commit-ci[bot]@users.noreply.github.com>
  Co-authored-by: Mamoru Sobue <hilo.soblin@gmail.com>
* feat(path_generator): use `route_manager` to handle route data (`#803 <https://github.com/mitsudome-r/autoware_core/issues/803>`_)
  Co-authored-by: Mamoru Sobue <hilo.soblin@gmail.com>
  Co-authored-by: Mamoru Sobue <mamoru.sobue@tier4.jp>
* feat(autoware_lanelet2_extension): replace remaining lanelet2_extension utilities functions (`#842 <https://github.com/mitsudome-r/autoware_core/issues/842>`_)
  * replace getArcCoordinates usage
  * replace combineLaneletsShape
  * remove null return for get_dirty_expanded_lanelet
  * change get_dirty_expanded_lanelet(s) positive right_offset (and negative left_offset) handler
  ---------
  Co-authored-by: Mamoru Sobue <hilo.soblin@gmail.com>
* Contributors: Mitsuhiro Sakamoto, NorahXiong, Ryuta Kambe, Sarun MUKDAPITAK, Yukinari Hisaki, github-actions, teranishi
