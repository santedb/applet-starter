# Alien Folder
The `alien` folder is used to define the foreign data format importers that your project will use. The structure of this file is contained in `ForeignDataMap.xsd`, which can be referenced in the `xsi:schemaLocation` attribute as:

```
<ForeignDataMap xmlns="http://santedb.org/import" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://santedb.org/import http://santedb.org/schema/v3.0/SanteDBForeignData.xsd" 
    priority="0">
    
</ForeignDataMap>
```

You can use the `@priority` attribute to override an existing foreign data map that is registered in the underlying plugins of SanteDB.

No further modifications to your `manifest.xml` file is required.

For more information see [SanteSuite Help Wiki](https://help.santesuite.org/developers/applets/external-data-maps)