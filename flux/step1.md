Online terminal comes with minikube and kubectl installed. You can check that kubectl is configured to talk to your cluster, by running:

`kubectl version`{{execute}}

OK, kubectl is installed and you can see both the client and the server versions.

To view the nodes in the cluster, run:

`kubectl get nodes`{{execute}}

Here we see the available nodes (1 in our case). Kubernetes will choose where to deploy our application based on Node available resources.

Next up, we need to install fluxct, a command-line tool that can talk to Weave Flux. We do this by running:

`snap install fluxctl --classic`{{execute}}