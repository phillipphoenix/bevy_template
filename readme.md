# Bevy Template

This template comes with an empty Bevy project along with Github Actions for CI and release.
The CI and release actions are modified versions of the examples in the Bevy CI template repo:

https://github.com/bevyengine/bevy_github_ci_template

## Updates to the Github Actions

A few changes were necessary to make the actions run.

In the CI pipeline, Clippy needs to have added permissions to run:

`permissions: write-all`

This should be at the top level of the job.

Furthermore, each job that uploads a release in the release pipeline also needs added permissions to run:

`permissions: write-all`

This should be at the top level of the job.

This has been included in the template.
