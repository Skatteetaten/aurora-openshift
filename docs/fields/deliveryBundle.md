releaseTo                      |              | Used to release a given version as a shared tag in the docker registry. Other env can then use it in 'version'. NB! Must be manually updated with ao/console
path                           | default      | description
debug                          | false        | Toggle to enable remote debugging on port 5005. Port forward this port locally and setup remote debugging in your Java IDE.
deployStrategy/type            | rolling      | Specify type of deployment, either rolling or recreate
deployStrategy/timeout         | 180          | Set timeout value in seconds for deployment process
resources/cpu/min              | 100m         | Specify minimum/request cpu. 1000m is 1 core.
resources/cpu/max              | 2000m        | Specify maximum/limit cpu.
resources/memory/min           | 128Mi        | Specify minimum/request memory.
resources/memory/max           | 512Mi        | Specify maximum/limit memory. By default 25% of this will be set to XMX in java.
groupId                        |              | groupId for your application.  Max 200 length. Required if deploy/development
artifactId                     | $fileName    | artifactId for your application. Max 50 length
splunkIndex                    |              | Set to a valid splunk-index to log to splunk. Only valid if splunk is enabled in the Aurora API
serviceAccount                 |              | Set to an existing serviceAccount if you need special privileges
prometheus                     | true         | Toggle to false if application do not have Prometheus metrics
prometheus/path                | /prometheus  | Change the path of where prometheus is exposed
prometheus/port                | 8081         | Change the port of where prometheus is exposed
management                     | true         | Toggle of if your application does not expose an management interface
management/path                | /actuator    | Change the path of where the management interface is exposed
management/port                | 8081         | Change the port of where the management interface is exposed
readiness                      | true         | Toggle to false to turn off default readiness check
readiness/path                 |              | Set to a path to do a GET request to that path as a readiness check
readiness/port                 | 8080         | If no path present readiness will check if this port is open
readiness/delay                | 10           | Number of seconds to wait before running readiness check
readiness/timeout              | 1            | Number of seconds timeout before giving up readiness
liveness                       | false        | Toggle to true to enable liveness check
liveness/path                  |              | Set to a path to do a GET request to that path as a liveness check
liveness/port                  | 8080         | If no path present liveness will check if this port is open
liveness/delay                 | 10           | Number of seconds to wait before running livenss check
liveness/timeout               | 1            | Number of seconds timeout before giving up livenss
replicas                       | 1            | Number of replicas of this application to run.
pause                          | false        | Toggle to pause an application. This will scale it down to 0 and add a label showing it is paused.
