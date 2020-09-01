Flux's main feature is the automated synchronisation between a version control repository and a cluster. In other words, if you make any changes to your repository, those changes are automatically deployed to your cluster.

In order to sync, you need to give flux write access to the repository. At startup Flux generates a SSH key and its public key can be obtainer by running:

`fluxctl identity --k8s-fwd-ns flux`{{execute}}

Now, create a deploy key on your GitHub repository. Make sure you check ***Allow write access**.

By default, Flux git pull frequency is set to 5 minutes. However, you can tell flux to sync the changes immediately with:

`fluxctl sync --k8s-fwd-ns flux`{{execute}}

If you now run `fluxctl get pods -n cloud-training`{{execute}} you can see pods are starting.