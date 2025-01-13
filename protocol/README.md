# CDSS Protocols & Libraries

The `protocol/` library is used to store the CDSS libraries that are to be seeded into the SanteDB instance when your applet is loaded. These can be changed after the fact in the [CDSS Library Screen](https://help.santesuite.org/operations/cdr-administration/santedb-administration-panel/cdr-administration/decision-support-library).

CDSS definitions can be in a legacy XML format, such as:

```
<CdssLibrary xmlns="http://santedb.org/cdss" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://santedb.org/cdss http://santedb.org/schema/v3.0/Cdss.xsd"
    name="My CDSS library" id="org.santedb.sample.rule" uuid="56761a56-cd31-11ef-a8e8-7740b3bb8e7f" oid="2.25.2032903290">

    <status>dont-use</status>
    <meta>
        <version>2.0</version>
    </meta>

    <!-- Logic Here -->
</CdssLibrary>
```

Or can be expressed in the CDSS DSL such as:

```
define library "My CDSS Library"
	having id <org.snatedb.sample.rule>
	having uuid {56761a56-cd31-11ef-a8e8-7740b3bb8e7f}
	having oid "2.25.2032903290"
	having status dont-use
	with metadata
		version 2.0
	end metadata
	as
    // Logic Here
end library
```

**Note:** The SanteDB applet host will not replace the CDSS definition in the target SanteDB system unless the version expressed in the file you have provided is higher than the user's defined version. This is to prevent overwriting user's
changes in the SanteDB UI. This file in your applet should be seen as a "seeding" version of the file.

More information about these formats is available on the [SanteSuite Help Wiki](https://help.santesuite.org/developers/applets/cdss-protocols/cdss-definitions).

No further registration in your `manifest.xml` file is required.