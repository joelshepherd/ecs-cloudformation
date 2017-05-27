# joelshepherd/ecs-cloudformation

This repository contains opinionated AWS CloudFormation templates for creating
and managing ECS Clusters.

The templates has been tailored to run as staging and production environments
for small-to-medium size businesses and price points.

## Available templates
- `cluster.yml` Create an autoscaling ECS cluster and load balancer
- (coming soon) `app.yml` Deploy a continuous integration application to a cluster

## Features
- VPC with private and public subnets across two availability zones
- Autoscaling ECS cluster with instances placed in the private subnets
- Persistent EFS storage shared across all ECS instances
- Application Load Balancer in front on the ECS cluster
- Security Groups locking resources down to just those that need them

## Coming soon
- Template to deploy applications to clusters
- Bastion server for SSH access to private resources (ECS instances, EFS, etc.)

Adapted from `awslabs/ecs-refarch-cloudformation` and
`awslabs/ecs-refarch-continuous-deployment`.
