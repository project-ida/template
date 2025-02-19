# template

Template python repo. Use this template for repos that contain jupyter notebooks.

In order for the notebook automation workflow (inside of .github folder) to work when you protect the main branch (see [rulesets](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/about-rulesets)), you'll need to use the `deploy keys` approach detailed in this [release-workflow-example](https://github.com/sbellone/release-workflow-example/tree/main) (note that we've chosen a different name for the secret - `ACTIONS_BOT_KEY`).

To create and use a deploy key:
- On your local machine run `ssh-keygen -t ed25519 -C "github-actions@github.com" -f key -N ""`
- Go to settings in the repo, find `Deploy keys` in `Security`
- Create a new key called `Github Actions`, paste in the **public** key from the result of running `ssh-keygen`, select `Allow write access`
- Go to settings in the repo, find `Actions` in `Secret and variables` inside of `Security`
- Create a `Repository secret` with the name `ACTIONS_BOT_KEY` (**the name has to be exactly thiss**), paste in the **private** key from the result of running `ssh-keygen`.
