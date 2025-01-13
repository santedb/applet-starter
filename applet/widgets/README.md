# AngularJS Widgets Folder

The widgets folder is used to define custom widgets which are used for extending parts of pages which provide extension endpoints for (for example: adding a tab to an existing screen, adding a panel to an existing tab, etc.).

```
<div xmlns="http://www.w3.org/1999/xhtml" 
  xmlns:sdb="http://santedb.org/applet"
>
  <sdb:widget name="org.example.widget" type="Tab" order="10" context="org.santedb.configuration">
    <sdb:demand>1.3.6.1</sdb:demand>
    <sdb:icon>fas fa-cog</sdb:icon>
    <sdb:guard>!scopedObject.tag</sdb:guard>
    <sdb:description lang="en">Example Widget</sdb:description>
    <sdb:views>
        <sdb:view type="Edit">
            <sdb:demand>POLICY_OID</sdb:demand>
            <sdb:guard>JavaScript Guard</sdb:guard>
        </sdb:view>
    </sdb:views>
  </sdb:widget>
  <!-- Content Here -->
</div>
```

For more information see the [SanteSuite Help Wiki](https://help.santesuite.org/developers/applets/assets/html-assets)