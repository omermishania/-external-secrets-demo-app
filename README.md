## Helm Chart Templates for using external secrets in cloudlet
This project provides template Helm Charts for using external secrets in application   into any Kubernetes based cloud (Cloudlet).

The templates require your application to built into a Docker image. The [Docker Image](https://hub.docker.com/r/bonomat/nodejs-hello-world)  provides in this demo assistance in displaying an example of external secret using helm-charts.

This project provides the following files:

| File                                              | Description                                                           |
|---------------------------------------------------|-----------------------------------------------------------------------|  
| `/chart/external-secret/Chart.yaml`                    | The definition file for your application                           | 
| `/chart/external-secret/values.yaml`                   | Configurable values that are inserted into the following template files      |        
| `/chart/external-secret/templates/external-secret.yaml`     | Template to configure your external secret resource.                 | 
| `/chart/external-secret/templates/pod.yaml`        | Template to configure your application pod.                 |
| `/chart/external-secret/templates/service.yaml`        | Template to configure your application service.                 |
| `/chart/external-secret/templates/route.yaml`          | Template to configure your application route.                 | 

In order to use these template files, copy the files from this project into your application directory. You should only need to edit the  `values.yaml` file.

## Configuring the Values for your Application

The following table lists the configurable parameters of the template Helm values.

| Parameter             | Description              | Default                              |
| ----------------------| -------------------------| -------------------------------------|
| `client_name`         | Client name to deploy    | None                                 |
| `cluster_name`        | Cluster Name             | `ocp43-dev`                          |
| `OC_APP_PATH`         | Path to App on OpenShift | `apps.ocp43-dev.cloudlet-dev.com`    |
