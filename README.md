# yaml
YAML Kubernetes manifests

 To create the Pod shown above, run the following command: 
 kubectl apply -f <link to a file>
 
---

## Manifest Portfolio

| NAME               | PROMPT                                              | DESCRIPTION                                                 | EXAMPLE                                              |
|-------------------------|-----------------------------------------------------|-------------------------------------------------------------|------------------------------------------------------|
| app.yaml                | Pod that run a single container                 | The following is an example of a Pod which consists of a container the image nginx: 1.14.2 | [app.yaml](https://github.com/gena460/yaml/blob/main/app.yaml)                |
| app-livenessProbe.yaml  | Liveness probe for the Pod                           | Configures a liveness probe for the Pod                    | [app-livenessProbe.yaml](https://github.com/dereban25/generate_manifest_k8s/blob/main/app-livenessProbe.yaml)  |
| app-readinessProbe.yaml | Readiness probe for the Pod                          | Configures a readiness probe for the Pod                   | [app-readinessProbe.yaml](https://github.com/dereban25/generate_manifest_k8s/blob/main/app-readinessProbe.yaml) |
| app-volumeMounts.yaml   | Volume mounts for the Pod                            | Defines volume mounts for the Pod                          | [app-volumeMounts.yaml](https://github.com/dereban25/generate_manifest_k8s/blob/main/app-volumeMounts.yaml)   |
| app-cronjob.yaml        | CronJob resource for scheduling jobs                  | Schedules jobs on a cron-like schedule                      | [app-cronjob.yaml](https://github.com/dereban25/generate_manifest_k8s/blob/main/app-cronjob.yaml)        |
| app-job | Short time running process | A simple case is to create one Job object in order to reliably run one Pod to completion. The Job object will start a new Pod if the first Pod fails or is deleted (for example due to a node hardware failure or a node reboot).
| app-multicontainer.yaml | Pod that run multiple containers that need to work together                         | Defines a Pod with multiple containers                      | [app-multicontainer.yaml](https://github.com/dereban25/generate_manifest_k8s/blob/main/app-multicontainer.yaml) |
| app-resources.yaml      | Resource limits and requests for the Pod             | Configures resource limits and requests for the Pod        | [app-resources.yaml](https://github.com/dereban25/generate_manifest_k8s/blob/main/app-resources.yaml)      |
| app-secret-env.yaml     | Use a Secret to set environment variables            | Retrieves values from a Secret as environment variables    | [app-secret-env.yaml](https://github.com/dereban25/generate_manifest_k8s/blob/main/app-secret-env.yaml)    |

---

