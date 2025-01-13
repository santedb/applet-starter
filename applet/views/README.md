# AngularJS Views Folder

The view folder is where the HTML files are contained which represent the views in the SanteDB instance. Views are `XHTML` files which have additional routing information added to them:

```
<div xmlns="http://www.w3.org/1999/xhtml" xmlns:sdb="http://santedb.org/applet">
    <!-- The SDB:STYLE element allows the injection of CSS into the HTML headers by the server -->
    <sdb:style static="false">~/css/theme.css</sdb:style>
    <!-- The SDB:SCRIPT element allows the injection of JavaScript via lazy loading (or static loading if static = true) -->
    <sdb:script static="false">~/controllers/index.js</sdb:script>
    <!-- SDB:STATE Defines an AngularJS state for the SPA -->
    <sdb:state name="santedb-sample">
        <!-- One or more demands which the user must have to view this asset -->
        <sdb:demand>1.3.6.1.4.1.33349.3.1.5.9.2.1</sdb:demand>
        <!-- The URL of the asset relative to its parents -->
        <sdb:url>/</sdb:url>
        <!-- Control the view / layout -->
        <sdb:view>
            <!-- The name of the AngularJS controller this file uses -->
            <sdb:controller>SampleLayoutController</sdb:controller>
            <!-- The title of this page which appears in the breadcrumb list -->
            <sdb:title lang="en">SanteDB Sample Application</sdb:title>
        </sdb:view>
    </sdb:state>
</div>
```

For more information see the [SanteSuite Help Wiki](https://help.santesuite.org/developers/applets/assets/html-assets)