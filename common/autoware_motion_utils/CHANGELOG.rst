^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package autoware_motion_utils
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1.8.0 (2026-05-01)
------------------
* chore: align package versions to 1.7.0 and reset changelogs
* Merge remote-tracking branch 'origin/main' into tmp/bot/bump_version_base
* refactor(autoware_core): add USE_SCOPED_HEADER_INSTALL_DIR to common and testing packages (`#967 <https://github.com/mitsudome-r/autoware_core/issues/967>`_)
  Co-authored-by: github-actions <github-actions@github.com>
  Co-authored-by: Junya Sasaki <j2sasaki1990@gmail.com>
* fix(autoware_motion_utils): fix bugprone-unchecked-optional-access warnings (`#896 <https://github.com/mitsudome-r/autoware_core/issues/896>`_)
  fix(autoware_motion_utils): fix bugprone-unchecked-optional-access in resample.cpp
* fix(autoware_motion_utils): fix bugprone-optional-value-conversion warnings (`#906 <https://github.com/mitsudome-r/autoware_core/issues/906>`_)
* feat(motion_utils): add option to pose interpolation (`#997 <https://github.com/mitsudome-r/autoware_core/issues/997>`_)
* fix(autoware_motion_utils): fix bugprone-narrowing-conversions warnings (`#932 <https://github.com/mitsudome-r/autoware_core/issues/932>`_)
  * fix(autoware_motion_utils): fix bugprone-narrowing-conversions warnings
  * style(pre-commit): autofix
  ---------
  Co-authored-by: pre-commit-ci[bot] <66853113+pre-commit-ci[bot]@users.noreply.github.com>
* feat(motion_utils): skip nearby points to improve direction estimation (`#945 <https://github.com/mitsudome-r/autoware_core/issues/945>`_)
  * skip nearby points in isDrivingForward to improve direction estimation stability
  * change default value
  * fix comment
  ---------
* fix(motion_utils): properly use negative jerk in calculate_stop_distance (`#870 <https://github.com/mitsudome-r/autoware_core/issues/870>`_)
* feat(motion_utils): add calculate_stop_distance (`#849 <https://github.com/mitsudome-r/autoware_core/issues/849>`_)
  Co-authored-by: Mamoru Sobue <hilo.soblin@gmail.com>
* Contributors: Go Sakayori, Maxime CLEMENT, NorahXiong, Vishal Chauhan, Yuki TAKAGI, github-actions
