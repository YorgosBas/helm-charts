# Installing the http-echo Chart
To install the http-echo chart from this repository, run:

```helm install my-http-echo my-helm-charts/http-echo```

This command deploys the http-echo service on your Kubernetes cluster using the default configuration. The configuration section lists the parameters that can be configured during installation.

## Configuration
The following table lists the configurable parameters of the `http-echo` chart and their default values.

| Parameter           | Description               | Default                 |
|---------------------|---------------------------|-------------------------|
| `replicaCount`      | Number of replicas        | `2`                     |
| `image.repository`  | Image repository          | `hashicorp/http-echo`   |
| `image.tag`         | Image tag                 | `"0.2.3"`               |
| `image.pullPolicy`  | Image pull policy         | `IfNotPresent`          |
| `service.type`      | Kubernetes Service type   | `NodePort`              |
| `service.port`      | Service port              | `8081`                  |


```helm install my-http-echo my-helm-charts/http-echo --set replicaCount=3```

### Exposing the service
Once deployed you can access the service with 
```kubectl port-forward svc/http-echo-svc-name -n http-echo 8081```. However it would be better to set up an ingress for production use

## Uninstalling the Chart
To uninstall/delete the my-http-echo deployment:

```helm delete my-http-echo```

This command removes all the Kubernetes components associated with the chart and deletes the release.
