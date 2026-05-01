^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package autoware_ground_filter
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1.8.0 (2026-05-01)
------------------
* chore: align package versions to 1.7.0 and reset changelogs
* Merge remote-tracking branch 'origin/main' into tmp/bot/bump_version_base
* fix(ground_filter): remove unused `grid_id` (`#1025 <https://github.com/mitsudome-r/autoware_core/issues/1025>`_)
  * fix(ground_filter): remove unused `grid_id`
  * style(pre-commit): autofix
  ---------
  Co-authored-by: pre-commit-ci[bot] <66853113+pre-commit-ci[bot]@users.noreply.github.com>
* fix(autoware_ground_filter): solve variableScope warning (`#956 <https://github.com/mitsudome-r/autoware_core/issues/956>`_)
  Co-authored-by: Junya Sasaki <j2sasaki1990@gmail.com>
* test(autoware_ground_filter): add unit tests (`#497 <https://github.com/mitsudome-r/autoware_core/issues/497>`_)
  * test(autoware_ground_filter): add unit tests
  * style(pre-commit): autofix
  * fix(autoware_ground_filter): adapt tests to current codebase
  - Fix include paths after headers moved from include/ to src/
  - Add target_include_directories(PRIVATE src) for test targets
  - Fix integer division bugs (i/10 -> i/10.0f etc.) to produce
  correct floating point grid coordinates
  ---------
  Co-authored-by: pre-commit-ci[bot] <66853113+pre-commit-ci[bot]@users.noreply.github.com>
  Co-authored-by: Mete Fatih Cırıt <mfc@autoware.org>
* fix(ground_filter): remove unused struct member (`#812 <https://github.com/mitsudome-r/autoware_core/issues/812>`_)
* fix(autoware_ground_filter): fix bugprone-narrowing-conversions warnings (`#933 <https://github.com/mitsudome-r/autoware_core/issues/933>`_)
  * fix(autoware_ground_filter): fix bugprone-narrowing-conversions warnings
  * style(pre-commit): autofix
  ---------
  Co-authored-by: pre-commit-ci[bot] <66853113+pre-commit-ci[bot]@users.noreply.github.com>
* chore(ground_fitler): move header files from include/ to src/ (`#863 <https://github.com/mitsudome-r/autoware_core/issues/863>`_)
  * chore(ground_fitler): move header files from include/ to src/
  * chore(ground_filter): remove unused variable suppressions in grid.hpp
  ---------
  Co-authored-by: Takahisa.Ishikawa <takahisa.ishikawa@tier4.jp>
* Contributors: NorahXiong, Ryuta Kambe, Takahisa Ishikawa, github-actions
