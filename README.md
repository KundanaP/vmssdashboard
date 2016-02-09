# VMSS Dashboard
Dashboard to show Azure VM Scale Set status and properties

## Installation
1. Install Python 3.x.
2. Install the azurerm REST wrappers for Microsoft Azure: pip install azurerm
3. Install pygame: E.g. on Windows go here: <a href="http://www.lfd.uci.edu/~gohlke/pythonlibs/#pygame
">Python Extension Packages - pygame</a>
4. Clone this repo locally.
5. Register an Azure application, create a service principal and get your tenant id. See "Using vmssdashboard".
6. Put in values for your application, along with your resource group name, and VM Scale Set name in vmssconfig.json.
7. Run: python vmssdashboard.py

## Using vmssdashboard
To use this app (and in general to access Azure Resource Manager from a program without going through 2 factor authentication) you need to register your application with Azure and create a "Service Principal" (an application equivalent of a user). Once you've done this you'll have 3 pieces of information: A tenant ID, an application ID, and an application secret. You will use these to populate the vmssconfig.json file. For more information on how to get this information go here: <a href ="https://azure.microsoft.com/en-us/documentation/articles/resource-group-authenticate-service-principal/">Authenticating a service principal with Azure Resource Manager</a>. See also: <a href="https://msftstack.wordpress.com/2016/01/05/azure-resource-manager-authentication-with-python/">Azure Resource Manager REST calls from Python</a>.
