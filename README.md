# OpenShift API for Data Protection 


This repository contains the steps needed to demonstrate backup and restore using Velero on an OpenShift cluster.

## Prerequisites:

- OpenShift Data Foundation 
- OpenShift API for Data Protection

## Overview

The lab flow is as follows:

1. Launch OpenShift console and CLI 

2. Deploy a sample application with Physical volume on its own namespace. Perform modification on disk.

3. Run backup.

4. Delete storage

5. Restore and verify

6. Delete namespace (storage and resources)

7. Restore and verify


