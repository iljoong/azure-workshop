# Hands on Lab

Lab will use following samples:

[https://github.com/iljoong/azure-tf-paas](https://github.com/iljoong/azure-tf-paas)


## LAB 1: Run in Azure Cloud Shell

Provision/Deploy/Config Azure PaaS in Azure Cloud Shell environment.

Login to your Azure Cloud Shell and clone the sample: 

```
git clone https://github.com/iljoong/azure-tf-paas
```

Update `variables.tf` and run terraform. For basic terraform usage please refer [this doc](https://github.com/iljoong/azure-terraform#how-to-run).


You'll deloy a [sample app](https://github.com/iljoong/azure-tf-paas/blob/master/assets/apiapp.zip) using `zip deploy`.

Run this sample and test using following commands.

```
curl https://hostname.azurewebsites.net/api/events

curl -X POST https://hostname.azurewebsites.net/api/events -H "Content-Type: application/json" -d '{"message": "test"}'

curl https://hostname.azurewebsites.net/api/events
```

## LAB 2: Deploy App using ARM Template

First you need to upload a [sample app](https://github.com/iljoong/azure-tf-paas/blob/master/assets/apiapp.zip) to one of your blob storage (public access or private access with sas token).

Update `package_url` value and change value of `zipdeploy` to `false` in `veriables.tf`.

Run this sample and test it.

## LAB 3: Run in Your PC (Windows 10 or Linux)

> Tested in the latest __Windows 10__ environment.

### Install SW

You need to install [odbc driver](https://www.microsoft.com/en-us/download/confirmation.aspx?id=56567) and [sqlcmd](https://docs.microsoft.com/en-us/sql/tools/sqlcmd-utility?view=sql-server-ver15) tool in your PC to run successfully.

Enable `deploy_ps.tf` (i.e.: `deploy_ps.tf_ -> deploy.ps.tf, deploy_sh.tf -> deploy_sh.tf_`).

Run this sample and test using following commands.

## LAB 4: Advanced (IoT Service)

Use this sample [https://github.com/iljoong/azure-tf-iot](https://github.com/iljoong/azure-tf-iot).

This sample demonstrates how to provision/deploy `Azure Function` and config `Event trigger` and `HTTP trigger`.

Clone, run and test it.