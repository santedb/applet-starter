# Business Rules Folder

The `rules/` folder is used to store the JavaScript business rules files which are to be added to the SanteDB iCDR or dCDR. JavaScript business rules allow your plugin to alter the behavior
of the SanteDB persistence layer by changing data before or after it is persisted.

The rules are expressed in JavaScript 5 format:

```
/// <reference path="../.ref/js/santedb-bre.js" />
/// <reference path="../.ref/js/santedb-model.js" />
/// <reference path="../.ref/js/santedb.js" />

// Add a rule 
SanteDBBre.AddBusinessRule(
    "org.santedb.sample",  // Name of the rule
    "TypeTheRuleAppliesTo",  // The type (Patient, Provider, Act, etc.)
    "[Before|After][Insert|Update|Delete]", // The trigger
    { },  // Filter criteria 
    function(data) {
        // To stuff here
        return data; // Always return the modified data
    });

```

For more information see the [SanteSuite Help Wiki](https://help.santesuite.org/developers/applets/business-rules)