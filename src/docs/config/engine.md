| Name | Type | Default Value | Environment Var | Description |
 | :--- | :--- | :--- | :--- | :--- |
 | *agentproxy.enabled* | bool | false |  | The enabled flag for agent proxy |
| *autoremove_engines* | bool | true | _AIWARE_AUTOREMOVE_ENGINES_ | If enabled, the docker container for engine instances will be removed after the engine instance completes |
| *image* | string | prom/prometheus:v2.21.0 | _AIWARE_PROMETZHEUS_IMAGE_ | This specifies docker image to use for the prometheus service.   |
| *port* | int64 | 9090 | _AIWARE_PROMETHEUS_PORT_ | This specifies port to use for NFS. |
| *root* | string | /opt/aiware/prometheus | _AIWARE_PROMETHEUS_ROOT_ | *Secure* The root to use for prometheus |
