^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package autoware_ndt_scan_matcher
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Forthcoming
-----------
* chore: align package versions to 1.7.0 and reset changelogs
* Merge remote-tracking branch 'origin/main' into tmp/bot/bump_version_base
* fix(ndt_scan_matcher): fix concurrency bugs caused by missing locks by introducing Guarded class (`#1030 <https://github.com/mitsudome-r/autoware_core/issues/1030>`_)
  * Removed `setInputSource`
  * Applied `pre-commit run -a`
  * Corrected according to cppcheck's indications
  * bug: fix wrongly remaining `getInputSource` (see below)
  * This bug is caused due to my previous conflict resolve
  * fix(agnocastlib): fix missing lock on latest_ekf_position\_ and add Guarded class
  The `latest_ekf_position\_` field in `NDTScanMatcher` was intended to be
  protected by `latest_ekf_position_mutex\_`, but a concurrency bug existed
  due to missing lock acquisitions.
  To resolve this issue, this commit introduces a new `Guarded` class. This
  class encapsulates both the mutex and the data it protects into a single
  entity. By enforcing lock acquisition whenever the internal data is accessed,
  it systematically prevents bugs caused by forgetting to acquire locks.
  * refactor(ndt_scan_matcher): apply Guarded class to last_update_position\_
  * fix(ndt_scan_matcher): fix missing lock bugs by wrapping ndt_ptr\_ with Guarded
  Refactored `ndt_ptr\_` and `ndt_ptr_mtx\_` in `NDTScanMatcher` using `Guarded`
  to fix missing lock bugs. This change was also applied to `MapUpdateModule`.
  Due to this change, some member functions were updated to take `NDT` as
  an argument. Whenever possible, these functions now take a reference to
  `NDT` instead of a `shared_ptr`. This is a best practice to prevent the
  pointer from leaking outside of `Guarded::with()`.
  Note: `MapUpdateModule::secondary_ndt_ptr\_` also has a missing lock bug.
  This will be fixed in a future commit and is not covered here.
  * refactor(ndt_scan_matcher): pass NDT by reference instead of std::shared_ptr
  When a function takes `std::shared_ptr<T>` as an argument, there should
  be a specific reason to use a pointer (such as sharing ownership).
  However, functions like `estimate_xy_covariance_by_laplace_approximation()`
  do not actually need these characteristics internally. By changing the
  arguments to take a reference instead, we reduce the risk of leaking
  pointers outside unnecessarily.
  Although this commit is not a bug fix, it is important as an example of
  a best practice when using `Guarded`: preventing internal data from
  leaking outside as much as possible.
  * refactor(ndt_scan_matcher): pre-commit
  * fix(ndt_scan_matcher): fix concurrency bug in secondary_ndt_ptr\_ using Guarded
  The `secondary_ndt_ptr\_` field in `MapUpdateModule` previously lacked
  lock protection. Since it can be accessed by multiple threads at the same
  time (from `NDTScanMatcher::service_ndt_align()` and
  `NDTScanMatcher::callback_timer()`), it needs to be protected.
  To fix this, we wrapped it with `Guarded` to add a lock.
  Generally, this data is accessed from within a *MutuallyExclusive* timer
  callback. Because it is not accessed frequently by multiple threads, we
  decided to use a larger lock scope for the basic processing.
  * refactor(ndt_scan_matcher): move heavy map update operations outside the lock
  To prevent the NDT scan matcher from being blocked during dynamic map loading,
  this commit moves the cloning and destruction of the NDT map out of the
  `ndt_ptr\_` lock scope. By using only a fast `std::swap` inside the lock,
  the align process is no longer delayed.
  * fix(ndt_scan_matcher): fix cppcheck errors
  ---------
  Co-authored-by: Shintaro Sakoda <shintaro.sakoda@tier4.jp>
  Co-authored-by: Junya Sasaki <j2sasaki1990@gmail.com>
  Co-authored-by: Junya Sasaki <junya.sasaki@tier4.jp>
* fix(ndt_scan_matcher): remove `setInputSource` (`#837 <https://github.com/mitsudome-r/autoware_core/issues/837>`_)
  * Removed `setInputSource`
  * Applied `pre-commit run -a`
  * Corrected according to cppcheck's indications
  * bug: fix wrongly remaining `getInputSource` (see below)
  * This bug is caused due to my previous conflict resolve
  ---------
  Co-authored-by: Junya Sasaki <j2sasaki1990@gmail.com>
  Co-authored-by: Junya Sasaki <junya.sasaki@tier4.jp>
* refactor(autoware_core): add USE_SCOPED_HEADER_INSTALL_DIR to localization packages (`#984 <https://github.com/mitsudome-r/autoware_core/issues/984>`_)
  Co-authored-by: github-actions <github-actions@github.com>
  Co-authored-by: Junya Sasaki <j2sasaki1990@gmail.com>
* fix(`ndt_scan_matcher`): guard input source access with mutex (`#991 <https://github.com/mitsudome-r/autoware_core/issues/991>`_)
  * bug(`ndt_scan_matcher`): fix to guard input source access with mutex
  * bug(`ndt_scan_matcher`): do not lock unnecessarily longer
  * This fix is according to the following review comment:
  ```
  Because the input\_ is copied within BaseRegType::operator=(other), we should only lock the guard when necessary.
  ```
  * bug: deep-copy to avoid data races (see below)
  * When the producer (callback timer) mutates the cloud after passing it in,
  there is a risk that the `input\_` pointcloud is updated unexpectedly after
  getting `input\_` by `getInputSource()`
  ---------
  Co-authored-by: Anh Nguyen <vietanhng17@gmail.com>
* feat(autoware_ndt_scan_matcher): apply autoware_agnocast_wrapper for CIE (`#966 <https://github.com/mitsudome-r/autoware_core/issues/966>`_)
  Co-authored-by: Koichi Imai <45482193+Koichi98@users.noreply.github.com>
  Co-authored-by: Ryohsuke Mitsudome <43976834+mitsudome-r@users.noreply.github.com>
* fix(autoware_ndt_scan_matcher): fix bugprone-narrowing-conversions warnings (`#929 <https://github.com/mitsudome-r/autoware_core/issues/929>`_)
* revert: "chore(`autoware_ndt_scan_matcher`)): move header files from `include` to `src`" (`#880 <https://github.com/mitsudome-r/autoware_core/issues/880>`_)
  This reverts commit ee1c5d1d4d70e43e8345d06402e1fcb3a4007db3.
* chore(`autoware_ndt_scan_matcher`): move header files from `include` to `src` (`#866 <https://github.com/mitsudome-r/autoware_core/issues/866>`_)
  * chore(ndt_scan_matcher): move headers from `include` to `src` not to be public
  * bug(`ndt_omp`): fix a missing copyright
  * bug(ndt_scan_matcher): remove unnecessary lines in `CMakeLists.txt`
  * style(pre-commit): autofix
  * bug: fix by `pre-commit`
  * bug: fix by `cppcheck`
  * style(pre-commit): autofix
  * bug: fix by `pre-commit`
  ---------
  Co-authored-by: pre-commit-ci[bot] <66853113+pre-commit-ci[bot]@users.noreply.github.com>
* Contributors: Junya Sasaki, NorahXiong, Ryohsuke Mitsudome, SakodaShintaro, Takumi Jin, Vishal Chauhan, atsushi yano, github-actions
