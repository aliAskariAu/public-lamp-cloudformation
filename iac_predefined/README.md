# CloudFormation Pre-Defined Template for LAMP Stack.

This README explains the "LAMP_Single_instance_template.yml" for a sample CloudFormation deployment with Infrastructure as Code (IaC) to showcase a simple solution in AWS.

## Components

The main components are:

- Parameters: are the way to choose the customizations of the solution. For example "KeyName", "DBName", "DBUser", "DBPassword", "DBRootPassword", "InstanceType", "SSHLocation". These configure the database, the EC2 instance and the access IP ranges.
- EC2 instance: is the main Linux server for the LAMP deployment. It allows to select the instance type from an input parameter (enabling the user to choose a "big" or "small" server configuration).
- Security Group: is the firewall that protects the server and the origin source CIDR range can be selected to enable different IP addresses to communicate with the solution.
- Outputs: allow to see the final website URL, so that it's easily accessible from the user's perspective.

## Deployment

To deploy the solution, please go to the "AWS Console", then search for "CloudFormation" and select "Create Stack". Then, follow the steps and replace the input variables with the desired ones.

## Deletion

To destroy the solution, please go to the "AWS Console", then search for "CloudFormation" and select the name of the stack to delete (depends on the name applied to it). Then click on "Delete" and follow the steps.

## Author

Ali Askari.
Junior DevOps Engineer (main tool is PHP).
