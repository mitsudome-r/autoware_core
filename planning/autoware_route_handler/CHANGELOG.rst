^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package autoware_route_handler
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Forthcoming
-----------
* chore: align package versions to 1.7.0 and reset changelogs
* Merge remote-tracking branch 'origin/main' into tmp/bot/bump_version_base
* feat(autoware_route_handler): add test for validating the `route_handler`'s reference path algorithm  (`#986 <https://github.com/mitsudome-r/autoware_core/issues/986>`_)
  Co-authored-by: Junya Sasaki <j2sasaki1990@gmail.com>
  Co-authored-by: Mamoru Sobue <hilo.soblin@gmail.com>
* feat(autoware_route_handler): smooth the centerline from `route_handler` function (`#1029 <https://github.com/mitsudome-r/autoware_core/issues/1029>`_)
  * fix border's discontinuity
  * add route_handler constructor using laneletMapPtr explicitly
  * change waypoint-centerline trim margin
  * improve interpolation at start_s to be on waypoint
  * change use_exact condition
  * add abnormal case comment
  ---------
* chore(planning, bvp): remove unused lanelet2_extension header (`#902 <https://github.com/mitsudome-r/autoware_core/issues/902>`_)
  * remove unused lanelet2_extension in bvp modules
  * remove unused lanelet2_extension in planning components
  ---------
* fix(autoware_route_handler): fix bugprone-narrowing-conversions warnings (`#923 <https://github.com/mitsudome-r/autoware_core/issues/923>`_)
  Co-authored-by: Junya Sasaki <j2sasaki1990@gmail.com>
* fix(lanelet2_utils): change is_in_lanelet argument order (`#890 <https://github.com/mitsudome-r/autoware_core/issues/890>`_)
* feat(lanelet2_extension): port lanelet2_extension utilities functions (final)  (`#838 <https://github.com/mitsudome-r/autoware_core/issues/838>`_)
  Co-authored-by: pre-commit-ci[bot] <66853113+pre-commit-ci[bot]@users.noreply.github.com>
  Co-authored-by: Mamoru Sobue <hilo.soblin@gmail.com>
* feat(autoware_lanelet2_extension): replace remaining lanelet2_extension utilities functions (`#842 <https://github.com/mitsudome-r/autoware_core/issues/842>`_)
  * replace getArcCoordinates usage
  * replace combineLaneletsShape
  * remove null return for get_dirty_expanded_lanelet
  * change get_dirty_expanded_lanelet(s) positive right_offset (and negative left_offset) handler
  ---------
  Co-authored-by: Mamoru Sobue <hilo.soblin@gmail.com>
* chore: organize maintainer (`#856 <https://github.com/mitsudome-r/autoware_core/issues/856>`_)
* Contributors: NorahXiong, Sarun MUKDAPITAK, Satoshi OTA, github-actions
