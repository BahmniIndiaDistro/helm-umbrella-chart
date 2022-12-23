Once the "custom-backend.yaml" and "custom-error.yaml" files are deployed, we need to do the following steps

1. Edit the ingress-nginx-controller Deployment and set the value of the "--default-backend-service" flag to the name of the newly created error backend with the namespace.

2. Edit the ingress-nginx-controller ConfigMap and create the key "custom-http-errors" with a value of "500".