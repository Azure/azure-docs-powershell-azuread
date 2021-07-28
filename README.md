# Microsoft AzureAD 2.0 PowerShell Module and AzureAD 2.0 Preview PowerShell Module Documentation

Welcome to the open-source [documentation](https://docs.microsoft.com/azure) of the [Microsoft AzureAD 2.0 PowerShell Module](https://docs.microsoft.com/powershell/module/azuread/?view=azureadps-2.0) and the [Microsoft AzureAD 2.0 Preview PowerShell Module](https://docs.microsoft.com/powershell/module/azuread/?view=azureadps-2.0-preview). Please review this README file to understand how you can assist in contributing to the Microsoft Azure documentation.

## Getting Started

Contributing to open source is more than just providing updates, it's also about letting us know when there is an issue. Read our [Contributing guidance](CONTRIBUTING.md) to find out more.

> [!IMPORTANT]
> New pull requests **MUST** always be created against the master branch which is the default branch in the main repository and not the live branch. PRs created against the live branch will not be accepted.

### Prerequisites

You've decided to contribute, that's great! To contribute to the documentation, you need a few tools.

Contributing to the documentation requires a GitHub account. If you don't have an account, follow the instructions for the [GitHub account setup](https://docs.microsoft.com/contribute/get-started-setup-github) from our contributor guide.

#### Download

Install the following tools:

* [Git](https://git-scm.com/download)
* [Visual Studio Code](https://code.visualstudio.com/Download)
* [Docs Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) extension for Visual Studio Code

#### Install

Follow the instructions provided in the [Install content authoring tools](https://docs.microsoft.com/contribute/get-started-setup-tools) from our contributor guide.

## License

Please refer to [LICENSE](LICENSE), [LICENSE-CODE](LICENSE-CODE) and [ThirdPartyNotices](ThirdPartyNotices.md) for all Licensing information.

## Code of Conduct

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information, see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

## Current State of Repo
We are currently aware of the backlog for this repo and are working to address this.  Please be aware that if you have any updates to automatically generated reference content, you should create an issue and not a PR.  The issue will then be created into a bug and triaged accordingly.  We do this because the reference content must mirror the &#42;dll-help.xml file and subsequent updates to the reference content may overwrite any changes made through the repo.  Capturing it in the source code ensures that this does not occur.  Any PR with changes to automatically generated reference content will be closed.  

Automatically generated reference content is any of the content under this Reference node, such as [Get-AzureADUser](https://docs.microsoft.com/powershell/module/AzureAD/Get-AzureADUser?view=azureadps-2.0)

This only applies to reference content and not conceptual content.  Pull requests for changes to conceptual content are accepted and encouraged.  An example of the conceptual content is the [Overview](https://docs.microsoft.com/powershell/azure/active-directory/overview?view=azureadps-2.0) or a scenario such as [importing data](https://docs.microsoft.com/powershell/azure/active-directory/importing-data?view=azureadps-2.0).
