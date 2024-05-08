# Contact Application

This is a web application for managing contacts.

## Deployment

This application is deployed using a GitHub Actions workflow that deploys the application to Azure. The workflow is defined in the `.github/workflows/deploy.yaml` file.

### Prerequisites

Before you can deploy the application, you need to set up the following secrets in your GitHub repository:

- `AZURE_USERNAME`: Your Azure username.
- `AZURE_PASSWORD`: Your Azure password.

These secrets are used by the Azure CLI to authenticate with Azure.

### Deploying the Application

To deploy the application, you simply need to push to the `master` branch of your repository. The GitHub Actions workflow will automatically run and deploy the application to Azure.

The workflow uses the `az deployment group create` command to deploy the application. The command uses the `deploy.json` and `deploy.parameters.json` files at the root of the repository to define the resources to deploy.

## Usage

After the application is deployed, you can access it at the URL provided in the output of the GitHub Actions workflow.