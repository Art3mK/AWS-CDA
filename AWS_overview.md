# AWS global infra

- 16 Regions
- 44 AZs
- +6 regions +17 more AZs for 2018
- не тестируют сколько регионов и зон.
- **Регион** включает 2 и более AZs
    * AZ is DC

Edge locations
  - Для кеширования ресурсов (Cloudforint CDN)
  - 96 edge locations
  - Helsinki, Stockholm, Munich

Regional Edge caches
  - Frankfurt
  - London

Regional Edge Caches, in addition to improving performance, also help reduce the load on your origin resources, minimizing operational burden associated with scaling your origin and reducing your origin costs. Regional Edge Caches are turned on by default for your CloudFront distributions; you do not need to make any changes to your distributions to take advantage of this feature. There are also no additional charges to use this feature.
These locations sit between your origin webserver and the 68 global edge locations that serve traffic directly to your viewers
Regional Edge Caches have larger cache-width than any individual edge location, so your objects remain in cache longer at these locations
For instance, our edge locations in Europe now go to the regional edge cache in Frankfurt to fetch an object before going back to your origin webserver.

#Compute

# EC2

Elasctic Compute Cloud

# ECS

EC2 Container Service

# Elastic Beanstalk

Blackbox for developers

# Lambda

# Lightsail

Blackbox for provisioning servers

# Batch

Batch computing

# Storage

# S3

Simple Storage Service, object based storage

# EFS

Elastic File System, NAS, NFS volumes

# Glacier

Data archival

# Snowball

Data transfer, DC -> Amazon DC on physical device

33 Storage Gateway

VM on local DC, replicate data to S3

# Databases

## RDS

MySQL, PostgreSQL, Microsoft SQL, Aurora, Oracle

## DynamoDB

noSQL DB

## ElasticCache

Redis, memcached

## Redshift

Data warehouse, Business intelligence

# Migration

## AWS Migration Hub

tracking service

## Application Discovery Service

Track dependencies for apps

## Database migration service

on-site DB -> RDS

## Server migration service

on-site VM -> EC2

## Snowball

Data transfer, DC -> Amazon DC on physical device

# Networking and content delivery

## VPC

Virtual Private Cloud

## Cloudfront

Amazon CDN (content delivery network)

## Route53

Amazon DNS service

## API gateway

way of creating APIs for other services

## Direct connect

Way of running dedicated line between local DC and Amazon DC

# Developer tools

## CodeStar

way of getting group of devs to collaborate, project managing

## CodeCommit

place to store code, SCM, git repos

## CodeBuild

pipeline for building code

## CodeDeploy

automates code deployment to EC2/on-premises/lambda

## CodePipeline

CD service, visualise, automate steps to release software

## X-Ray

Debugging/Analyzing, request traces, route cause of issues

## Cloud9

IDE in cloud

# 10,000 foot overview part 3

# Management tools

## Cloudwatch

Monitoring, alerts

## CloudFormation

IAC

## Cloudtrail

Collecting logs about actions for API calls

## Config

Monitors config on entire AWS env. PIT snapshots for env

## OpsWorks

Elastic Beanstalk like, Chef/Puppet, automating environment

## Service Catalog

Catalog of IT services, VMs, OSes, DBs, etc. Service catalog

## Systems manager

EC2, for patching. Resource grouping

## Trusted Advisor

Шняга, которая показывает всякие полезные штуки, что можно улучшить, открытые группы, как сэкономить денег и т.д.

## Managed services

Manage cloud for you

# Media Services

## Elastic Transcoder

For example converts videos for different devices

## Media(Convert|Live|Package|Store|Tailor)

# Machine learning

## SageMaker

Deep learning for devs (neural networks)

## Comprehend

Some analysis?

## DeepLens

AI camera, recognizes objects (with no backend required)

## Lex

Way of communicating with customers (AI, machine learning)

## Machine Learning

Dataset -> analyze -> results

## Polly

text to speech service

## Rekognition

Images/Video -> tells what happens in files

## Amazon Translate

Machine translation service

## Amazon Transcribe

распознование речи

# Analytics

## Athena

SQL queries on S3 buckets, serverless

## Elastic Map Reduce (EMR)

processing large amounts of data

## CloudSearch

## ElasticSearch

## Kinesis

Ingesting large amounts of data into AWS

## Kinesis Video Streams

## QuickSight

BI tool

## Data pipeline

moving data between services

## Glue

data ETL service
