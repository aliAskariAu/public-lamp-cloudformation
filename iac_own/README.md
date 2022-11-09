# CloudFormation Template for Gorgeous Cupcake solution.

This README explains the "LAMP_Own_template_storage.yml" and ""LAMP_Own_template_compute.yml" CloudFormation deployments with Infrastructure as Code (IaC) to showcase a real example of a solution in AWS.

## Components

The main parameters for the storage stack are:

- AppName: name of the application.
- DBName: name of the database.
- DBPassword: password of the database.
- InstanceType: instance type for the database.

The main parameters for the compute stack are:

- AppName: name of the application.
- DBName: name of the database.
- DBHost: host of the database (from the storage stack).
- DBUser: user of the database (from the storage stack configs).
- DBPassword: password of the database.
- InstanceType: instance type for the EC2 server.
- InstanceAMI: instance image for the EC2 server.
- KeyName: SSH KeyName (must be created before deployment in AWS account).
- SSHLocation: CIDR to access the server.

## Deployment

To deploy the solution, please go to the "AWS Console", then search for "CloudFormation" and select "Create Stack". Then, follow the steps and replace the input variables with the desired ones.

The order for the deployment is:

- First, deploy the storage stack.
- Second, execute SQL commands in the database.
- Third, deploy the compute stack.

## Deletion

To destroy the solution, please go to the "AWS Console", then search for "CloudFormation" and select the name of the stack to delete (depends on the name applied to it). Then click on "Delete" and follow the steps.

- First, destroy the compute stack.
- Second, destroy the storage stack.

## Author

Ali Askari.
Junior DevOps Engineer (main tool is PHP).
