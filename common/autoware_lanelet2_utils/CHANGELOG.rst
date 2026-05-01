^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package autoware_lanelet2_utils
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Forthcoming
-----------
* chore: align package versions to 1.7.0 and reset changelogs
* Merge remote-tracking branch 'origin/main' into tmp/bot/bump_version_base
* chore: sync files (`#845 <https://github.com/mitsudome-r/autoware_core/issues/845>`_)
  * chore: sync files
  * style(pre-commit): autofix
  ---------
  Co-authored-by: github-actions <github-actions@github.com>
  Co-authored-by: pre-commit-ci[bot] <66853113+pre-commit-ci[bot]@users.noreply.github.com>
* fix(autoware_lanelet2_utils): fix bugprone-unchecked-optional-access warnings (`#897 <https://github.com/mitsudome-r/autoware_core/issues/897>`_)
* fix: fix bugprone-exception-escape errors in autoware lanelet2 utils (`#882 <https://github.com/mitsudome-r/autoware_core/issues/882>`_)
  fix(autoware_lanelet2_utils): fix bugprone-exception-escape errors of clang-tidy check
* fix(autoware_lanelet2_utils): fix bugprone-narrowing-conversions warnings (`#931 <https://github.com/mitsudome-r/autoware_core/issues/931>`_)
  * fix(autoware_lanelet2_utils): fix bugprone-narrowing-conversions warnings
  * style(pre-commit): autofix
  ---------
  Co-authored-by: pre-commit-ci[bot] <66853113+pre-commit-ci[bot]@users.noreply.github.com>
* chore(common, map): remove unused lanelet2_extension header (`#903 <https://github.com/mitsudome-r/autoware_core/issues/903>`_)
  * remove unused lanelet2_extension in map component
  * remove unused lanelet2_extension in common component
  ---------
* docs(lanelet2_utils): simplify API table title for utils (`#851 <https://github.com/mitsudome-r/autoware_core/issues/851>`_)
  * change API table title to filename instead of raw path
  * fix typo
  ---------
* fix(lanelet2_utils): add invalid bound size handler in combine_lanelets_shape (`#878 <https://github.com/mitsudome-r/autoware_core/issues/878>`_)
  add invalid bound handler
* fix(lanelet2_utils): change is_in_lanelet argument order (`#890 <https://github.com/mitsudome-r/autoware_core/issues/890>`_)
* feat(lanelet2_extension): port lanelet2_extension utilities functions (final)  (`#838 <https://github.com/mitsudome-r/autoware_core/issues/838>`_)
  Co-authored-by: pre-commit-ci[bot] <66853113+pre-commit-ci[bot]@users.noreply.github.com>
  Co-authored-by: Mamoru Sobue <hilo.soblin@gmail.com>
* feat(path_generator): use `route_manager` to handle route data (`#803 <https://github.com/mitsudome-r/autoware_core/issues/803>`_)
  Co-authored-by: Mamoru Sobue <hilo.soblin@gmail.com>
  Co-authored-by: Mamoru Sobue <mamoru.sobue@tier4.jp>
* feat(lanelet2_utils): define create ConstLanelet from ConstLineString3d  (`#868 <https://github.com/mitsudome-r/autoware_core/issues/868>`_)
  * define create_safe_lanelet for ConstLineString3d
  * Update common/autoware_lanelet2_utils/src/conversion.cpp
  * remove unused definition
  * remove unused comment
  ---------
  Co-authored-by: Mamoru Sobue <hilo.soblin@gmail.com>
* feat(autoware_lanelet2_utils): add a custom find-nearest function (`#839 <https://github.com/mitsudome-r/autoware_core/issues/839>`_)
  * feat: add a custom find-nearest function
  * test: add unit testings
  * style: update docstrings
  * refactor: minor fixes
  * refactor: update boolean condition
  * refactor: replace zero to epsilon
  * docs: update API references for find_nearest
  ---------
* feat(autoware_lanelet2_extension): replace remaining lanelet2_extension utilities functions (`#842 <https://github.com/mitsudome-r/autoware_core/issues/842>`_)
  * replace getArcCoordinates usage
  * replace combineLaneletsShape
  * remove null return for get_dirty_expanded_lanelet
  * change get_dirty_expanded_lanelet(s) positive right_offset (and negative left_offset) handler
  ---------
  Co-authored-by: Mamoru Sobue <hilo.soblin@gmail.com>
* Contributors: Kotaro Uetake, Mitsuhiro Sakamoto, NorahXiong, Sarun MUKDAPITAK, awf-autoware-bot[bot], github-actions
