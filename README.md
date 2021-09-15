## Product Overview
RackWare's RMM Migrations are an automated, easy and convenient process to move existing workloads
between systems such as bare metal to bare metal, creating an exact duplicate of a running image
without the burden of rebuilding or recreating template images and applications. Migrating large
complex environments through a simple interface and automated tasks reduces the time required from
weeks to days.


RackWare’s RMM software platform delivers a suite of intuitive and automated services that provide
IT resiliency and simplified migration to the cloud, while reducing capital and operating expenses.
RMM decouples the application stack from the underlying platform allowing it to be ported to the IBM
Cloud infrastructure. RackWare RMM includes discovery, analysis and automation features allowing all
processes to be fast, easy and error-free.

Key Benefits
- Live Migrations
- Highly secure and efficient data transfer.
- Include / Exclude Lists: Capture and sync only specific files and directories rather than entire
systems.
- Delta Sync: Sync only the changed parts of files during the final data sync, drastically lowering
cutover times.
- Network optimization: bandwidth usage limitations, compression and check point restart for all
sync operations

For more information, visit https://www.rackwareinc.com/cloud-migration

## Supported Migration
- Classic bare metal to classic bare metal
## Before you begin software installation
 Make sure you have the following:
- Proper IBM Cloud account permissions and access
- Identify a region and zone on where you will want to  deploy the RMM server
- The region should be under IBM Cloud account quota for VPC, security groups, and floating IP
- Know more about IBM VPC, visit https://cloud.ibm.com/docs/vpc?topic=vpc-getting-started 

## Software Installation/Deployment
The RMM software will come pre-installed as part of the VSI provisioning.  Once VSI is deployed, you
can access RMM through the CLI or GUI.  For GUI access, enter the public IP address of the RMM
server.  Default credential is admin and rackware for password.  Be sure to change the default
password.

Link to the user guide for RMM server, https://www.rackwareinc.com/rackware-rmm-users-guide-for-ibm-cloud

# License Requirements
For migration using the RMM server, the license model is bring your own license (BYOL). The license is a subscription based license, paid monthly.  Each license allows you to migrate one or more servers during the subscription period. Only one server can be migrated at any given time with one license. You will need additional licenses to perform concurrent migrations.  To purchase and install licenses please refer to the section : License Procurement Process


### Ordering Page Deployment Values
This will create a new VPC to install the RMM server.

| Parameter | Description | Value |
| --- | --- | --- |
| TF_Version | terraform engine version to be used in schematics | Leave default value |
| ibm_region | IBM Cloud region where the resources to be deployed | MZR (i.e, us-south) |
| ibmcloud_api_key | IBM Cloud VPC API key needed to deploy IAM enabled resources | API key |
| image_url |  | Leave default value |
| name | The name of the VPC | Any arbitrary name that complies to IBM VPC naming schema |
| profile | | Leave default value |
|resource_group | IBM Cloud resource group | Name of an existing resource group that you want this resource to be placed under |
| ssh_key | Public ssh key to login into the resource | Name of an existing SSH key of the region that you wished to login in with |
| zone | VPC zone that you wished to deploy the resource in | Zone name (ie., us-south-1) |

### Production configuration
- Change the default password
- Create additional user (optional)
- Update VPC security groups or ACL if needed

### License Procurement Process

To purchase license, follow the below steps. 
1)	Contact RackWare at sales@rackwareinc.com to purchase
the licenses and specify the number of licenses. 
2)	User should receive purchase order from RackWare sales team after license are purchased. 
3)	Run command 'rwadm relicense' on RMM CLI to generate preinstall file.
4)	Please send an email to licensing@rackwareinc.com with following information.
- RackWare RMM License ( Subject line )
- CompanyName
- LicenseCount
- PreinstallFile (attached)
- PurchaseOrder (attached)
5) You will receive the requested licenses. Please follow the steps mentioned in the email to apply the licenses and validate.
Now you are ready to use the RMM server for migration. 

## Uninstalling the software
Complete the following steps to uninstall a Helm chart from your account. 

1. Go to the **Menu** > **Schematics**.
2. Select your workspace name. 
3. Click **Actions** > **Destroy resources**. All resources in your workspace are deleted.
4. Click **Update**.
5. To delete your workspace, click **Actions** > **Delete workspace**.


## Getting Support
### Getting support through RackWare support team
Please open any issues directly with RackWare support team. The support team is available 365x24x7.

Please open a case via following options:
- Email : support@rackwareinc.com
- Phone : +1 (844) 797-8776

In all cases, please add RackWare RMM - IBM Cloud in the subject line. The RackWare support is based in United States and India.
