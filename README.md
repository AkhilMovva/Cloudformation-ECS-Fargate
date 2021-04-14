# Cloud Formation Templates for Deploying Fargate Tasks in a VPC on a Public Subnet.

## I have built the below architecture using CloudFormation Templates
![11-ecs-cfn-public-vpc-public-subnet](https://user-images.githubusercontent.com/23433121/114659950-77a7b480-9cc2-11eb-81c8-e64ee6738ef0.png)

## Step-00: Template Categories
### I'm going to divide templates in to two categories
- Network Stack (Parent Stack)
- Create VPC
-- Create ECS Cluster & ECS Roles
-- Create Load Balancer (ALB)
-- Create Outputs
- Faragte Service Stack
-- Create Input Parameters
-- Create Task Definition
-- Create Load Balancer Target Group & Load Balancer Rule
-- Create ECS Service

## Step-01: Create Network Stack (Parent Stack)
### I'm going to build the network stack in a incremental manner.
- CreateVPC
- ECSCluster-ECSRoles
- SecurityGroups-LoadBalancers
- Export Outputs

## Step-02: Create Fargate Service Stack
### I'm going to build the network stack in a incremental manner.
- InputParameters
- TaskDefinition
- ALB-TargetGroup-and-LoadBalancerRule
- FECSService

## Step-03: Clean-Up
- Delete CloudFormation Stacks
- First delete Service Stack
- Next delete the Network Stack ( Network stack resources are used in Service Stack - Always recommended to delete parent stacks at the end.)
