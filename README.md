# poc_dependent_workflow_run
This repository shows how a project can run multiple workflows depending on each other

The example workflows run push to main and if a [conventional commit](https://www.conventionalcommits.org/en/v1.0.0/) is merged and the version upgrades it creates a release after the [github actions demo workflow](https://docs.github.com/en/actions/writing-workflows/quickstart#creating-your-first-workflow) succeeds.

## test by your own
You can test this behavior by pushing a commit to main with a conventional commit message:

* feat:   to update the minor version (e.g. 1.2.3 -> 1.3.0)
* fix:    to update the fix version (e.g. 1.2.3 -> 1.2.4)
* feat!:  to update the major version (e.g. 1.2.3 -> 2.0.0)
* chore:  nothing to update (e.g. 1.2.3 -> 1.2.3)

Keep in mind that a `feat` is something that changes the behavior of you application.
`feat!` is a breaking change (sometimes not backwards compatible!). 
