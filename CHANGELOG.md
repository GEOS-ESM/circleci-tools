# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [4.17.0] - 2025-12-15

### Changed

- Update gfortran executor to allow for using either OpenBLAS or MKL via `blas_lib` parameter (Default: `blas`)

## [4.16.0] - 2025-10-17

### Changed

- Update to Baselibs v8.20.0 by default
- Update ifx executor to use Intel 2025.2 and Intel MPI 2021.16

## [4.15.0] - 2025-09-24

### Changed

- Update to Baselibs v8.19.0 by default

## [4.14.0] - 2025-08.27

### Changed

- Update to Baselibs v8.18.0 by default

## [4.13.0] - 2025-05-06

### Changed

- Updated ifx executor to use Intel 2025.1 and Intel MPI 2021.15

## [4.12.0] - 2025-04-24

### Changed

- Changed default to use Baselibs v7.33.0

## [4.11.0] - 2025-04-07

### Changed

- Revert to using `large` resource class for the build job (was doubling costs unnecessarily)

## [4.10.0] - 2025-02-25

### Changed

- Changed default to use Baselibs v7.32.0

## [4.9.0] - 2025-02-07

### Changed

- Changed default to use Baselibs v7.31.0

## [4.8.0] - 2025-01-17

### Changed

- Added `build_type` to `run_mapl_tutorial` for matrix purposes

## [4.7.0] - 2025-01-15

### Changed

- Changed default to use Baselibs v7.29.0

## [4.6.0] - 2024-12-18

### Changed

- Move to Ubuntu 24 images/executors by default

## [4.5.0] - 2024-11-29

### Changed

- The build job now defaults to the `xlarge` resource class. It was found `ifx` jobs required more memory.

## [4.4.0] - 2024-11-19

### Changed

- Updated ifx executor to use Intel 2025.0 and Intel MPI 2021.14

## [4.3.0] - 2024-11-07

### Added

- Added new `remove_pfunit` option to the build job to remove PFUnit from the build (allowing testing of an edge case in MAPL)

## [4.2.0] - 2024-10-31

### Changed

- Update to use GCC 14.2 and Open MPI 5.0.5 for gfortran executors

## [4.1.0] - 2024-10-28

### Changed

- Changed default to use Baselibs v7.27.0

## [4.0.0] - 2024-08-23

Note: This is a major version bump due to the change from `intel` to `ifort` and `ifx` executors.
So older v2 based CI will need to change their `.circleci/config.yml` to use the new executors.

### Added

- Added new `ifx` executor as we transition from `ifort` to `ifx`

### Changed

- Changed the `ifort` executor to use newly named Docker images

### Removed

## [2.12.0] - 2024-07-23

### Changed

- Update default BCs to v11.6.0

## [2.11.0] - 2024-07-19

### Changed

- Changed default to use Baselibs v7.25.0
- Moved to use Intel 2024.2 (ifort 2021.13) and Intel MPI 2021.13

## [2.10.0] - 2024-06-10

### Changed

- Update default BCs to v11.5.0

## [2.9.0] - 2024-04-25

### Changed

- Revert back to Baselibs v7.23.0
  - GCC 13 oddities are appearing in testing

## [2.8.0] - 2024-04-25

### Changed

- Changed default to use Baselibs v7.24.0

## [2.7.0] - 2024-04-12

### Added

- Added `checkout_if_exists` option to `build.yml`. This gives the option to turn off `mepo checkout-if-exists` (needed for LDAS workflow). By default, it is `true`.

## [2.6.0] - 2024-04-04

### Changed

- Updated to GCC 13.2.0 and Open MPI 5.0.2 on the GNU executor

## [2.5.0] - 2024-04-03

### Changed

- Changed default to use Baselibs v7.23.0

## [2.4.0] - 2024-02-23

### Changed

- Due to [Linux image deprecations by CircleCI](https://discuss.circleci.com/t/linux-image-deprecations-and-eol-for-2024/50177), we
  have updated the docker executor to use the `default` image.

## [2.3.0] - 2024-02-07

### Added

- Added feature for conditional blobless mepo clones of the model.

## [2.2.0] - 2024-01-10

### Added

- Added new command `checkout_feature_branch_on_fixture_allow_fail` which will try and checkout the current PRs branch on the fixture. If it fails, it will just continue on.

## [2.1.0] - 2023-12-21

### Changed

- Updated the GNU image to use Open MPI 5.0.0

### Fixed

- Fixed some issues with the v12 orb-tools migration

## [2.0.1] - 2023-12-01

### Changed

- Updated all examples to use circleci-tools v2

## [2.0.0] - 2023-12-01

### Changed

- Migrated to orb-tools v12
  - This now requires snake_case for all commands and jobs
    - The major one will be `publish-docker` which is now `publish_docker`

## [1.26.0] - 2023-12-01

### Changed

- Update to use Baselibs v7.17.0 by default

## [1.25.0] - 2023-10-31

### Changed

- Update to use BCs v11.3.0 by default
  - New file for MOM6 runs

## [1.24.0] - 2023-08-28

### Changed

- Update to use BCs v11.2.0 by default

## [1.23.0] - 2023-08-25

### Changed

- Updated `checkout_mapl3_release_branch` command to also checkout `geos/release/MAPL-v3`

## [1.22.0] - 2023-07-31

### Changed

- Update to use Baselibs v7.14.0

## [1.21.0] - 2023-06-22

### Changed

- Update to use Baselibs v7.13.0 and BCs v11.1.0 by default

## [1.20.0] - 2023-05-30

### Added

- Add `remove_flap` and `remove_pflogger` options to `build` job for better UFS testing

## [1.19.0] - 2023-03-15

### Changed

- Moved to use BCs version v11.0.0 as the default

## [1.18.0] - 2022-12-16

### Changed

- Moved to use Baselibs v7.7.0 as the default

## [1.17.1] - 2022-10-20

### Fixed

- Pass `change_layout` through run_gcm

## [1.17.0] - 2022-10-20

### Added

- Added `change_layout` boolean to makeoneday command. Needed because the coupled run does not like the layout change.

## [1.16.1] - 2022-10-20

### Fixed

- Add `coupled_diagnostics` and `post` to the persisted workspace

## [1.16.0] - 2022-10-18

### Added

- Add `bcs_version` as a build arg for docker builds

## [1.15.1] - 2022-10-18

### Fixed

- Fix typo in run job

## [1.15.0] - 2022-10-17

## Added

- Added `gcm_ocean_type` to GCM experiment to support MOM6 runs

## [1.14.0] - 2022-10-13

### Changed

- Move to use `machine` executor for CircleCI Docker builds

## [1.13.1] - 2022-10-13

### Fixed

- Append compiler name to docker images as either Intel or GCC images might be built.

## [1.13.0] - 2022-10-13

### Added

- Added docker publish job
  - Has option to push to either Docker Hub or GitHub Container Registry (or both)

## [1.12.0] - 2022-09-14

### Added

- Add ability to use Ninja generator during CMake

### Changed

- Update executors to default to v10.23.0

## [1.11.0] - 2022-08-30

### Added

- Add ability to pass `fv_precision` into builds

### Changed

- Update `README.md` to reflect v11 orb-tools workflow

## [1.10.0] - 2022-08-25

### Changed

- Migrated to orb-tools v11

## [1.9.0] - 2022-08-16

### Changed

- Updated executors defaults to
  - GCC 12.1.0, Open MPI 4.1.4
  - Intel 2022.1.0, Intel MPI 2021.6.0
  - Baselibs v7.5.0
  - v10.22.5 boundary conditions

## [1.8.1] - 2022-07-13

### Fixed

- Fixed description of tutorial job

## [1.8.0] - 2022-07-13

### Added

- Add job and command to run MAPL tutorials

## [1.7.0] - 2022-05-18

### Fixes

- Add ability to pass in `bcs_version` to jobs and executors

## [1.6.1] - 2022-04-21

### Fixes

- Extend `baselibs_version` to jobs

## [1.6.0] - 2022-04-19

### Changed

- Added ability to pass in baselibs version to executors

## [1.5.2] - 2022-04-11

### Fixed

- Fixed all the dates in CHANGELOG

## [1.5.1] - 2022-04-11

### Fixed

- Fixed bug with handling of ESMA_cmake and ESMA_env in `checkout-if-exists`

## [1.5.0] - 2022-04-01

### Added

- Added `make_onehour_history` command

### Changed

- Changed GCM experiment
  - Runs for 1 hour
  - geosgcm_prog frequency is set to 1 hour (via sed)
  - ExtData is turned off as it seems to use too much memory

## [1.4.0] - 2022-04-01

### Changed

- Revert back to just bcs image for run

## [1.3.0] - 2022-04-01

### Changed

- Use the BCs image for all executors

## [1.2.0] - 2022-04-01

### Fixed

- Use the bcs executors for GCM run jobs

### Changed

- Persist fewer install directories

## [1.1.0] - 2022-03-23

### Added

- Added ability to checkout mapl3 branches in build job

## [1.0.0] - 2022-03-23

### Changed

- Tweaked some readmes

## [0.18.0] - 2022-03-23

### Added

- Commands
  - run_fv3_setup
  - run_fv3_experiment
  - create_gcm_expt
  - run_makeoneday
  - run_gcm_experiment
- Jobs
  - run_fv3
  - run gcm

## [0.17.0] - 2022-03-23

### Added

- Add persist_workspace step to build job

## [0.16.0] - 2022-03-23

### Changed

- Make mepodevelop true by default in build job

## [0.15.0] - 2022-03-22

### Changed

- Add ability to pass in subrepos to mepodevelop command

## [0.14.5] - 2022-03-22

### Fixed

- Fix *yet another* bug in fixture checkout handling

## [0.14.4] - 2022-03-22

### Fixed

- Add working_directory to build job

## [0.14.3] - 2022-03-22

### Fixed

- Fix bug in cmake handling in build job

## [0.14.2] - 2022-03-22

### Fixed

- Fix *another* bug in fixture handling in build job

## [0.14.1] - 2022-03-22

### Fixed

- Fix bug in fixture handling in build job

## [0.14.0] - 2022-03-22

### Added

- Added new `build` job
- Added `buildtests` and `runtests` commands
- Added example

## [0.13.0] - 2022-03-14

### Added

- Add new `buildtarget` command to build any target

## [0.12.0] - 2022-03-09

### Changed

- Updated executors to use Baselibs 6.2.13

## [0.11.0] - 2022-02-14

### Fixed

- Fix edge case in checkout_if_exists for the else.

## [0.10.0] - 2022-02-07

### Added

- Added new parameter to cmake command to allow extra options to be passed to CMake.

## [0.9.0] - 2022-02-07

### Added

- Added new parameter to cmake command to allow build type to be specified. Uses enum to force allowed value

### Changed

- Added `mepo status` at the end of subrepo-checkout step

## [0.8.0] - 2022-02-07

### Added

- Added new parameter to buildinstall to allow number of processes for rebuild step to be changed

## [0.7.0] - 2022-02-07

### Added

- Add command to `mepo checkout` branch on subrepo

## [0.6.0] - 2022-01-28

### Added

- Added executors with boundary conditions
- Added checkoutifexists command

## [0.5.0] - 2022-01-13

### Added

- Add command to checkout MAPL 3 branches

## [0.4.0] - 2022-01-11

### Changed

- Change how to handle retry-builds.
  - Before, it used `when: on_fail` and this worked in CircleCI land, but CircleCI labels any failure of a job a failure overall even with an `on_fail`. So here we use a bash `||` to trigger the rebuild
- Turned off shellcheck code due to [issues with CircleCI, GitHub, etc.](https://discuss.circleci.com/t/discussion-and-resolution-for-error-youre-using-an-rsa-key-with-sha-1-which-is-no-longer-allowed/42572/2?u=mathomp4)

## [0.3.0] - 2022-01-10

### Changed

- Fixed up readmes

## [0.2.0] - 2022-01-10

### Added

- Added the gfortran and ifort executors
  - They have a parameter, `resource_class` which defaults to `large`

## [0.1.0] - 2022-01-10

### Changed

- Made GEOSgcm the default repo of the commands

## [0.0.1] - 2022-01-10

### Added

- Added `.editorconfig` file
- Added commands from MAPL CI
- Add changelog enforcer
- Added GEOS contributing file

### Changed

- Updated `@orb.yml`
- Updated license to GEOS Apache
- Updated README

