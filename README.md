## Product Overview
RackWare Management Module (RMM) migrations are an automated, easy, and convenient process to migrate existing workloads from your current location to IBM Cloud.
RMM creates an exact duplicate of a running image without the burden of rebuilding or recreating template images and applications. It decouples the application stack from the underlying platform, allowing it to be ported to the IBM Cloud infrastructure with ease.
RMM simplifies migration of large, complex environments through a simple interface and reduces the time required from weeks to days, reducing capital and operating expenses. RMM includes discovery, analysis, and automation features, allowing all  processes to be fast, easy, and error-free.

## Supported Migration 
For additional information on the supported migrations, see below:
-	[VMware virtual machine (On-premises) to IBM Cloud VPC virtual servers](https://cloud.ibm.com/docs/cloud-infrastructure?topic=cloud-infrastructure-migrating-images-vmware-vpc)
-	[VMware virtual machine (IBM Cloud classic) to IBM Cloud VPC virtual servers](https://cloud.ibm.com/docs/cloud-infrastructure?topic=cloud-infrastructure-migrating-images-vmware-vpc-classic)
-	[Hyper-V virtual machine (On-premises, IBM Cloud Classic) to IBM Cloud VPC virtual servers](https://cloud.ibm.com/docs/cloud-infrastructure?topic=cloud-infrastructure-migrating-images-vmware-vsi)
-	[On-premises physical machines to IBM Cloud VPC virtual servers](https://cloud.ibm.com/docs/cloud-infrastructure?topic=cloud-infrastructure-migrating-on-prem-cloud-vpc)
-	[GCP, AWS, Azure, virtual machines and OCI Baremetal to IBM Cloud VPC virtual servers](https://cloud.ibm.com/docs/cloud-infrastructure?topic=cloud-infrastructure-aws-azure-gcp-and-oci-workloads-to-ibm-cloud-vpc-vsi-migration-with-rackware-rmm)
-	[IBM Cloud classic bare metal to IBM Cloud classic bare metal](https://cloud.ibm.com/docs/cloud-infrastructure?topic=cloud-infrastructure-p-p-migration-bare-metal-overview)

## Key Benefits 
-	Live and Non-Disruptive Migrations
-	Highly secure and efficient data transfer
-	Auto discovery of VMware vSphere and Hyper-V workloads 
-	Auto provision of target Virtual Server Instance
-	Include/Exclude Lists: Capture and sync only specific files and directories rather than entire systems
-	Delta Sync: Sync only the changed parts of files during the final data sync, drastically lowering cutover times
-	Network optimization: bandwidth usage limitations, compression and check point restart for all sync operations

For more information, visit https://www.rackwareinc.com/cloud-migration

## Pre-requisites
Review the following pre-requisites for RMM software installation:
-	Make sure that you have IBM Cloud account permissions and access.
-	Identify the region and zone where you want to deploy the RMM server
-	For more information about IBM Cloud VPC, see  https://cloud.ibm.com/docs/vpc?topic=vpc-getting-started

## Software installation/deployment 
The RMM software comes preinstalled as part of the virtual server provisioning process. After the virtual server  is deployed, you can access RMM through the CLI or GUI. For GUI access, enter the public/reserved IP address of the RMM server. If you have not created public IP address then use private IP address with appropriate VPN connection. Default credential is “admin” and “rackware” is the password. Be sure to change the default password.

**Note:** Setup VPN to access the reserved IP address.

For more information, see the user guide for the RMM server: https://www.rackwareinc.com/rackware-rmm-users-guide-for-ibm-cloud

## License Requirements 
For migration using the RMM server, the license model is “Bring Your Own License” (BYOL). This is a subscription-based license, paid monthly. Each license allows you to migrate one or more servers during the subscription period. Only one server can be migrated at any given time with one license. You will need additional licenses to perform concurrent migrations. To purchase and install licenses, see the “License procurement process” section.

## Ordering Page Deployment Values
This will create a new VPC to install the RMM server.

| Parameter | Description | Value |
| --- | --- | --- |
| ibm_region | IBM Cloud region where the resources to be deployed | MZR (for example, us-south) |
| zone | VPC zone that you wished to deploy the resource in | Zone name (for example, us-south-1) |
| ibmcloud_api_key | IBM Cloud VPC API key needed to deploy IAM enabled resources | API key |
| ssh_key | Public ssh key to login into the resource | Name of an existing SSH key of the region that you wished to login in with |
| resource_group | IBM Cloud resource group | Name of an existing resource group that you want this resource to be placed under |
| vpc_ame | The name of the VPC | Any arbitrary name that complies to IBM VPC naming schema |
| subnet_name | The name of the subnet | Any arbitrary name that complies to IBM subnet naming schema |
| host_name | The name of the VSI | Any arbitrary name that complies to IBM vsi naming schema |
| attach_floating_ip | Create and attach floating IP address to RMM server | Leave default value if you do not want public adress to be created and attached |
| profile | | Leave default value |

## Product configuration 
- Change the default password 
- Create additional user (optional) 
- Update VPC security groups or ACL if needed

## License Procurement Process
To purchase a license, use the following steps. 
1) Contact RackWare at sales@rackwareinc.com to purchase the licenses and specify the number of licenses. 
2) User should receive purchase order from RackWare sales team after licenses are purchased. 
3) Run command 'rwadm relicense' on RMM CLI to generate a preinstall file. 
4) Send an email to licensing@rackwareinc.com with the following information: 
   - RMM License ( Subject line ) 
   - Company Name 
   - License Count 
   - Preinstall File (attached) 
   - Purchase Order (attached) 
5) You will receive the requested licenses. Follow the steps mentioned in the email to apply the licenses and to validate.  Now you are ready to use the RMM server for migration.

## Uninstalling the software 
Complete the following steps to uninstall a Helm chart from your account:
1. Go to the **Menu** > **Schematics**. 
2. Select your workspace name. 
3. Click **Actions** > **Destroy resources**. All resources in your workspace will be deleted. 
4. Click **Update**. 
5. To delete your workspace, click **Actions** > **Delete workspace**.

## Support
For assistance, contact the RackWare support team.

Open any issues directly with the RackWare support team. The support team is available 365x24x7.
Open a case by using the  following options:
- Email : support@rackwareinc.com 
- Phone : +1 (844) 797-8776
In all cases, please add RMM - IBM Cloud in the subject line. The RackWare support is based in United States and India.
