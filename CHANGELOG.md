# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added

### Changed

### Removed

## [0.4.0] - 2021-01-11

### Changed

- Change how to handle retry-builds.
  - Before, it used `when: on_fail` and this worked in CircleCI land, but CircleCI labels any failure of a job a failure overall
    even with an `on_fail`. So here we use a bash `||` to trigger the rebuild

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

