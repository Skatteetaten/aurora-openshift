# Why do wo not use s2i

[S2i](https://docs.openshift.org/latest/architecture/core_concepts/builds_and_image_streams.html#source-build) is an abstraction for building DockerImages that is provided out of the box in OpenShift.

 - Applications are delivered as DeliveryBundle that is security scanned in Nexus IQ
 - Jenkins already compiles everything for testing, not need to do this again
 - We push several tags for each build not just one
 
Instead we use a CustomBuilder strategy that still gets the benefits from s2i, but insted of building the artifact 
that is in the DockerImage from source we fetch something that is already built.
 
 
