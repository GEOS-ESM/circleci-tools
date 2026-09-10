# Executors

This directory contains the [Parameterized Executors](https://circleci.com/docs/2.0/reusing-config/#executors) used in GEOS-ESM
CircleCI jobs. Executors are named to match the Fortran compiler, with `_bcs` variants that include boundary conditions.

## Available Executors

### Without Boundary Conditions

1. [gfortran.yml](./gfortran.yml): GEOS-ESM gfortran (GCC) docker executor
2. [gfortran-16.yml](./gfortran-16.yml): GEOS-ESM gfortran 16 docker executor
3. [ifort.yml](./ifort.yml): GEOS-ESM ifort (Intel classic) docker executor
4. [ifx.yml](./ifx.yml): GEOS-ESM ifx (Intel LLVM) docker executor

### With Boundary Conditions

5. [gfortran_bcs.yml](./gfortran_bcs.yml): GEOS-ESM gfortran docker executor with boundary conditions
6. [gfortran-16_bcs.yml](./gfortran-16_bcs.yml): GEOS-ESM gfortran 16 docker executor with boundary conditions
7. [ifort_bcs.yml](./ifort_bcs.yml): GEOS-ESM ifort docker executor with boundary conditions
8. [ifx_bcs.yml](./ifx_bcs.yml): GEOS-ESM ifx docker executor with boundary conditions

### With Regression Test Data

9. [gfortran_regression.yml](./gfortran_regression.yml): GEOS-ESM gfortran docker executor with regression test data
10. [gfortran-16_regression.yml](./gfortran-16_regression.yml): GEOS-ESM gfortran 16 docker executor with regression test data
11. [ifort_regression.yml](./ifort_regression.yml): GEOS-ESM ifort docker executor with regression test data
12. [ifx_regression.yml](./ifx_regression.yml): GEOS-ESM ifx docker executor with regression test data

### Other

13. [docker.yml](./docker.yml): Generic GEOS-ESM docker executor (used for Docker image publishing)

## Parameters

All compiler executors accept the following parameters:

- `resource_class`: Resource class to use (default: `large`)
- `baselibs_version`: Version of Baselibs to use (default: `v9.13.0`)

The `_bcs` variants additionally accept:

- `bcs_version`: Version of boundary conditions to use (default: `v12.0.0`)

The `_regression` variants additionally accept:

- `regression_version`: Version of regression test data to use (default: `v1.0.0`)

## See:
 - [Orb Author Intro](https://circleci.com/docs/2.0/orb-author-intro/#section=configuration)
 - [How To Author Executors](https://circleci.com/docs/2.0/reusing-config/#authoring-reusable-executors)
 - [Node Orb Executor](https://github.com/CircleCI-Public/node-orb/blob/master/src/executors/default.yml)
