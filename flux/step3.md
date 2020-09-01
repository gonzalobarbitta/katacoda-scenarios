Flux's main feature is the automated synchronisation between a version control repository and a cluster. In other words, if you make any changes to your repository, those changes are automatically deployed to your cluster.

`fluxctl sync --k8s-fwd-ns flux`{{execute}}

At startup, flux generates a SSH key. SSH public key can be found running:

`fluxctl identity --k8s-fwd-ns flux`{{execute}}

Copy this key and create a deploy key with write access on your GitHub repository.