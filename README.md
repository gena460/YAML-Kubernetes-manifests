# yaml
YAML Kubernetes manifests

 To create the Pod shown above, run the following command: 
 kubectl apply -f <link to a file>
 
---

## Manifest Portfolio

| NAME               | PROMPT                                              | DESCRIPTION                                                 | EXAMPLE                                              |
|-------------------------|-----------------------------------------------------|-------------------------------------------------------------|------------------------------------------------------|
| app.yaml                | Pod that run a single container                 | The following is an example of a Pod which consists of a container the image nginx: 1.14.2 | [app.yaml](https://github.com/gena460/YAML-Kubernetes-manifests/blob/main/yaml/app.yaml)                |
| app-livenessProbe.yaml  | Liveness probe for the Pod                           | In the configuration file, you can see that the Pod has a single Container. The periodSeconds field specifies that the kubelet should perform a liveness probe every 5 seconds. The initialDelaySeconds field tells the kubelet that it should wait 5 seconds before performing the first probe. To perform a probe, the kubelet executes the command cat /tmp/healthy in the target container. If the command succeeds, it returns 0, and the kubelet considers the container to be alive and healthy. If the command returns a non-zero value, the kubelet kills the container and restarts it.              | [app-livenessProbe.yaml](https://github.com/gena460/YAML-Kubernetes-manifests/blob/main/yaml/app-livenessProbe.yaml)  |
| app-readinessProbe.yaml | Readiness probe for the Pod                          | Readiness probe is defined exactly like the Liveness probe. We just need to replace livenessProbe with readinessProbe. Both liveness & readiness probes are used to control the health of an application. Failing liveness probe will restart the container, whereas failing readiness probe will stop application from serving traffic.                   | [app-readinessProbe.yaml](https://github.com/gena460/YAML-Kubernetes-manifests/blob/main/yaml/app-readinessProbe.yaml) |
| app-volumeMounts.yaml   | Configure a volume for a Pod                  | This Pod has a Volume of type emptyDir that lasts for the life of the Pod, even if the Container terminates and restarts                   | [app-volumeMounts.yaml](https://github.com/gena460/YAML-Kubernetes-manifests/blob/main/yaml/app-volumeMounts.yaml)   |
| app-cronjob.yaml        | A CronJob creates Jobs on a repeating schedule                  | This example CronJob manifest prints the current time and a hello message every minute                      | [app-cronjob.yaml](https://github.com/gena460/YAML-Kubernetes-manifests/blob/main/yaml/app-cronjob.yaml)        |
| app-job | Short time running process | A simple case is to create one Job object in order to reliably run one Pod to completion. The Job object will start a new Pod if the first Pod fails or is deleted (for example due to a node hardware failure or a node reboot).| [app-multicontainer.yaml](https://github.com/gena460/YAML-Kubernetes-manifests/blob/main/yaml/app-job.yaml) |
| app-multicontainer.yaml | Pod that run multiple containers that need to work together                         | Defines a Pod with multiple containers                      | [app-multicontainer.yaml](https://github.com/gena460/YAML-Kubernetes-manifests/blob/main/yaml/app-multicontainer.yaml) |
| app-resources.yaml      | Resource limits and requests for the Pod             | Configures resource limits and requests for the Pod        | [app-resources.yaml](https://github.com/gena460/YAML-Kubernetes-manifests/blob/main/yaml/app-resources.yaml)      |
| app-secret-env.yaml     | A Secret can be used with your workloads in two ways: 1)specify environment variables that reference the Secret’s values; 2) mount a volume containing the Secret.            | Retrieves values from a Secret as environment variables    | [app-secret-env.yaml](https://github.com/gena460/YAML-Kubernetes-manifests/blob/main/yaml/app-secret-env.yaml)    |

---

