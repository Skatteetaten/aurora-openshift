webseal | false | Toggle to expose application through WebSeal.
webseal/host | $name-$affiliation-$envName | Set this to change the default prefix in WebSeal
webseal/roles | | Set roles required to access this route. This can either be set as CSV or as an array of strings
certificate | false | Toggle to add a certificate with CommonName $groupId.$artifactId.
certificate/commonName | | Generate an STS certificate with the given commonName.
database | false | Toggle this to add a database with $name to your application.
database/<name> | | If you want to add multiple databases specify a name for each. Set the value to 'auto' for auto generation or a given ID to pin it.
