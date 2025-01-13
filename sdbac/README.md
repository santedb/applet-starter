# SanteDB Admin Console Initialization Scripts

This directory is typically used to store SanteDB administrative console scripts for your project. These scripts are used to:

* Create any special groups or roles
* Assign or alter permissions for roles
* Create any special users, applications or devices for your solution

The files should be stored with a `.sdbac` extension (example:`users.sdbac`) and helps other developers seed their instances of SanteDB. The contents are simple sdbac commands, for example:

```
user.add -u demouser -r CLINICAL_STAFF -e "demouser@example.com" -p "@ChangeMe2024"
profile.edit -u demouser --name="Mr. Demo User" --tel="905-515-5049 ext=3029" --lang=en
facility.staff.add -u demouser -f "Demoland Community Hospital"
```

Users may run these scripts using the `sdbac` tool:

```
sdbac users.sdbac -r dev.example.com --tls --port=8443
```
