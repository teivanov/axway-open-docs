{
"title": "Install Policy Studio",
"linkTitle": "Install Policy Studio",
"weight":"16",
"date": "2019-10-02",
"description": "Policy Studio is a graphical IDE that allows you to virtualize APIs and develop policies."
}

You can install Policy Studio on both Linux and Windows.

{{< alert title="Note" color="primary" >}}Windows is supported only for a limited set of developer tools, see [Install developer tools on Windows](/docs/apigtw_install/install_dev_tools). API Gateway and API Manager do not support Windows.{{< /alert >}}

## Prerequisites

Ensure that all of the prerequisites detailed in [Prerequisites](/docs/apigtw_install/system_requirements) are met.

## Install Policy Studio

To install Policy Studio in GUI mode, perform an installation following the steps described in [Installation options](/docs/apigtw_install/installation#select-setup-type), using the following selections:

* Select the **Custom** setup type. This screen is omitted on Windows.
* Select to install the Policy Studio component.

To install Policy Studio in unattended mode, follow the steps described in [Unattended installation](/docs/apigtw_install/installation_unattended).

The following example shows how to install the Policy Studio component in unattended mode on Linux:

```
./APIGateway_7.8_Install_linux-x86-32-BN<n>.run --mode unattended --setup_type advanced  
--enable-components policystudio --disable-components nodemanager,apigateway,qstart,apitester,analytics,configurationstudio,apimgmt,cassandra,packagedeploytools
```

## Start Policy Studio

{{< alert title="Note" color="primary" >}}Before starting Policy Studio, ensure both the Admin Node Manager and the API Gateway instance are running. For more details, see [Start API Gateway](/docs/apigtw_install/install_gateway#start-api-gateway).{{< /alert >}}

If you did not select to launch Policy Studio after installation, perform the following steps:

1. Open a command prompt.
2. Change to your Policy Studio installation directory (for example, `INSTALL_DIR/policystudio`).
3. Run `policystudio`.
4. When Policy Studio starts up, select **File > New Project**.
5. In the New Project dialog, enter a name for the project and click **Next**.
6. Select **From a running API Gateway instance** and click **Next**.
7. In the Open Connection dialog, select the Admin Node Manager session to connect to, enter the administrator user name and password you specified when you installed API Gateway, and click **OK**.
8. In the Download Options dialog, select a group and an API Gateway instance to download its configuration.
9. If a passphrase has been set, enter it in the **Passphrase** field, and click **Finish**. Alternatively, if no passphrase has been set, click **Finish**.

{{< alert title="Tip" color="primary" >}}You can also create configuration projects from `.fed` files or from existing configurations. For more information, see the
[API Gateway Policy Developer Guide](/bundle/APIGateway_77_PolicyDevGuide_allOS_en_HTML5/).{{< /alert >}}
