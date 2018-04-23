*affiliation*                  |              | Used to group the project for resource monitoring. All projects start with affiliation. lower case letters max length 10. Required.
envName                        | $folderName  | Change the name of the project. Note that the default value here is the actual name of the folder where the app file is. This option must be specified in either global or env file.
env/name                       |              | An alias for envName
env/ttl                        |              | Set a time duration in format 1d, 12h aso that indicate how long until this namespace should be deleted
*permissions/admin*            |              | The groups in OpenShift that will have the admin role for the given project. Can either be an array or a space delimitered string. This option must be specified in either global or env file. Required.
permissions/view               |              | The groups in OpenShift that will have the view role for the given project. Can either be an array or a space delimitered string. This option must be specified in either global or env file.
permissions/adminServiceAccount|              | The serviceaccounts in OpenShift that will have the admin role for the given project. Can either be an array or a space delimitered string. This option must be specified in either global or env file.
