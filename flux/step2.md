Create the flux namespace:

`kubectl create ns flux`{{execute}}

Install flux:

```
export GHUSER="gonzalobarbitta"
fluxctl install \
--git-user=${GHUSER} \
--git-email=${GHUSER}@users.noreply.github.com \
--git-url=git@github.com:${GHUSER}/flux-training \
--git-path=workloads \
--namespace=flux | kubectl apply -f -
```{{execute}}
