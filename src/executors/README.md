# Executors

This directory contains the [Parameterized Executors](https://circleci.com/docs/2.0/reusing-config/#executors) used in GEOS-ESM
CircleCI jobs. We currently define two executors:

1. gfortran
2. ifort

These are named to match the Fortran compiler.

They have on optional parameter `resource_class` which is default to `large`

## See:
 - [Orb Author Intro](https://circleci.com/docs/2.0/orb-author-intro/#section=configuration)
 - [How To Author Executors](https://circleci.com/docs/2.0/reusing-config/#authoring-reusable-executors)
 - [Node Orb Executor](https://github.com/CircleCI-Public/node-orb/blob/master/src/executors/default.yml)
