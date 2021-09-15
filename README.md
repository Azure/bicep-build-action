# 💪 Bicep Build Action [![Build](https://github.com/Azure/bicep-build-action/actions/workflows/ci.yml/badge.svg)](https://github.com/Azure/bicep-build-action/actions/workflows/ci.yml)

GitHub Action that builds a [Bicep](https://docs.microsoft.com/EN-US/azure/azure-resource-manager/bicep/overview) main file and outputs a generated ARM Template file.

## When to use

The action is particularly useful for Continuous Integration scenarios where you want to validate the ARM template further on your workflow and/or publish it as an artifact.

## Getting Started

### Prerequisites

If your GitHub Actions workflows are running on a [self-hosted runner](https://docs.github.com/en/actions/hosting-your-own-runners/about-self-hosted-runners):

- [Azure CLI](https://docs.microsoft.com/en-us/azure/azure-resource-manager/bicep/install#azure-cli) 2.20.0 or later installed
- File write permission on the runner as this action creates an ARM template file dynamically.

### Usage

```yml
steps:
  - name: Bicep Build
    uses: Azure-Samples/bicep-build-action@v1.0.0
    with:
      bicepFilePath: main.bicep
      outputFilePath: azuredeploy.json
```

### Inputs

| Name | Description | Required | Default value |
| --- | --- | --- | --- |
| `bicepFilePath` | Bicep main file path | false | `./main.bicep` |
| `outputFilePath` | Path where the ARM template file will be created | false | `./azuredeploy.json` |  ARM |

# Contributing

This project welcomes contributions and suggestions. Most contributions require you to
agree to a Contributor License Agreement (CLA) declaring that you have the right to,
and actually do, grant us the rights to use your contribution. For details, visit
https://cla.microsoft.com.

When you submit a pull request, a CLA-bot will automatically determine whether you need
to provide a CLA and decorate the PR appropriately (e.g., label, comment). Simply follow the
instructions provided by the bot. You will only need to do this once across all repositories using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/)
or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.
