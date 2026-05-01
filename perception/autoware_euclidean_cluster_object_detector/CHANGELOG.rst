^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package autoware_euclidean_cluster_object_detector
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1.8.0 (2026-05-01)
------------------
* chore: align package versions to 1.7.0 and reset changelogs
* Merge remote-tracking branch 'origin/main' into tmp/bot/bump_version_base
* fix(autoware_euclidean_cluster_object_detector): fix bugprone-narrowing-conversions warnings (`#938 <https://github.com/mitsudome-r/autoware_core/issues/938>`_)
  * fix(autoware_euclidean_cluster_object_detector): fix bugprone-narrowing-conversions warnings
  * style(pre-commit): autofix
  ---------
  Co-authored-by: pre-commit-ci[bot] <66853113+pre-commit-ci[bot]@users.noreply.github.com>
  Co-authored-by: Junya Sasaki <j2sasaki1990@gmail.com>
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
* chore(euclidean_cluster): move header files from include to src (`#869 <https://github.com/mitsudome-r/autoware_core/issues/869>`_)
  * chore(autoware_euclidean_cluster_object_detector): move header files from include/ to src/
  * chore(euclidean_cluster): remove pragma once
  ---------
  Co-authored-by: Takahisa.Ishikawa <takahisa.ishikawa@tier4.jp>
* Contributors: NorahXiong, Takahisa Ishikawa, github-actions
