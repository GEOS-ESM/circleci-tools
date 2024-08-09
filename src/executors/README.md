# Executors

This directory contains the [Parameterized Executors](https://circleci.com/docs/2.0/reusing-config/#executors) used in GEOS-ESM
CircleCI jobs. We currently define two executors:

1. gfortran
2. ifort
3. ifx

These are named to match the Fortran compiler.

They have on two optional parameters:

1. `resource_class` which defaults to `large`
2. `baselibs_version` which defaults to `v7.25.0`
3. `bcs_version` which defaults to `v11.6.0`

## See:
 - [Orb Author Intro](https://circleci.com/docs/2.0/orb-author-intro/#section=configuration)
 - [How To Author Executors](https://circleci.com/docs/2.0/reusing-config/#authoring-reusable-executors)
 - [Node Orb Executor](https://github.com/CircleCI-Public/node-orb/blob/master/src/executors/default.yml)
