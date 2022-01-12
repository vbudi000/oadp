# Login to OpenShift Cluster Environment

The following information are needed:

- OpenShift Console URL: `https://console-openshift-console.apps.vbudi-001.cp.fyre.ibm.com`
- OpenShift API URL: `https://api.vbudi-001.cp.fyre.ibm.com:6443`
- Login method: `htpasswd`
- OpenShift user: `student`
- OpenShift password: `passw0rd`

Perform the following actions:

1. Open a Web Browser to the OpenShift console URL. Accept the certificate errors for both `console-openshift-console` and `oauth-openshift` URLs. 

2. Login using the login method, click the button representing the method.

3. Enter the user and password for OpenShift.

4. From the console, make sure that both OpenShift Data Foundation and OpenShift API for Data Protection are both installed. Go to **Operators -> Installed Operators**. With the Project showing `All projects` - you should be able to see the OADP Operator and OpenShift Data Foundation there. <br/>
![images/01-01-operators.png](Installed Operators)

    Note that the OADP is installed in the `openshift-adp` namespace and ODF is installed in the `openshift-storage` namespace.

7. Verify all the other required CLIs from your system:

    - oc: see [https://docs.openshift.com/container-platform/4.7/cli_reference/openshift_cli/getting-started-cli.html](https://docs.openshift.com/container-platform/4.7/cli_reference/openshift_cli/getting-started-cli.html)
    - velero: see [https://github.com/vmware-tanzu/velero/releases](https://github.com/vmware-tanzu/velero/releases)
    - git: see [https://git-scm.com/downloads](https://git-scm.com/downloads)

5. Go to yout login drop down on the top right corner select **Copy Login Command**; In the new window, click `Display Token` and copy the `oc login` command with the token. <br/> ![images/01-02-login-token.png](Login token)

6. Open a command line window where you have the `oc` command and paste the login command. 
<br/>![images/01-03-cli-login.png](CLI login)

8. Get the necessary files using GIT:

    ```
    git clone https://github.com/vbudi000/oadp
    cd oadp
    ```



Now you have validated the environment.