# JupiterOne - j1-delete-suspended-aws-account-instances

This repository is used to programmatically delete JupiterOne integration instances for AWS accounts that have `Status: SUSPENDED`

## Requirements

You must have the following credentials available:
  
  **JuptiterOne**
  1. JupiterOne Account ID
  2. JupiterOne API Token

  **AWS**
  1. An `~/.aws` directory configured with a profile that is allowed to list AWS accounts for an organization

You also need to have Node.js installed locally, and either `yarn` or `npm` package manager

## Setup

1. Clone & navigate into this repository
    ```
    $ git clone git@github.com:ndowmon/j1-delete-suspended-aws-account-instances.git

    $ cd j1-delete-suspended-aws-account-instances
    ```

2. Install packages for this project
    ```
    # if using yarn
    $ yarn install

    # if using npm
    $ npm install
    ```

## Usage

```
# if using yarn
$ AWS_PROFILE='profile-with-access' yarn j1-delete-suspended-aws-account-instances --j1-account-id <YOUR_J1_ACCOUNT_ID> --j1-api-key <YOUR_J1_API_KEY>

# if using npm
$ AWS_PROFILE='profile-with-access' npm run j1-delete-suspended-aws-account-instances --j1-account-id <YOUR_J1_ACCOUNT_ID> --j1-api-key <YOUR_J1_API_KEY>
```

Help:

```
yarn j1-delete-suspended-aws-account-instances --help
yarn run v1.22.15
$ ./tools/j1-delete-suspended-aws-account-instances --help
Usage: j1-delete-suspended-aws-account-instances [options]

Programmatically delete all JupiterOne integration instances of AWS accounts that have 'Status: SUSPENDED'

Options:
  --j1-account-id <j1AccountId>  JupiterOne account id
  --j1-api-key <j1ApiKey>        JupiterOne api key
  --j1dev                        Use JupiterOne dev environment
  -h, --help                     display help for command
✨  Done in 0.26s.
```