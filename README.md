# java-spring-example-charts
Helm charts to deploy the java spring example application

These charts can be used to deploy the [java spring polls example application](https://github.com/Blueshoe/java-spring-example-charts), which is done in one of the [Unikube guides](#https://unikube.io).

They are designed to be run with Unikube, i.e. [k3d](https://k3d.io/) as a kubernetes cluster. 
This is reflected in `values.yaml` in `ingress.annotations`, where `traefik` is set. 
If this doesn't reflect your setup, feel free to change it.

The charts deploy the `latest`-tag of the image, which of course is not something you would generally want to do. 
But as this is only an example application we're fine with that.

The charts don't contain any probes for the polls deployment. 
Upon initial installation, the application pod will be running immediately, although the database isn't ready yet.
