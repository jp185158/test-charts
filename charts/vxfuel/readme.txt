There are two values files, values.xml, (which seems to be used by virtue of its presence by the edge deployment system),
but also there is local-values.yaml which can be provided to helm by hand on your local system to deploy to a local "kind" cluster.

The local-values.yaml deployment values expect the Docker registry to be available at localhost:5001.  You can verify this is in operation
by running (e.g., if you have a "vxfuel:latest" image in your local Docker image repository) by running:

   curl https://localhost:5001/v2/vxfuel/manifests/latest


