^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package autoware_gnss_poser
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1.8.0 (2026-05-01)
------------------
* chore: align package versions to 1.7.0 and reset changelogs
* Merge remote-tracking branch 'origin/main' into tmp/bot/bump_version_base
* refactor(autoware_core): add USE_SCOPED_HEADER_INSTALL_DIR to sensing packages (`#985 <https://github.com/mitsudome-r/autoware_core/issues/985>`_)
  Co-authored-by: github-actions <github-actions@github.com>
* fix(autoware_gnss_poser): fix flaky test timeout on CI (`#1018 <https://github.com/mitsudome-r/autoware_core/issues/1018>`_)
  Replace background spin() threads with main-thread spin_some() to make
  the test deterministic. The previous approach used two executors with
  two background threads per test, creating race conditions in cancel/join
  during TearDown that caused intermittent 60s timeouts on CI.
  - Use single executor with spin_some() instead of background spin()
  - Extract rebuildGnssPoserNode() to properly reset subscriptions before
  destroying the old node, preventing dangling references
  - Replace std::atomic<bool> with plain bool (single-threaded now)
  - Replace sleep_for waits with executor->spin_some() to process work
* fix(autoware_gnss_poser): fix test timeout on Humble (`#1015 <https://github.com/mitsudome-r/autoware_core/issues/1015>`_)
  fix(autoware_gnss_poser): fix test timeout on Humble by using single rclcpp init/shutdown
  The test_autoware_gnss_poser binary was timing out on the humble-above CI
  job because each test fixture performed its own rclcpp::init()/shutdown()
  cycle (9 total). On Humble, repeated init/shutdown cycles cause resource
  leaks that eventually hang the executor.
  Move rclcpp::init() and rclcpp::shutdown() to main() so there is a single
  lifecycle for the entire test binary. Also reset publisher_executor\_ in
  TearDown to avoid dangling references.
* fix(autoware_gnss_poser): fix bugprone-implicit-widening-of-multiplication-result warnings (`#912 <https://github.com/mitsudome-r/autoware_core/issues/912>`_)
  fix(autoware_gnss_poser): fix bugprone-implicit-widening-of-multiplication-result warnings
* chore(sensing): move header files from include/ to src/ (`#852 <https://github.com/mitsudome-r/autoware_core/issues/852>`_)
  * refactor(sensing): move header files from include/ to src/ for crop_box_filter and gnss_poser
  These headers are internal implementation details not used by external
  packages. Moving them to src/ clarifies they are private headers.
  * style(pre-commit): autofix
  * fix(crop_box_filter): fix for linter
  * style(pre-commit): autofix
  ---------
  Co-authored-by: pre-commit-ci[bot] <66853113+pre-commit-ci[bot]@users.noreply.github.com>
  Co-authored-by: Takahisa.Ishikawa <takahisa.ishikawa@tier4.jp>
* Contributors: Mete Fatih Cırıt, NorahXiong, Takahisa Ishikawa, Vishal Chauhan, github-actions
