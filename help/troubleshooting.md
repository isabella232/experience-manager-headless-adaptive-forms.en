---
title: Headless Adaptive Forms architecture
description: Headless Adaptive Forms architecture
keywords: headless, adaptive form, architecture
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

1. Completely [remove present installtions of Node.JS](https://khushwantsehgal.wordpress.com/2022/06/28/how-to-remove-node-js-completely-from-windows-10/) from your environment.

1. Install the supported version of [Node.JS and NPM](setup-development-environment.md).

1. Reboot your machine.
