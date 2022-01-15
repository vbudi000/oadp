# Setting up lab environment in Fyre lab

1. Setup an OCP environment on Fyre

    - setup htpasswd authentication for students
    - prepare student roles for accessing non-standard backup resources
    - connect to system:cluster-admin group for noobaa

2. Setup ODF: https://github.ibm.com/vbudi/ocs-on-fyre/blob/master/odf-on-fyre.sh


3. Setup OADP: https://github.ibm.com/vbudi/ocs-on-fyre/blob/master/oadp-on-fyre.sh


4. 

odf-on-fyre.sh 

Setup users

oc create secret generic htpasswd -n openshift-config --from-file htpasswd=htpasswd.file --dry-run -o yaml | oc replace -f -

user 
