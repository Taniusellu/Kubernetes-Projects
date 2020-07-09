Static Pods are managed directly by the kubelet daemon on a specific node, without the API server observing them. Unlike Pods that are managed 
by the control plane (for example, a Deployment); instead, the kubelet watches each static Pod (and restarts it if it crashes).

Static Pods are always bound to one Kubelet on a specific node.

The kubelet automatically tries to create a mirror Pod on the Kubernetes API server for each static Pod. This means that the Pods running on a node are visible on the API server,
 but cannot be controlled from there.
