---

copyright:
  years: 2018, 2021
lastupdated: "2021-09-13"

keywords: apps, deploy, virtual server, App Service, vsi, virtual machine, delivery pipeline, virtual deployment

subcollection: virtual-servers

---

{:external: target="_blank" .external}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:table: .aria-labeledby="caption"}

# Deploying to a virtual server
{: #deploying-to-a-virtual-server}

If you have a Pay-As-You-Go account, you can use the {{site.data.keyword.cloud}} [App Service](https://{DomainName}/developer/appservice/starter-kits){: external} to deploy your apps to many types of environments, including virtual server instances. A virtual server instance emulates a bare metal machine and is a common deployment choice when you move on-premises workloads to the cloud.
{: shortdesc}

A virtual server instance offers better transparency, predictability, and automation for all workload types when compared to other configurations. Combine it with a bare metal server to create unique workload combinations. For example, you can create high-performance database logic or machine learning with bare metal and GPU configurations that run a Debian Linux-based operating system.

Provisioning a virtual server instance and deploying it can be a complex and time-consuming process, but you can get up and running quickly by using the {{site.data.keyword.cloud_notm}} App Service.

Services don't bind to the virtual server instance. You cannot add services to an application in a virtual server. However, you can still use any {{site.data.keyword.cloud_notm}} service in an application that is running in a virtual server if you made the credentials available to the app that is running in the virtual server instance.
{: important}

## Deploying apps
{: #create-deploy-vsi}

The App Service provisions a virtual server instance for you, loads an image that includes your app, creates a DevOps toolchain, and initiates the first deployment cycle for you.

1. [Create an app](/docs/apps?topic=apps-tutorial-scratch#tutorial-scratch){: external}.
2. Click **Configure continuous delivery** from the App details page.
3. Select **Deploy to a Virtual Server**, along with the region in which to run your server.

## How the deployment process works
{: #how-the-deployment-process-works}

The virtual server deployment process consists of several key technologies that include Terraform, pipeline enablement, API key management (Git operations), and understanding the toolchain process.

### Deploying through Terraform
{: #deploying-through-terraform}

You can deploy any of the App Service starter kits in a dynamically created virtual instance through [Terraform](/docs/terraform?topic=terraform-getting-started), an open source infrastructure as code framework.

### Enabling your pipeline deployment
{: #enabling-your-pipeline-deployment}

When you create a starter kit that uses the {{site.data.keyword.cloud_notm}} [App Service](https://{DomainName}/developer/appservice/starter-kits){: external}, the virtual server instance is enabled. After the app is created, you can then choose where you want to deploy the app. The starter kits are enabled to support deployment by using a Continuous Delivery toolchain. Starter kits can target Kubernetes, Cloud Foundry, and Virtual Server Instances. The toolchain includes a source code repository and a deployment pipeline.

The virtual server option works in phases. First, the app code is prepared and stored into a GitLab Git repository and the source code creates a toolchain with a pipeline. The pipeline is defined to build the code and package it into a Debian Package manager format. Then, Terraform provisions a virtual instance. Finally, the app is deployed, installed, and started inside the running virtual image and its health is validated.

The pipeline uses a set of user account properties and a fresh SSH key pair to deploy to infrastructure. These properties are automatically passed into the toolchain, but not stored in Git source code for security reasons.

To view these environment properties, complete the following steps.

1. From the App details page, click **View toolchain**.
2. Click the **Delivery Pipeline** tile.
3. Click the **Stage Configure** icon, then click **Configure Stage** on the build stage.
4. Click the **Environment Properties** tab to view the properties. Use the following table to learn about the properties that are available.

| Property  | Description  |
|-----------|--------------|
| `TF_VAR_ibm_sl_api_key` | The [infrastructure API key](/docs/virtual-servers?topic=virtual-servers-deploying-to-a-virtual-server#iaas-key) is from the classic infrastructure console. |
| `TF_VAR_ibm_sl_username` | The [infrastructure username](/docs/virtual-servers?topic=virtual-servers-deploying-to-a-virtual-server#user-key) that identifies the classic infrastructure account |
| `TF_VAR_ibm_cloud_api_key` | The {{site.data.keyword.cloud_notm}} [API key](/docs/virtual-servers?topic=virtual-servers-deploying-to-a-virtual-server#platform-key) is used to enable service creation. |
| `PUBLIC_KEY` | [Public key](/docs/virtual-servers?topic=virtual-servers-deploying-to-a-virtual-server#public-key) that is defined to enable access to the virtual server instance. |
| `PRIVATE_KEY` | [Private key](/docs/virtual-servers?topic=virtual-servers-deploying-to-a-virtual-server#public-key) that is defined to enable access to the virtual server instance. You must use `\n` newline style formatting. |
| `VI_INSTANCE_NAME` | Auto-generated name for the virtual server instance |
| `GIT_USER` | If you set the [Terraform state](/docs/virtual-servers?topic=virtual-servers-deploying-to-a-virtual-server#tform-state) to store the state of the apply command, the GitLab username is required. |
| `GIT_PASSWORD` | If you set the [Terraform state](/docs/virtual-servers?topic=virtual-servers-deploying-to-a-virtual-server#tform-state) to store the state of the apply command, the GitLab password is required. |
{: caption="Table 1. Environment variables to change for enablement" caption-side="top"}


#### Classic infrastructure API key
{: #iaas-key}

Terraform requires a classic infrastructure API key to create infrastructure resources. The API key is obtained automatically during deployment. To manually retrieve a key, complete the following steps.

1. Go to the user list by clicking **Manage** > **Access (IAM)** > **Users**.
2. Click a username, and then click **User details**.
3. Click **Add a classic infrastructure key** in the API keys section.
4. Copy or download the API key `TF_VAR_ibm_sl_api_key`, and save it in a safe place. You can retrieve the details of the API key later by using the **View details** option from the **Actions** ![List of actions icon](../icons/action-menu-icon.svg) menu.
5. Paste the copied API key value into the toolchain configuration to replace the `TF_VAR_ibm_sl_api_key`.

For more information, see [Managing classic infrastructure API keys](/docs/account?topic=account-classic_keys#classic_keys) and [Classic infrastructure permissions](/docs/account?topic=account-infrapermission).

#### Classic infrastructure user name
{: #user-key}

The classic infrastructure username is also automatically obtained and used during deployment. To manually obtain the username, complete the following steps.

1. Go to the user list by clicking **Manage** > **Access (IAM)** > **Users**.
2. Click a username, and then click **User details**.
3. Locate the **VPN Username** property.
4. Cut and paste this value and replace the toolchain configuration `TF_VAR_ibm_sl_username`.

#### {{site.data.keyword.cloud_notm}} API key
{: #platform-key}

To create platform-level services in Terraform, like databases and compose services, the {{site.data.keyword.cloud_notm}} API key is automatically obtained and stored as an environment variable in your pipeline. To manually retrieve an {{site.data.keyword.cloud_notm}} API key, complete the following steps.

1. Go to the user list by clicking **Manage** > **Access (IAM)** > **Users**.
2. Click a username, and then click **User details**.
3. Locate the API keys section, and click **Create an IBM Cloud API key**.
4. Enter a name and description and click **Create**.
5. When the window opens, click **Show** to review the key.
6. Copy and paste the key into the clipboard, or download the key.
7. Replace the value in the toolchain configuration `TF_VAR_ibm_cloud_api_key` with the value that was generated.

#### Public and private keys
{: #public-key}

You need a toolchain to install the Debian packaging into the virtual server instance. The deployment infrastructure automatically generates a private and public SSH key pair to transfer the Git contents to the instance.

To manually generate an SSH key pair, use the following steps:
1. In your client, use the following instructions to create a [public and private key pair](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/){: external}.
2. Go to the **Infrastructure SSH keys view** by clicking **Menu** > **Classic infrastructure** > **Devices** > **Manage** > **SSH Keys**.
3. Click **Add**.
4. Copy the contents of the public key that you previously created and paste it into the key contents.
5. Give the key a name and click **Add**.

The private key must be on a single line. Replace new lines with `\n`. See the following example.
{: tip}

```
---------BEGIN RSA KEY----------\nasdfasdfeqwtqf13rf1eqwfwe\netq3efaewf23fa23f23f\n.....\n----------END RSA KEY-------------
```
{: screen}

#### Enabling Terraform state
{: #tform-state}

Terraform supports storing the state of the Terraform `apply` command. This state file runs the `apply` command a second time to determine whether any of the Terraform configuration files changed. The state is stored in the Git repo where the app and configuration are automatically set up.

To enable the state storage, `GIT_USER` and `GIT_PASSWORD` are automatically configured as properties in the toolchain environment variables. If you need to access these values, follow these steps:

1. From the toolchains view, access the Git repo from the code tool.
2. In GitLab, click the **Profile icon** and then click **Settings**.
3. Click **Account** and copy the username and replace the `GIT_USER` value.
4. Click **Access Tokens**.
5. Give your token an appropraite name, select a scope, and click **Create Personal Access Token**.
6. Click **Copy** from the `Your New Personal Access Token` field, and replace the value of the `GIT_PASSWORD` in the toolchain properties.

The Terraform state is stored in a branch that is called `terraform`, and doesn't trigger the pipeline to run if it was changed.

### Enabling Git operations
{: #git-repo-vsi}

When the app is deployed to {{site.data.keyword.cloud_notm}}, a GitLab repository is created to host the code for source code management. You can use Git operations to enable teams to work and deliver changes to your app. The folders included in this repository and an explanation of their contents.

#### Debian folder
{: #debian-folder}

The `debian` folder holds the configuration that is required to enable the packaging of the app into a Debian package.

#### Terraform folder
{: #terraform-folder}

The `terraform` folder holds the configuration for the infrastructure as code that can be used to provision infrastructure resources. The file `main.tf` is the main source for changing the options for your Terraform configuration.

```json
resource "ibm_compute_vm_instance" "vm1" {
    hostname = "${var.vi_instance_name}"
    domain = "example.com"
    os_reference_code = "DEBIAN_8_64"
    datacenter = "${var.datacenter}"
    network_speed = 100
    hourly_billing = true
    private_network_only = false
    cores = 1
    memory = 1024
    disks = [25]
    local_disk = false
    ssh_key_ids = [
        "${ibm_compute_ssh_key.ssh_key_gip.id}"
    ]
}
```
{: codeblock}

You can also provision bare metal servers with Terraform. For more information, see [IBM Terraform Provider Documentation](/docs/terraform?topic=terraform-getting-started){: external} and [IBM Terraform Provider GitHub Repo](https://github.com/IBM-Cloud/terraform-provider-ibm){: external}.

The `variables.tf` can be used to change the data center you want to target to create the virtual instance. To see the list of defined data centers on the platform, see [Data centers](https://www.ibm.com/cloud/data-centers/){: external}.

By default, the Terraform file is configured for Washington and `wdc04`.

```json
variable "datacenter" {
   description = "Washington"
   default = "wdc04"
}
```
{: codeblock}

### Understanding the toolchain stages
{: #toolchain-stages-vsi}

The toolchain shows infrastructure and app deployment in one simple pipeline. Break the infrastructure as code part into one pipeline and the app deployment into another pipeline.

The toolchain process has five stages.

1. The build stage clones the Git repo and packages the code into a Debian package.
2. The Terraform plan stage prepares a Terraform plan.

  ```console
  terraform init -input=false
  terraform validate
  terraform plan -var "ssh_public_key=$PUBLIC_KEY" -input=false -out tfplan
  ```
  {: pre}
3. The Terraform apply stage applies the Terraform configuration and waits until the IP address of the virtual server is available.

  ```console
  terraform apply -auto-approve -input=false tfplan
  terraform output "host ip" > hostip.txt
  ```
  {: pre}
4. The deployment, install, start stage moves the Debian package that is built in the first stage into the running virtual server, installs it and then starts it.
5. The health check stage validates the health endpoint is available on the app and then completes the pipeline.

To access the app after it starts, check the logs of the Health Check Stage. Click the URL links listed in the logs that show the IP address and port of the app.
