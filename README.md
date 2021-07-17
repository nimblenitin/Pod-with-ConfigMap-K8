# Pod-with-ConfigMap-K8
A ConfigMap allows you to decouple environment-specific configuration from your container images, so that your applications are easily portable. Pods can consume ConfigMaps as environment variables, command-line arguments, or as configuration files in a volume.

Simple example to demonstrate ConfigMap in a Pod-

Steps followed:

*As Root*
```

1. Create an index.html file
$ vi index.html

2. Create the ConfigMap file and checkout the file
$ kubectl create configmap nginx-cm --from-file index.html
$ kubectl describe cm nginx-cm

3. Create the Pod using the ConfigMap file
$ vi Pod_with_CM.yaml
$ kubectl apply -f  Pod_with_CM.yaml

4. Checkout the Pod created and it's IP address
$ kubectl get pod nginx-with-cm -o wide

5. Use the curl command to find whether ConfigMap works correctly.
curl <IP Address>

 ```
  *As Root*
