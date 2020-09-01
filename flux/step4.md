Flux can also be used to automate container image updates in your cluster, and it does so by continuously monitoring container registries and deploying new versions where applicable.

One way to enable this feature is by annotating your deployments using 

`fluxcd.io/automated: "true"`{{execute}}

You can also use `fluxcd.io/tag.app: semver:~1.0` to instruct flux to only update the image when you push an image tag that matches the semantic version expression e.g cloud-sample:1.0.1 but not cloud-sample:1.2.0.
