# Business Intelligence Folder

The `bi/` folder is used to store the Business Intelligence assets. BI Assets can be:

* BI Queries (`BiQueryDefinition`)
* BI Views (`BiViewDefinition`)
* BI Reports (`BiReportDefinition`)
* BI Parameter Definitions (`BiParameterDefinition`)
* BI Indicator Periods (`BiInidcatorPeriodDefinition`)
* BI Indicators (`BiIndicatorDefinition`)

To ease editing it is recommended to create a link to the BI asset schema on your BI asset definition:

```
<BiIndicatorDefinition xmlns="http://santedb.org/bi" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://santedb.org/bi http://santedb.org/schema/v3.0/BusinessIntelligence.xsd">
    
</BiIndicatorDefinition>
```

For more information see the [SanteSuite Help Wiki](https://help.santesuite.org/developers/applets/business-intelligence-bi-assets/bi-asset-definitions)