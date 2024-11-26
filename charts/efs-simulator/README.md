# EFS Simulator
Version 0.11.38

## Overview
This chart will deploy the EFS Simulator.
It contains:
* Simulator
* Mosquitto broker

Ports are currently hardcoded:
Cluster Ports:
| port | description    |
| -----| -------------- |
| 8000 | Simulator API  |
| 9001 | MQTT Websocket |
| 1883 | MQTT TCP       |

Ingress Ports (Outside of the cluster):
| port | description    |
| -----| -------------- |
| 80   | Simulator API  |
| 9001 | MQTT Websocket |
| 1883 | MQTT TCP       |

Example Simulator API Call
NOTE:  specifying -k to simplify the certificate validation.  This isn't needed if you register the edge certificate on your machine.
You will need to register the "efs-simulator.store.ncr.corp" host in your hosts file and point to the cluster IP.

```
curl -k -v -X POST -d "IDLE" https://efs-simulator.store.ncr.corp/web/pump/2/status
```
