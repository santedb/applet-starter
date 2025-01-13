# SanteDB Applet Starter Code

This repository contains a skeleton for a start applet project.

To get started, clone this project to a directory on your development machine and install the [SanteDB Software Development Kit](https://github.com/santedb/santedb-sdk/releases) and one of the SanteDB iCDR services (SanteDB, SanteMPI, etc.). 

Configure your SanteDB iCDR as described in [Getting Started](https://help.santesuite.org/developers/getting-started) and run your SanteDB SDK applet debugging environment against that instance with:

```
sdb-ade --ref="C:\Program Files\SanteSuite\SanteDB\SDK\santedb.admin.sln.pak" --applet=path_to_this_repo\applet
```