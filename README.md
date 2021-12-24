# Provision API Management Instance with Azure DevOps

This repository contains sample ARM template, parameter file, and GitHub Actions flow to provision Azure API Management instance with system assigned managed identity enabled.
For more details, check my blog entry below (in Japanese).

> Azure AD と OpenID Connectで連携した GitHub Actions で Azure API Management インスタンスを 生成する<br>
> [https://logico-jp.io/2021/12/24/provision-api-management-instance-using-github-actions-integrated-with-azure-ad-via-openid-connect/](https://logico-jp.io/2021/12/24/provision-api-management-instance-using-github-actions-integrated-with-azure-ad-via-openid-connect/)

GitHub Actions flow file (`provisioning-instance-on-Linux-runner.yaml`) is not located in `.github/workflows/` to avoid provisioning lots of instances. To enable GitHub Actions flow, the YAML file should be located in designated directory (i.e., `.github/workflows/provisioning-instance-on-Linux-runner.yaml`).

## Reference

The following items are used in this sample (as of December 24, 2021).

- GitHub Action
  - Azure login<br>
    [https://github.com/marketplace/actions/azure-login](https://github.com/marketplace/actions/azure-login)  
  - Deploy Azure Resource Manager (ARM) Template<br>
    [https://github.com/marketplace/actions/deploy-azure-resource-manager-arm-template](https://github.com/marketplace/actions/deploy-azure-resource-manager-arm-template)
  - Azure CLI Action<br> 
    [https://github.com/marketplace/actions/azure-cli-action](https://github.com/marketplace/actions/azure-cli-action)
  - Checkout<br>
    [https://github.com/marketplace/actions/checkout](https://github.com/marketplace/actions/checkout)
- ARM template
  - [https://github.com/Azure/azure-quickstart-templates/tree/master/quickstarts/microsoft.apimanagement/api-management-create-with-msi](https://github.com/Azure/azure-quickstart-templates/tree/master/quickstarts/microsoft.apimanagement/api-management-create-with-msi) 
- Documents
  - Use GitHub Actions to connect to Azure<br>[https://docs.microsoft.com/azure/developer/github/connect-from-azure](https://docs.microsoft.com/azure/developer/github/connect-from-azure)
  -  Configuring OpenID Connect in Azure<br>
     [https://docs.github.com/en/actions/deployment/security-hardening-your-deployments/configuring-openid-connect-in-azure](https://docs.github.com/en/actions/deployment/security-hardening-your-deployments/configuring-openid-connect-in-azure)
