# OpenShift API for Data Protection 


This repository contains the steps needed to demonstrate backup and restore using Velero on an OpenShift cluster.

## Prerequisites:

- OpenShift Data Foundation 
- OpenShift API for Data Protection

## Overview

The lab flow is as follows:

1. Launch OpenShift console and check CLIs - [01-login.md](01-login.md) 

2. Deploy a sample application with Physical volume on its own namespace. Perform modification on disk. - [02-sampleapp.md](02-sampleapp.md)

3. Run backup. - [03-backup.md](03-backup.md)

4. Restore and verify - [04-restore.md](04-restore.md)


