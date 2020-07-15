## Osome GitHub

### Workflows

- :boxing_glove: [`bump-version-on-dispatch`](#boxing_glove-bump-version-on-dispatch)

- :fist_left: [`bump-version-on-merge`](#fist_left-bump-version-on-merge)

- :ledger: [`storybook`](#ledger-storybook)

### Adding workflows to public repositories

In public repositories you can choose one of our workflow templates when creating a new workflow from the **Actions** tab:

<img src="https://user-images.githubusercontent.com/900311/87473296-e075d980-c629-11ea-9613-5b314edd5182.png" height="256px" />


### Adding workflows to private repositories

Unfortunately, the above functionality is not supported in private repositories. But still instead of manually copying and pasting workflow files you can automate the process a bit and ask [@osome-bot](https://github.com/osome-bot) to create a pull request for you.

To do it, open **[Actions](https://github.com/OsomePteLtd/.github/actions?query=workflow%3A%22Install+workflow%22)** tab, select **Install workflow** and fill in repository name and workflow name fields in the **Run workflow** dropdown:

<img src="https://user-images.githubusercontent.com/900311/87471298-cf779900-c626-11ea-940d-e572ea9f54bb.png" height="256px" />

---

### :boxing_glove: `bump-version-on-dispatch`

#### Features

- Provides support for triggering package deployment with a **[Slack bot](https://github.com/OsomePteLtd/slack-bot)**.
- Flexible releases, best fitted for packages that are under active development and/or released often.

#### Requirements

- Requires additional workflows that will run on any tagged push and will take care of deployment.

### :fist_left: `bump-version-on-merge`

#### Features

- Provides support for triggering package deployment whenever a pull request is merged into a default branch.
- A more strict approach to managing releases, best fitted for packages that are hosted on NPM or GitHub Package Registry.

#### Requirements

- Requires additional workflows that will run on any tagged push and will take care of deployment.

### - :ledger: `storybook`
-

### - :package: `deploy-to-npm`

### - :package: `deploy-to-s3`

- Provides support for deploying packages to an S3 bucket. 
- Requires `DEPLOYMENT_ENVIRONMENT_URL` secret to be set to environment URL, with `{0}` masking the environment, e.g. `https://agent.{0}.osome.club/`.
