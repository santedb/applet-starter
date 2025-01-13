# Seeding Dataset

The contents of the `Data/` directory of your applet starter are used to store dataset files which seed data into your SanteDB iCDR instance. These are stored separately from the `applet/` directory where the applet code is stored as we want to reduce the amount of information flowing in an applet for the update process, and some datasets can be quite large.

To start, place `.dataset` files in to this directory and reference them from your SanteDB configuration. A dataset file has format:

```
<dataset 
    xmlns="http://santedb.org/data"
    id="My Project's Custom Data Seeding"
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xsi:schemaLocation="http://santedb.org/data http://santedb.org/schema/v3.0/Dataset.xsd" >
</dataset>
```

You can reference this directory by updating your `santedb.config.xml` file to point to it, notably `FileSystemDatasetProviderConfigurationSection`:

```
<section xsi:type="FileSystemDatasetProviderConfigurationSection">
    <sources>
      <add>data</add>
      <add>{path-to-this-directory}</add>
    </sources>
</section>
```

For more information see the [SanteDB Help Wiki](https://help.santesuite.org/developers/applets/distributing-data).