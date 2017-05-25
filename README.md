# joelshepherd/ecs-cloudformation

This repository contains opinionated AWS CloudFormation templates for creating
and managing ECS Clusters.

## Available templates
- `cluster.yml` Create an autoscaling ECS cluster and load balancer
- (coming soon) `app.yml` Deploy a continuous integration application to a cluster

## Features
- VPC with private and public subnets across two availability zones
- Autoscaling ECS cluster in the private subnet (triggers not yet setup)
- Persistent EFS storage shared across all ECS instances (automatic mounting not yet setup)
- Application Load Balancer in front on the ECS cluster
- Security Groups locking resources down to just those that need them

## Coming soon
- Template to deploy applications to clusters
- Autoscaling triggers for the ECS cluster
- Automatically mounting EFS storage to ECS instances
- Bastion server for SSH access into the private resources (ECS instances, EFS, etc.)

Adapted from `awslabs/ecs-refarch-cloudformation` and
`awslabs/ecs-refarch-continuous-deployment`.
