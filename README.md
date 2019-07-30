# Forcepoint NGFW AWS High Availability

The run-at-boot script can be used with two or more forcepoint NGFW AWS
instances to implement High Availability.

run-at-boot monitors one or more Route Tables in an AWS VPC to determine when
the primary NGFW goes down. The primary NGFW is the one that is the default
route of the internal subnet in a VPC.

In order to use the run-at-boot script, the NGFW instances need to have an IAM
role attached that gives ec2 instances permission to make AWS API calls. The
policy.json file shows the IAM policy needed to create such a role.

For more information on how to use the scripts, please consult the Forcepoint
Documentation - [How to deploy Forcepoint Next Generation Firewall in the Amazon
Web Services cloud](https://support.forcepoint.com/KBArticle?id=How-to-deploy-Next-Generation-Firewall-in-the-Amazon-Web-Services-cloud)
