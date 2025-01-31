# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.13.0] - 2021-09-22

### Changed

* Change in behavior for `pygitops.operations.stage_commit_push_changes`:
  * Previously, the `items_to_stage` optional argument will drive autodiscovery of items to stage if not provided.
  * Previously, when no items to stage are discovered, a `PyGitOpsError` is raised.
  * The new change in behavior allows `items_to_stage` to be explicitly set to `[]`, indicating that the caller does not want autodiscovery of items to stage to occur, and the list is indeed empty.
  * This change caters to more advanced use cases such as [performing automated updates to git submodules where staged changes are intentionally absent](https://wayfair-incubator.github.io/pygitops/making-changes-on-feature-branch/#advanced-example)

## [0.12.1] - 2021-09-21

### Changed

* Restrict the allowable version range of GitPython to >=3.1,<=3.1.18
  * Newer versions of GitPython have had significant issues with typehinting that are proving to be incompatible with mypy

## [0.12.0] - 2021-08-30

### Changed

* Cleaned up the working directory on feature branch when we exit feature branch context manager.

## [0.11.1] - 2021-05-17

### Fixed

* Properly increment version number to `0.11.1` (version `0.11.0` was not tagged properly so it was not pushed to PyPI)

## [0.11.0] - 2021-05-14

### Changed

* Removed `repo_name` parameter of the `get_updated_repo` function to give the user control of exactly where to clone the repo contents to. The `clone_dir` argument is now the directory into which the contents of the repo will be cloned.

## [0.10.0] - 2021-05-07

### Added

- First public release!!!
