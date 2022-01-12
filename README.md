# OpenShift API for Data Protection 


This repository contains the steps needed to demonstrate backup and restore using Velero on an OpenShift cluster.

## Prerequisites:

- OpenShift Data Foundation 
- OpenShift API for Data Protection

## Overview

The lab flow is as follows:

1. Launch OpenShift console and check CLIs - [01-login](01-login) 

2. Deploy a sample application with Physical volume on its own namespace. Perform modification on disk. - [02-sampleapp](02-sampleapp)

3. Run backup. - [03-backup](03-backup)

4. Restore and verify - [04-restore](04-restore)


