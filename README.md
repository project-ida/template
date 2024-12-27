# template

Template python repo

In order for the notebook automation workflow (inside of .github folder) to work when you protect the main branch (see [rulesets](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/about-rulesets)), you'll need to use the `deploy keys` approach detailed in this [release-workflow-example](https://github.com/sbellone/release-workflow-example/tree/main) (note that we've chosen a different name for the secret - `ACTIONS_BOT_KEY`).
