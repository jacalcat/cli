---



copyright:

  years: 2015, 2017

lastupdated: "2017-05-15"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}

# Downloads
{: #cli}

With {{site.data.keyword.Bluemix_short}}, you have access to powerful tools such as a unified command line interface and CLI plug-ins. Each of these CLI downloads are all available to support your {{site.data.keyword.Bluemix_notm}} experience.
{:shortdesc}

There are two ways to get started with the Bluemix CLIs and plugins. On macOS, the easiest way to get started is by installing IBM Cloud Application Tools. Alternatively, you can follow the instructions and documentation below to install the CLIs and plugins manually.

## IBM Cloud Application Tools
{: #icat}

IBM Cloud Application Tools 2.0 is a menubar application streamlined for local environment setup and management. Users can easily install and update {{site.data.keyword.Bluemix_notm}} tools and CLIs, change CLI deployment targets, and quickly access common {{site.data.keyword.Bluemix_notm}} links.

(Internal IBM release only)

[Download IBM Cloud Application Tools 2.0 for macOS ![External link icon](../icons/launch-glyph.svg)](http://ibm.biz/icat-2-download ){: new_window} <br>
[Please Provide Feedback ![External link icon](../icons/launch-glyph.svg)](http://ibm.biz/icat-2-feedback){: new_window}

## ![](./images/CLI.svg) Manual command line interface installation
{: #downloads notoc}

Download and install the command line tool to support your {{site.data.keyword.Bluemix_notm}} experience.

{{site.data.keyword.Bluemix_notm}} CLI provides a command line experience to manage your {{site.data.keyword.Bluemix_notm}} environment. It also includes a Cloud Foundry command line interface, cf, in its installation, for managing Cloud Foundry applications and services. 

Both CLI tools use 443 port by default. If you have HTTP proxy between the CLI tools and {{site.data.keyword.Bluemix_notm}} environment, you must configure the `HTTP_PROXY` environment variable with the actual HTTP proxy url and port if there is any. See [Using the CLI with an HTTP Proxy Server ![External link icon](../icons/launch-glyph.svg)](http://docs.cloudfoundry.org/cf-cli/http-proxy.html){: new_window} for more details.

[Download {{site.data.keyword.Bluemix_notm}} CLI ![External link icon](../icons/launch-glyph.svg)](http://clis.stage1.ng.bluemix.net/){: new_window} <br> 
[View Docs](/docs/cli/reference/bluemix_cli/index.html)

## ![](./images/CLI_Plugin.svg) Command line interface plug-ins
{: #cliplugins notoc}

Easily extend your {{site.data.keyword.Bluemix_notm}} command line interface with more commands. To access the {{site.data.keyword.Bluemix_notm}} command line interface plug-ins, see the [CLI Plug-in Repository ![External link icon](../icons/launch-glyph.svg)](https://plugins.stage1.ng.bluemix.net/){: new_window}.

### Extend your {{site.data.keyword.Bluemix_notm}} command line interface: bx
{: #cli_bluemix_ext notoc}


After you install the {{site.data.keyword.Bluemix_notm}} cli tool, the [CLI Plug-in Repository ![External link icon](../icons/launch-glyph.svg)](https://plugins.ng.bluemix.net/){: new_window} is pre-configured with a repository alias `Bluemix` by default. You can install available plug-ins directly.

```
bluemix plugin install plugin_name -r Bluemix
```

<!-- Do not move full table into production because Catalog Manager is staging only -->

| *{{site.data.keyword.autoscaling}} CLI* | *Catalog Manager* | *IBM Bluemix Container Service*  |
|-----|-----|-----|
| Plug-in name: auto-scaling <br> [View Docs](/docs/cli/plugins/auto-scaling/index.html) | Plug-in name: catalog-manager  <br> [View Docs](/docs/cli/plugins/catalogmanager/index.html) | Plug-in name: container-service  <br> [View Docs](/docs/containers/cs_cli_devtools.html) |
{: caption="Table 2. Plug-ins" caption-side="top"}

|  *Private network peering* | *Schematics* | *VPN*  |
|-----|-----|-----|
| Plug-in name: private-network-peering  <br> [View Docs](/docs/cli/plugins/pnp/index.html) | Plug-in name: Schematics  <br> [View Docs](/docs/services/schematics/schematics_reference.html) | Plug-in name: VPN  <br> [View Docs](/docs/cli/plugins/bx_vpn/index.html) |
{: caption="Table 3. Plug-ins" caption-side="top"}

You can also add plug-ins from other repositories that complies with the {{site.data.keyword.Bluemix_notm}} cli architecture.
1. To install {{site.data.keyword.Bluemix_notm}} CLI plug-ins from another repository, set the plug-in registry endpoint:
```
bluemix plugin repo-add bluemix-other-repo [repo_url]
```
where `repo_url` is the https url of the plugin repository.

2. Run the following command to install a plug-in:
```
bluemix plugin install plugin_name -r bluemix-other-repo
```


### Extend Cloud Foundry command line interface: bx cf
{: #cli_cf_ext notoc}

After you install the {{site.data.keyword.Bluemix_notm}} command line tool, a Cloud Foundry command line interface is also installed inside the Bluemix CLI directory. Run the Cloud Foundry CLI commands using `bluemix cf`.

* To install cf CLI plug-ins from the {{site.data.keyword.Bluemix_notm}} registry, set the plug-in registry endpoint:

```
bluemix cf add-plugin-repo bluemix-cf-repo https://plugins.ng.bluemix.net
```
{: codeblock}

* Then, run the following command to install a plug-in:

```
bluemix cf install-plugin plugin_name -r bluemix-cf-repo
```
{: codeblock}

| *Admin Console* |
-----------------|
|  Plug-in name: bluemix-admin <br> [View Docs](/docs/cli/plugins/bluemix_admin/index.html) |
{: caption="Table 4. Plug-ins" caption-side="top"}

| *{{site.data.keyword.IBM}} Containers for {{site.data.keyword.Bluemix_notm}}* | *VPN* |
|-----------------|-----------------|
| Plug-in name: ibm-containers <br> [View Docs ![External link icon](../icons/launch-glyph.svg)](https://www.{DomainName}/docs/containers/container_cli_cfic.html#container_cli_cfic){: new_window} | Plug-in name: VPN <br> [View Docs](/docs/cli/plugins/vpn/index.html) |
{: caption="Table 5. Plug-ins" caption-side="top"}

## ![](./images/Integrated_Dev_Tools.svg) Integrated development tools
{: #ide notoc}

Download and install plug-ins to integrate your favorite {{site.data.keyword.Bluemix_notm}} services.

| *Liberty for Java* | *MobileFirst* | *{{site.data.keyword.rules_short}}* | *API Connect* | *Eclipse Tools for Bluemix* |
|----------|----------|----------|----------|----------|
| [Liberty Eclipse Plug-in ![External link icon](../icons/launch-glyph.svg)](https://developer.ibm.com/wasdev/downloads/liberty-profile-using-eclipse/){: new_window} | [Eclipse Plug-in ![External link icon](../icons/launch-glyph.svg)](https://marketplace.eclipse.org/content/ibm-mobilefirst-platform-studio){: new_window} | [Rules Designer Eclipse Plug-in](../services/rules/index.html#rulov002) | [Developer Toolkit](/docs/services/apiconnect/apic_003.html#apic_001 ) | [Bluemix Eclipse Plug-in](/docs/manageapps/eclipsetools/eclipsetools.html) |
{: caption="Table 6. Plug-ins" caption-side="top"}