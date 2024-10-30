# Github SignIn

###### for macbook
## install gh client, https://cli.github.com/
brew install gh

## github auth login
ivovosahlik@Ivos-MacBook-Pro ~ % gh auth login
? What account do you want to log into? GitHub.com
? What is your preferred protocol for Git operations on this host? HTTPS
? Authenticate Git with your GitHub credentials? Yes
? How would you like to authenticate GitHub CLI? Login with a web browser

! First copy your one-time code: XXXX-XXXX (schovany :) )
Press Enter to open github.com in your browser...  
✓ Authentication complete.
- gh config set -h github.com git_protocol https
  ✓ Configured git protocol
  ✓ Logged in as ivosahlik

## github auth status
ivovosahlik@Ivos-MacBook-Pro ~ % gh auth status
github.com
✓ Logged in to github.com account ivosahlik (keyring)
- Active account: true
- Git operations protocol: https
- Token: gho_************************************
- Token scopes: 'gist', 'read:org', 'repo', 'workflow'

## show github token
ivovosahlik@Ivos-MacBook-Pro ~ % gh auth token

## set intellij idea, choose token

####### for win it will be the same, is need to use some tools for it
https://www.techielass.com/install-github-cli-on-windows/



# Using Actions in Workflows

This GitHub Actions workflow demonstrates how to use actions within our GitHub Actions workflow to test a React application.

## Workflow Details

- **Trigger**: This workflow is triggered manually from the UI.

- **Runner**: It runs on an Ubuntu environment provided by GitHub-hosted runners.

## Workflow Steps

1. **Checkout Code**: The workflow checks out the code from the repository using the `actions/checkout` action.

2. **Set up Node.js**: The `actions/setup-node` action sets up a Node.js environment with version 20.x. By specifying the `.x` option, we ensure that the latest release of the version 20 will be used.

3. **Install Dependencies**: It installs project dependencies using `npm ci`.

4. **Test**: It runs tests for the application using `npm run test`.

We use the `defaults` option in our `job` definition to define the common `working-directory` for the `run` commands executed from within steps. This default only applies to the `run` commands. 