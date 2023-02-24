---
layout: default
title: Pipeline and Deployment Setup
parent: Lab 1 | Configure AES
nav_order: 20
---

# Pipeline and Deployment Setup
{: .no_toc }

[Previous][PREVIOUS]{: .btn .mr-4 }
[Next][NEXT]{: .btn .btn-purple }

**Duration: 30 minutes**
{: .no_toc }

Once App Engine Studio Setup has been completed, administrators must complete the Pipeline and Deployment Guided Setup activities. 

Pipelines enable you to automate the propagation and installation of your applications from one instance to another. Pipelines are powered by the ServiceNow CI / CD spoke, which enables you to automate processes such as publishing applications to the application repository, installing them on target instances, and running ATF tests and/or instance scans. 

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Change current scope to "Deployment Pipeline"

## Configure Prod

### Install the "Deployment Pipeline" plugin
- com.snc.deployment-pipeline
### Configure credentials
### Configure environments
### Configure pipelines
### Add users to "App Engine Admins" group
- Ensure membership is consistent with Dev

## Configure sub-prod instances

### Install the "Deployment Pipeline" plugin
- com.snc.deployment-pipeline
### Configure credentials
### Configure controller instance
### Enable ATF if on Test instance

[Previous][PREVIOUS]{: .btn .mr-4 }
[Next][NEXT]{: .btn .btn-purple }

[PREVIOUS]: ../15_App_Engine_Studio_Setup
[NEXT]: ../30_App_Intake_Setup