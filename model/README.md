# View Model Definitions

The `model/` folder is used to store your view model definitions. View model definitions are used to instruct the HDSI or AMI which properties are to be loaded from the database before returning the information from the API.

These are applied when the `Accept` header is passed as `application/x.santedb.viewModel+json`. To ease editing reference the ViewModel.xsd file from the SanteDB community server:

```
<ViewModel xmlns="http://santedb.org/model/view" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
  xsi:schemaLocation="http://santedb.org/model/view http://santedb.org/schema/v3.0/ViewModelDescription.xsd">
    <include>base</include>
</ViewModel>
```

You will also need to register your view model in the `manifest.xml` to give it a friendly name mapping to the `X-SanteDB-ViewModel: xxxxx` header passed on API requests:

```
  <viewModel key="myViewName">
    <definition>/org.santedb.sample/model/myViewFile.xml</definition>
  </viewModel>
```