---
title: Headless Adaptive Forms Troubleshooting
description: Headless Adaptive Forms Troubleshooting
keywords: headless, adaptive form, Troubleshooting
hide: yes
exl-id: bfb7e688-d2be-4aaa-ac9b-147cbd74b516
---
# Troubleshooting 

## Unable to deploy the Archetype project on local development environment 

### Issue

When you use the `mvn -PautoInstallPackage clean install` or similar commands to deploy an AEM Archeype project, the project fails to deploy.

### Reason 

It can happen due to an unsupported version or corrupt installtion of node.js or NPM.

### Solution

1.  Completely [remove present installations of Node.JS](https://khushwantsehgal.wordpress.com/2022/06/28/how-to-remove-node-js-completely-from-windows-10/) from your environment.

1.  Install Node.JS 16.13.0 or later with NPM.

1.  Reboot your machine.


## The `mvn clean install` command fails to run

### Issue

When you use the `mvn clean install` or similar commands to deploy an AEM Archeype project, the command fails to run.

### Reason

It can happen if Git is not installed.

### Solution

Download and install the [latest release of Git](https://git-scm.com/downloads). If you are new to Git, see [Installing Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git).
