secretVault                    |              | Add files in the given vault as a secret to the application. If there is a latest.properties file in the secret it will be sourced as ENV
secretVault/name               |              | Works like setting 'secretValue'
secretVault/keys               |              | Filter the keys in the latest.properties secret on the values in this array.
config/<key>                   |              | Specify config values as strings. Will be env vars in application.
mounts/<name>/type             |              | Specify type of mount. Can either be Secret/ConfigMap/PVC.
mounts/<name>/path             |              | Path in the container where the mount will be mounted
mounts/<name>/secretVault      |              | The secret vault to mount if type is Secret
mounts/<name>/content          |              | The content for the ConfigMap if applicable. Can be specified as JSON
mounts/<name>/exist            |              | Toggle to true to indicate that the secret already exist and should just be mounted


