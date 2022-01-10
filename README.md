# CircleCI Tools for GEOS-ESM

[![CircleCI Build Status](https://circleci.com/gh/GEOS-ESM/circleci-tools.svg?style=shield "CircleCI Build Status")](https://circleci.com/gh/GEOS-ESM/circleci-tools) [![CircleCI Orb Version](https://badges.circleci.com/orbs/geos-esm/circleci-tools.svg)](https://circleci.com/orbs/registry/orb/geos-esm/circleci-tools) [![GitHub License](https://img.shields.io/badge/license-MIT-lightgrey.svg)](https://raw.githubusercontent.com/GEOS-ESM/circleci-tools/master/LICENSE) [![CircleCI Community](https://img.shields.io/badge/community-CircleCI%20Discuss-343434.svg)](https://discuss.circleci.com/c/ecosystem/orbs)


This repo holds commands, scripts, etc. for CircleCI tasks in GEOS-ESM

## Usage

_For full usage guidelines, see the [orb registry listing](https://circleci.com/orbs/registry/orb/geos-esm/circleci-tools)._

## Contributing

We welcome [issues](https://github.com/GEOS-ESM/circleci-tools/issues) to and [pull requests](https://github.com/GEOS-ESM/circleci-tools/pulls) against this repository!

## How to Publish

* Create and push a branch with your new features.
* When ready to publish a new production version, create a Pull Request from _feature branch_ to `master`.
* The title of the pull request must contain a special semver tag: `[semver:<segment>]` where `<segment>` is replaced by one of the following values.

| Increment | Description|
| ----------| -----------|
| major     | Issue a 1.0.0 incremented release|
| minor     | Issue a x.1.0 incremented release|
| patch     | Issue a x.x.1 incremented release|
| skip      | Do not issue a release|

Example: `[semver:major]`

* Squash and merge. Ensure the semver tag is preserved and entered as a part of the commit message.
* On merge, after manual approval, the orb will automatically be published to the Orb Registry.

For further questions/comments about this or other orbs, visit the Orb Category of [CircleCI Discuss](https://discuss.circleci.com/c/orbs).

