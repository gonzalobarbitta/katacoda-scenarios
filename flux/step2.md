Create the flux namespace:

`kubectl create ns flux`{{execute}}

Since you will need to create a deploy key flux to work, if you haven't done it already, please fork [this repository](https://github.com/gonzalobarbitta/flux-training) on GitHub.

Once forked, replace `GHUSER` with your username, and run the command:

`export GHUSER="gonzalobarbitta"`

Then, install flux in your cluster:

```
fluxctl install \
--git-user=${GHUSER} \
--git-email=${GHUSER}@users.noreply.github.com \
--git-url=git@github.com:${GHUSER}/flux-training \
--git-path=workloads \
--namespace=flux | kubectl apply -f -
```{{execute}}

Wait for Flux to start:

`kubectl -n flux rollout status deployment/flux`{{execute}}