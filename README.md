# OpenShift API for Data Protection 


This repository contains the steps needed to demonstrate backup and restore using Velero on an OpenShift cluster. See [velero-lab](velero-lab.md)

## Prerequisites:

- OpenShift Cluster 
- OpenShift Data Foundation 
- OpenShift API for Data Protection

## Setup 

Files from this repo:

- htpasswd.file: users and passwords for lab users
- studentrole.yaml: necessary role and access for students for this lab

1. Setup an OCP environment on Fyre

2. Setup ODF: https://github.ibm.com/vbudi/ocs-on-fyre/blob/master/odf-on-fyre.sh

3. Setup OADP: https://github.ibm.com/vbudi/ocs-on-fyre/blob/master/oadp-on-fyre.sh

4. Setup users

    - setup htpasswd authentication for students
    - prepare student roles for accessing non-standard backup resources
    - connect to system:cluster-admin group for noobaa

    ```
    oc create secret generic htpasswd -n openshift-config --from-file htpasswd=htpasswd.file --dry-run -o yaml | oc replace -f -

    oc create -f studentrole.yaml
    ```

5. Delete the default kubeadmin:

    ```
    oc delete secret kubeadmin -n kube-system
    ```

## Other information

sampleApp.drawio: diagram of the sample application
nginx-deployment.yaml: YAML file to deploy sample application