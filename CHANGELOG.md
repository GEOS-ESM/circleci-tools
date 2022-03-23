# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added

### Changed

### Removed

## [1.1.0] - 2021-03-23

### Added

- Added ability to checkout mapl3 branches in build job

## [1.0.0] - 2021-03-23

### Changed

- Tweaked some readmes

## [0.18.0] - 2021-03-23

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

## [0.17.0] - 2021-03-23

### Added

- Add persist_workspace step to build job

## [0.16.0] - 2021-03-23

### Changed

- Make mepodevelop true by default in build job

## [0.15.0] - 2021-03-22

### Changed

- Add ability to pass in subrepos to mepodevelop command

## [0.14.5] - 2021-03-22

### Fixed

- Fix *yet another* bug in fixture checkout handling

## [0.14.4] - 2021-03-22

### Fixed

- Add working_directory to build job

## [0.14.3] - 2021-03-22

### Fixed

- Fix bug in cmake handling in build job

## [0.14.2] - 2021-03-22

### Fixed

- Fix *another* bug in fixture handling in build job

## [0.14.1] - 2021-03-22

### Fixed

- Fix bug in fixture handling in build job

## [0.14.0] - 2021-03-22

### Added

- Added new `build` job
- Added `buildtests` and `runtests` commands
- Added example

## [0.13.0] - 2021-03-14

### Added

- Add new `buildtarget` command to build any target

## [0.12.0] - 2021-03-09

### Changed

- Updated executors to use Baselibs 6.2.13

## [0.11.0] - 2021-02-14

### Fixed

- Fix edge case in checkout_if_exists for the else.

## [0.10.0] - 2021-02-07

### Added

- Added new parameter to cmake command to allow extra options to be passed to CMake.

## [0.9.0] - 2021-02-07

### Added

- Added new parameter to cmake command to allow build type to be specified. Uses enum to force allowed value

### Changed

- Added `mepo status` at the end of subrepo-checkout step

## [0.8.0] - 2021-02-07

### Added

- Added new parameter to buildinstall to allow number of processes for rebuild step to be changed

## [0.7.0] - 2021-02-07

### Added

- Add command to `mepo checkout` branch on subrepo

## [0.6.0] - 2021-01-28

### Added

- Added executors with boundary conditions
- Added checkoutifexists command

## [0.5.0] - 2021-01-13

### Added

- Add command to checkout MAPL 3 branches

## [0.4.0] - 2021-01-11

### Changed

- Change how to handle retry-builds.
  - Before, it used `when: on_fail` and this worked in CircleCI land, but CircleCI labels any failure of a job a failure overall even with an `on_fail`. So here we use a bash `||` to trigger the rebuild
- Turned off shellcheck code due to [issues with CircleCI, GitHub, etc.](https://discuss.circleci.com/t/discussion-and-resolution-for-error-youre-using-an-rsa-key-with-sha-1-which-is-no-longer-allowed/42572/2?u=mathomp4)

## [0.3.0] - 2021-01-10

### Changed

- Fixed up readmes

## [0.2.0] - 2021-01-10

### Added

- Added the gfortran and ifort executors
  - They have a parameter, `resource_class` which defaults to `large`

## [0.1.0] - 2021-01-10

### Changed

- Made GEOSgcm the default repo of the commands

## [0.0.1] - 2021-01-10

### Added

- Added `.editorconfig` file
- Added commands from MAPL CI
- Add changelog enforcer
- Added GEOS contributing file

### Changed

- Updated `@orb.yml`
- Updated license to GEOS Apache
- Updated README

