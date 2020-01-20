custom-template
===============
Basically the same as the nginx-ingress chart, but using a custom template to include some other content

Current chart version is `0.2.0`

Source code can be found [here](https://github.com/norwoodj/helm-docs/tree/master/example-charts/custom-template)

## Additional Information
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore
et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut
aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse
cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in
culpa qui officia deserunt mollit anim id est laborum.

## Chart Requirements

| Repository | Name | Version |
|------------|------|---------|
| @stable | nginx-ingress | 0.22.1 |

## Chart Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| controller.extraVolumes[0].configMap.name | string | `"nginx-ingress-config"` | Uses the name of the configmap created by this chart |
| controller.extraVolumes[0].name | string | `"config-volume"` |  |
| controller.image.repository | string | `"nginx-ingress-controller"` |  |
| controller.image.tag | string | `"18.0831"` |  |
| controller.ingressClass | string | `"nginx"` | Name of the ingress class to route through this controller |
| controller.name | string | `"controller"` |  |
| controller.persistentVolumeClaims | list | Use this to override the default value specified here in the file | List of persistent volume claims to create. For very long comments, break them into multiple lines. |
| controller.podLabels | object | `{}` | The labels to be applied to instances of the controller pod |
| controller.publishService.enabled | bool | `false` | Whether to expose the ingress controller to the public world |
| controller.replicas | int | `nil` | Number of nginx-ingress pods to load balance between |
| controller.service.annotations."external-dns.alpha.kubernetes.io/hostname" | string | `"stupidchess.jmn23.com"` | Hostname to be assigned to the ELB for the service |
| controller.service.type | string | `"LoadBalancer"` |  |
