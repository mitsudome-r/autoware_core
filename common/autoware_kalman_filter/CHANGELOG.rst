^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package autoware_kalman_filter
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Forthcoming
-----------
* chore: align package versions to 1.7.0 and reset changelogs
* Merge remote-tracking branch 'origin/main' into tmp/bot/bump_version_base
* perf(autoware_kalman_filter): optimize `updateWithDelay` by replacing sparse matrix operations (`#739 <https://github.com/mitsudome-r/autoware_core/issues/739>`_)
  * Optimize `updateWithDelay` by replacing sparse matrix operations with block arithmetic
  * style(pre-commit): autofix
  * Add test
  * style(pre-commit): autofix
  * Update README.md for (Extended Kalman Filter)
  * style(pre-commit): autofix
  * Add more detailed comments
  * style(pre-commit): autofix
  * Handle negative delay step and refactor tests
  * Replace TDKF with full term
  * style(pre-commit): autofix
  * Remove LLM like comment
  * Address PR review comments: add input validation, NaN guard, and docs fix
  - Add dimension validation for y, R, and C matrices in updateWithDelay
  - Add NaN/Inf check on Kalman gain to match base KalmanFilter::update
  - Add [[unlikely]] branch hints on all error paths
  - Clarify "diagonal block" comment terminology
  - Fix README augmented state vector (x\_{k-d} -> x\_{k-d+1}) and clarify delay range
  - Add test for C matrix dimension mismatch
  * style(pre-commit): autofix
  * fix: remove [[unlikely]] C++20 attributes for C++17 compatibility
  The [[unlikely]] attribute is a C++20 feature that causes compilation
  errors under clang-tidy which enforces strict C++17 compliance.
  ---------
  Co-authored-by: pre-commit-ci[bot] <66853113+pre-commit-ci[bot]@users.noreply.github.com>
  Co-authored-by: Yamato Ando <yamato.ando@tier4.jp>
* refactor(autoware_core): add USE_SCOPED_HEADER_INSTALL_DIR to common and testing packages (`#967 <https://github.com/mitsudome-r/autoware_core/issues/967>`_)
  Co-authored-by: github-actions <github-actions@github.com>
  Co-authored-by: Junya Sasaki <j2sasaki1990@gmail.com>
* fix(autoware_kalman_filter): fix bugprone-implicit-widening-of-multiplication-result warnings (`#910 <https://github.com/mitsudome-r/autoware_core/issues/910>`_)
* fix(autoware_kalman_filter): fix bugprone-narrowing-conversions warnings (`#930 <https://github.com/mitsudome-r/autoware_core/issues/930>`_)
* Contributors: Keita Morisaki, NorahXiong, Vishal Chauhan, github-actions
