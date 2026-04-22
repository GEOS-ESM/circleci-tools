# Executors

This directory contains the [Parameterized Executors](https://circleci.com/docs/2.0/reusing-config/#executors) used in GEOS-ESM
CircleCI jobs. Executors are named to match the Fortran compiler, with `_bcs` variants that include boundary conditions.

## Available Executors

### Without Boundary Conditions

1. [gfortran.yml](./gfortran.yml): GEOS-ESM gfortran (GCC) docker executor
2. [ifort.yml](./ifort.yml): GEOS-ESM ifort (Intel classic) docker executor
3. [ifx.yml](./ifx.yml): GEOS-ESM ifx (Intel LLVM) docker executor

### With Boundary Conditions

4. [gfortran_bcs.yml](./gfortran_bcs.yml): GEOS-ESM gfortran docker executor with boundary conditions
5. [ifort_bcs.yml](./ifort_bcs.yml): GEOS-ESM ifort docker executor with boundary conditions
6. [ifx_bcs.yml](./ifx_bcs.yml): GEOS-ESM ifx docker executor with boundary conditions

### Other

7. [docker.yml](./docker.yml): Generic GEOS-ESM docker executor (used for Docker image publishing)

## Parameters

All compiler executors accept the following parameters:

- `resource_class`: Resource class to use (default: `large`)
- `baselibs_version`: Version of Baselibs to use (default: `v9.9.0`)

The `_bcs` variants additionally accept:

- `bcs_version`: Version of boundary conditions to use (default: `v12.0.0`)

## See:
 - [Orb Author Intro](https://circleci.com/docs/2.0/orb-author-intro/#section=configuration)
 - [How To Author Executors](https://circleci.com/docs/2.0/reusing-config/#authoring-reusable-executors)
 - [Node Orb Executor](https://github.com/CircleCI-Public/node-orb/blob/master/src/executors/default.yml)
