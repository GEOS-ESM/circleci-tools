# Commands

This directory contains [Reusable Commands](https://circleci.com/docs/2.0/reusing-config/#authoring-reusable-commands) that are used
in the GEOS-ESM CircleCI jobs.

Each _YAML_ file within this directory will be treated as an orb command, with a name which matches its filename.

## Available Commands

### Build

1. [buildinstall.yml](./buildinstall.yml): Build and install (retry after fail)
2. [buildtarget.yml](./buildtarget.yml): Build a specific CMake target (retry after fail)
3. [buildtests.yml](./buildtests.yml): Build unit tests
4. [cmake.yml](./cmake.yml): Run CMake configuration
5. [runtests.yml](./runtests.yml): Run unit tests via ctest
6. [versions.yml](./versions.yml): Print compiler and tool versions

### Checkout

7. [checkout_branch_on_fixture.yml](./checkout_branch_on_fixture.yml): Checkout a specific branch on a fixture repo
8. [checkout_branch_on_subrepo.yml](./checkout_branch_on_subrepo.yml): Mepo checkout a branch on a subrepo
9. [checkout_feature_branch_on_fixture_allow_fail.yml](./checkout_feature_branch_on_fixture_allow_fail.yml): Checkout the PR feature branch on a fixture, allowing failure
10. [checkout_fixture.yml](./checkout_fixture.yml): Checkout a fixture repository
11. [checkout_if_exists.yml](./checkout_if_exists.yml): Mepo checkout-if-exists
12. [checkout_mapl_branch.yml](./checkout_mapl_branch.yml): Mepo checkout the current MAPL branch
13. [checkout_mapl3_release_branch.yml](./checkout_mapl3_release_branch.yml): Mepo checkout release/MAPL-v3 branches

### Mepo

14. [mepoclone.yml](./mepoclone.yml): Mepo clone external repos
15. [mepodevelop.yml](./mepodevelop.yml): Mepo develop repos (e.g. GEOSgcm_GridComp, GEOSgcm_App, GMAO_Shared)

### GCM Experiment

16. [create_gcm_expt.yml](./create_gcm_expt.yml): Create a GCM experiment directory
17. [make_onehour_history.yml](./make_onehour_history.yml): Set geosgcm_prog collection to hourly output
18. [run_gcm_experiment.yml](./run_gcm_experiment.yml): Run a GCM experiment
19. [run_makeoneday.yml](./run_makeoneday.yml): Run the makeoneday script

### FV3 Experiment

20. [run_fv3_setup.yml](./run_fv3_setup.yml): Run fv3_setup
21. [run_fv3_experiment.yml](./run_fv3_experiment.yml): Run an FV3 standalone experiment

### GOCART Tests

22. [run_gocart_tests.yml](./run_gocart_tests.yml): Run GOCART tests against a GEOSgcm build

### Tutorials

23. [run_tutorial.yml](./run_tutorial.yml): Run a MAPL tutorial

### Artifacts

24. [compress_artifacts.yml](./compress_artifacts.yml): Compress log artifacts for storage

## See:
 - [Orb Author Intro](https://circleci.com/docs/2.0/orb-author-intro/#section=configuration)
 - [How to author commands](https://circleci.com/docs/2.0/reusing-config/#authoring-reusable-commands)
