### How is AuroraConfig parsed
- given an ApplicationId determine what files to use. See anchor:Files[]
- extract and validate the DeploymentSpecHeader from the given files using the HeaderMapper See anchor:Header[]
- extract and validate DeploymentSpec from the FieldMappers.
-- different fieldMappers are used for the different types
- generate objects according to the type field.
-- for deploy and development the generate process uses an DSL in Kotlin to generate the objects
-- for tempalte and localTemplate a template is applied
- enrich the generate objects with information from the DeploymentSpec
- the objects are created/updated in the cluster
-- note that this process does not use 'oc apply' on the objects. The state in the cluster is overwritten.
