![Build](https://github.com/Azure/bicep-types-az/workflows/Build/badge.svg) [![codecov](https://codecov.io/gh/Azure/bicep-types-az/branch/main/graph/badge.svg)](https://codecov.io/gh/Azure/bicep-types-az) [![Build Status](https://dev.azure.com/msazure/One/_apis/build/status/OneBranch/BicepMirror-Types-Az/BicepMirror-Types-Az-Official?repoName=BicepMirror-Types-Az&branchName=main)](https://dev.azure.com/msazure/One/_build/latest?definitionId=179851&repoName=BicepMirror-Types-Az&branchName=main)

# bicep-types-az
Bicep type definitions for ARM resources

## Re-generating types from swagger
1. Under [GitHub Actions](https://github.com/anthony-c-martin/bicep-types-az/actions), run the "Update Types" workflow on the main branch. Usually you'll want to leave the git ref input as "master" for this workflow.
1. After ~2hrs, this action will generate a PR in this repo from a branch named `autogenerate`.
1. To workaround [this issue](https://github.com/peter-evans/create-pull-request/issues/48), close the PR and open it to trigger Merge Validation to run.
1. Merge the PR. Type differences can be reviewed by looking at the Markdown files in [/generated/docs](./generated/docs).

## Running generation locally
1. Ensure you have a copy of the [azure-rest-api-specs](https://github.com/Azure/azure-rest-api-specs) repo checked out locally.
1. Build the dotnet generator code:
    ```sh
    dotnet build
    ```
1. Change to the generator directory, and install dependencies:
    ```sh
    cd src/generator
    npm i
    ```
1. To run generation across the entire specs repo:
    ```sh
    npm run generate -- --specs-dir {path to azure-rest-api-specs}
    ```
1. To run generation for a single path in the specs repo (e.g. 'compute'):
    ```sh
    npm run generate -- --specs-dir {path to azure-rest-api-specs} --single-path compute
    ```
1. To see other available generation parameters, including debugging options:
    ```sh
    npm run generate -- --help
    ```

## Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.opensource.microsoft.com.

When you submit a pull request, a CLA bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., status check, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.
