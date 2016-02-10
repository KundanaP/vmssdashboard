\# VMSS Dashboard
Dashboard to show Azure VM Scale Set status and properties

![Image of VMSS Dashboard](https://raw.githubusercontent.com/gbowerman/vmssdashboard/master/docs/vmssdash-img.png)


## Installation
  1. Install Python 3.x.
  2. Install the azurerm REST wrappers for Microsoft Azure: pip install azurerm
  3. Install [pygame](http://www.pygame.org/download.shtml)
  4. Clone this repo locally.
  5. Register an Azure application, create a service principal and get your tenant id. See "Using vmssdashboard".
  6. Put in values for your application, along with your resource group name, and VM Scale Set name in vmssconfig.json.
  7. Run: python vmssdashboard.py

## Using vmssdashboard To use this app (and in general to access Azure

Resource Manager from a program without going through 2 factor
authentication) you need to register your application with Azure and
create a "Service Principal" (an application equivalent of a
user). Once you've done this you'll have 3 pieces of information: A
tenant ID, an application ID, and an application secret. You will use
these to populate the vmssconfig.json file. For more information on
how to get this information go here: [Authenticating a service
principal with Azure Resource Manager][service-principle]. See also:
[Azure Resource Manager REST calls from Python][python-auth].

[service-principle]: https://azure.microsoft.com/en-us/documentation/articles/resource-group-authenticate-service-principal/
[python-auth]: https://msftstack.wordpress.com/2016/01/05/azure-resource-manager-authentication-with-python