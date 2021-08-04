# Azure DevOps Pipelines for Ship

Welcome to Ship's [Azure DevOps Pipelines](https://azure.microsoft.com/en-us/services/devops/pipelines/) support! To
learn how Ship can help you with your Azure DevOps Pipelines, please
see [our website](https://www.shipapp.io/integrations/azure-devops-pipelines).

To get Ship integrated, perform these steps:

## Step 1: Add the Ship App to your GitHub Organization

This can be done from our [GitHub Marketplace listing](https://github.com/marketplace/shipapp-io). Ship needs to
integrate with Github for user authentication.

## Step 2: Get your Ship API Key

Email [hello@shipapp.io](mailto:hello@shipapp.io) to get yours!

## Step 3: Setup Webhooks

* For each Project in Azure DevOps you need to set up a Service Hook. As an example, that might be
  at https://dev.azure.com/YOU_ORG/YOUR_PROJECT/_settings/serviceHooks
* Once you’ve got there, create a new service hook with the following details:
    * Service is "Web Hooks"
    * Trigger type is "Run State Changed" . Leave the filters as "[Any]"
    * "URL" is https://api.backend.shipapp.io/azureDevOps
    * "HTTP headers" will include an API Key - this is what you'll get from us in Step 2.
    * The remaining options can be "[All]"
    * Save, and run a test

You should start seeing events in Ship the next time your pipeline runs!

## Support

If you need any help please drop us a line at [support@shipapp.io](mailto:support@shipapp.io) .

Happy Shipping!
