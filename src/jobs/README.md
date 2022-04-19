# Jobs

Easily author and add [Parameterized Jobs](https://circleci.com/docs/2.0/reusing-config/#authoring-parameterized-jobs) to the `src/jobs` directory.

Each _YAML_ file within this directory will be treated as an orb job, with a name which matches its filename.

Jobs may invoke orb commands and other steps to fully automate tasks with minimal user configuration.

View the included _[hello.yml](./hello.yml)_ example.

We currently have three jobs:

1. [build yml](./build.yml): Job used to build repos
2. [run_gcm yml](./run_gcm.yml): Runs a 1-hour 1x6 GCM with no ExtData
3. [run_fv3 yml](./run_fv3.yml): Runs a 6-hour FV3 standalone

## See:
 - [Orb Author Intro](https://circleci.com/docs/2.0/orb-author-intro/#section=configuration)
 - [How To Author Commands](https://circleci.com/docs/2.0/reusing-config/#authoring-parameterized-jobs)
 - [Node Orb "test" Job](https://github.com/CircleCI-Public/node-orb/blob/master/src/jobs/test.yml)
