*schemaVersion*                   |              | All files in a given AuroraConfig must share a schemaVersion. For now only v1 is supported, it is here incase we need to break compatability. Required.
*type*                            |              | What type of flow does this application follow. Options here are [deploy, development, template, localTemplate]
applicationPlatform               | java         | Specify application platform. java or web are valid plattforms. Is only used if type is deploy/development.
name                              | $fileName    | The name of the application. All objects created in the cluster will get an app label with this name. Cannot be longer then 40 (alphanumeric -). Note that the default value here is the actual name of the app file.
*cluster*                         |              | What cluster should the application be deployed to. Must be a valid cluster name.
ttl                               |              | Set a time duration in format 1d, 12h aso that indicate how long until this application should be deleted
*version*                         |              | Version of the application to run. Can be set to any of the valid version strategies. TODO: Link to them |
