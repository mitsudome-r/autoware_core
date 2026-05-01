^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package autoware_crop_box_filter
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Forthcoming
-----------
* chore: align package versions to 1.7.0 and reset changelogs
* Merge remote-tracking branch 'origin/main' into tmp/bot/bump_version_base
* refactor(autoware_core): add USE_SCOPED_HEADER_INSTALL_DIR to sensing packages (`#985 <https://github.com/mitsudome-r/autoware_core/issues/985>`_)
  Co-authored-by: github-actions <github-actions@github.com>
* fix(autoware_crop_box_filter): add optional check before accessing crop_box_filter\_ (`#1016 <https://github.com/mitsudome-r/autoware_core/issues/1016>`_)
* refactor(crop_box_filter): simplify filter logic by using identity matrix for no-transform case (`#959 <https://github.com/mitsudome-r/autoware_core/issues/959>`_)
  refactor(autoware_crop_box_filter): simplify filter logic by using identity matrix for no-transform case
  Use identity matrices as default for preprocess/postprocess transforms,
  eliminating conditional branches in the filter loop. Pre-compute
  output_frame_id in the constructor to simplify frame_id resolution.
  Co-authored-by: Takahisa.Ishikawa <takahisa.ishikawa@tier4.jp>
* fix(autoware_crop_box_filter): fix bugprone-implicit-widening-of-multiplication-result warnings (`#911 <https://github.com/mitsudome-r/autoware_core/issues/911>`_)
* fix(autoware_crop_box_filter): fix bugprone-narrowing-conversions warnings (`#936 <https://github.com/mitsudome-r/autoware_core/issues/936>`_)
* refactor(autoware_crop_box_filter): extract CropBoxFilter logic class (`#941 <https://github.com/mitsudome-r/autoware_core/issues/941>`_)
  * refactor(autoware_crop_box_filter): rename CropBoxFilter node class to CropBoxFilterNode
  * refactor(autoware_crop_box_filter): extract CropBoxFilter logic class
  * refactor(autoware_crop_box_filter): remove output_frame from CropBoxFilterConfig
  * refactor(autoware_crop_box_filter): remove unnecessary member variables
  Convert tf_input_orig_frame\_ and max_queue_size\_ to local variables
  as they are only used in the constructor.
  * test(autoware_crop_box_filter): add unit tests for preprocess and postprocess transform
  * refactor(crop_box_filter): rename variable for clarity in transform handling
  * refactor(crop_box_filter): simplify transform handling by removing has_value checks
  ---------
  Co-authored-by: Takahisa.Ishikawa <takahisa.ishikawa@tier4.jp>
  Co-authored-by: Junya Sasaki <j2sasaki1990@gmail.com>
* fix(crop_box_filter): maybe-uninitialized build error (`#909 <https://github.com/mitsudome-r/autoware_core/issues/909>`_)
  fix(crop_box_filter): initialize CropBoxParam with default values in test
  Co-authored-by: Takahisa.Ishikawa <takahisa.ishikawa@tier4.jp>
* refactor(crop_box_filter): extract core and add unit tests (`#886 <https://github.com/mitsudome-r/autoware_core/issues/886>`_)
  * refactor(autoware_crop_box_filter): extract CropBoxParam and generate_crop_box_polygon to core library
  * test(autoware_crop_box_filter): add unit test for generate_crop_box_polygon
  * refactor(autoware_crop_box_filter): extract filter_pointcloud logic to core library
  * refactor(autoware_crop_box_filter): remove unnecessary includes from crop_box_filter_node.hpp
  * refactor(autoware_crop_box_filter): move filter_pointcloud tests to unit test file
  Move filter_pointcloud() tests from test_crop_box_filter_node.cpp to
  test_crop_box_filter.cpp since they test core logic, not node behavior.
  * refactor(autoware_crop_box_filter): apply AAA pattern and type aliases to filter_pointcloud tests
  * refactor(autoware_crop_box_filter): rename negative to keep_outside_box
  ---------
  Co-authored-by: Takahisa.Ishikawa <takahisa.ishikawa@tier4.jp>
* feat(crop_box_filter): simplify validation logic for input point cloud (`#875 <https://github.com/mitsudome-r/autoware_core/issues/875>`_)
  * feat(crop_box_filter): simplify point cloud validation logic and remove redundant functions
  * feat(crop_box_filter): remove dependency on rclcpp::Logger from validation logic
  * refactor(crop_box_filter): rename validation function
  * refactor(crop_box_filter): simplify point cloud validation tests and improve clarity
  * refactor(crop_box_filter): simplify point cloud validation logic by removing redundant lambda function
  * refactor(crop_box_filter): separate validation logic into its own files
  * refactor(crop_box_filter): remove rclcpp dependency and simplify timestamp handling in validation logic
  * chore(crop_box_filter): update copyright information to reflect current ownership
  * refactor(crop_box_filter): restructure validation logic by separating xyz field and data size checks
  * refactor(test): remove rclcpp dependency from test file
  * refactor(crop_box_filter): update validation functions to accept PointCloud2
  * refactor(crop_box_filter): improve error message comment
  * refactor(crop_box_filter): simplify PointCloud2 test cases by removing shared_ptr usage
  * feat(crop_box_filter): update data size validation logic to use greater than comparison
  * refactor(crop_box_filter): streamline validation logic for x, y, z fields in PointCloud2
  * refactor(crop_box_filter): remove unused memory header from crop_box_filter.cpp
  ---------
  Co-authored-by: Takahisa.Ishikawa <takahisa.ishikawa@tier4.jp>
* refactor(crop_box_filter): remove PCL dependencies and use PointCloud2 iterators (`#873 <https://github.com/mitsudome-r/autoware_core/issues/873>`_)
  * refactor(crop_box_filter): remove PCL dependencies and use PointCloud2 iterators for processing
  * refactor(crop_box_filter): rename out_x/y/z to output_x/y/z for clarity
  ---------
  Co-authored-by: Takahisa.Ishikawa <takahisa.ishikawa@tier4.jp>
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
